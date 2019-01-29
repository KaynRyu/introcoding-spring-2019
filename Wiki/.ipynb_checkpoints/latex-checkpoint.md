# LaTeX equations

LaTeX is a typesetting that allows technical writers and scientists to write focusing on the content and without worrying abou the format. LaTeX is free under the terms of the LaTeX Project Public License (LPPL).

>A nice feature of LaTeX is that there is a specific syntax for equations. For instance, you can define inline equations so that this: `$y=mx+b$`, get's converted into this: $y=mx+b$

It is also possible to write equations in separate lines. For instance,

Simple center-aligned equation,
\begin{align}
y = e^{-x}
\end{align}

Compact and spaced equations,

\begin{align*}
f(x) =& x^2\! +3x\! +2 \\
f(x) =& x^2\, +3x\, +2 \\
f(x) =& x^2\ +3x\ +2 \\
f(x) =& x^2\quad +3x\quad +2 \\
f(x) =& x^2\qquad +3x\qquad +2
\end{align*}

Split equation,

\begin{equation}
\begin{split}
  A ={} & B + C + D + E + F + \\
        & G + H + I + \dots, \quad\text{while $x$ is true}.
\end{split}
\end{equation}

<br/>

Below is a set of equations obtained from the [FAO 56 manual](http://www.fao.org/docrep/X0490E/X0490E00.htm) to calculate reference evapotranspiration. Use this equations as templates to learn how to implement your own equations.

<br/>

## Reference Evapotranspiration Equation

Penman-Monteith model:

$$ETo = \frac{0.408\Delta(Rn-G)+\gamma\frac{900}{T+273}u2(es-ea)}{\Delta+\gamma(1+0.34u2)}$$

ETo   = reference evapotranspiration (mm/day)

Rn    = net radiation at the crop surface (MJ/m2/day)

G     = soil heat flux density (MJ/m2/day)

T     = mean daily air temperature at 2 m height

u2    = wind speed at 2 m height (m/s)

es    = saturation vapor pressure (kPa)

ea    = actual vapor pressure (kPa)

es-ea = saturation vapor pressure deficit (kPa)

$\Delta$ = slope vapor pressure curve (kPa/°C)

$\gamma$ = psychrometric constant (kPa/°C)


<br/>

    
### Psychrometric constant  

> Eq. 8 in the FAO-56 amual

$$\gamma = \frac{Cp P}{\epsilon \lambda}$$

$\gamma$ = psychrometric constant (kPa/°C)

$\lambda$ = latent heat of vaporization, 2.45 (MJ/kg)

Cp = specific heat at constant pressure (MJ/kg/°C)

$\epsilon$ = ratio of molecular weight of water vapour/dry air = 0.622

P = atmospheric pressure (kPa)

z = elevation above sea level (m)


<br/>


### Wind speed 

Wind speed must be corrected to 2 meter above the soil surface (FAO-56 manual, Eq. 47):

$$u2 = uz\frac{4.87}{\ln(67.8z-5.42)}$$ 

u2 = wind speed at 2 m above ground surface (m/s)

uz = measured wind speed at z m above ground surface (m/s)

zm = height of measurement above ground surface (m)

<br/>

### Air temperature

Tmax = weather(:,3);
Tmin = weather(:,4);
Tmean = (Tmax + Tmin)/2;   % Eq. 9, FAO-56
T = Tmean;

<br/>

### Air humidity
> Mean saturation vapor pressure as defined in Eq. 12, FAO-56

$$es = \frac{eTmax+eTmin}{2}$$                                              

> es = mean saturation vapor pressure (kPa)

eTmax = saturation vapor pressure at temp Tmax (kPa)

eTmin = saturation vapor pressure at temp Tmin (kPa)

eTmax = 0.6108*exp(17.27*Tmax./(Tmax+237.3)); % Eq. 11, FAO-56
eTmin = 0.6108*exp(17.27*Tmin./(Tmin+237.3));
es = (eTmax + eTmin) / 2;

<br/>

### Slope of vapor pressure
Slope of saturation of vapor pressure curve ($\Delta$) as defined in Eq. 13, FAO-56

$$\Delta = \frac{4098\bigg[0.6108\exp\bigg(\frac{17.27 Tmean}{Tmean+237.3}\bigg)\bigg]}{(Tmean+237.3)^2}$$   

$\Delta$ = slope of saturation vapor pressure curve at air temp T (kPa/°C)

Tmean = average daily air temperture

<br/>

### Actual vapor pressure 
Equation derived from relative humidity data as defined in Eq. 17, FAO-56:

$$ea = \frac{eTmin\frac{RHmax}{100}+eTmax\frac{RHmin}{100}}{2}$$ 

ea = actual vapor pressure (kPa)

eTmax = saturation vapor pressure at temp Tmax (kPa)

eTmin = saturation vapor pressure at temp Tmin (kPa)

RHmax = maximum relative humidity (%)

RHmin = minimum relative humidity (%)

<br/>

### Extraterrestrial solar radiation
Extraterrestrial radiation for daily periods as defined in Eq. 21, FAO-56:

$$Ra = \frac{24(60)}{\pi} \hspace{2mm}Gsc \hspace{2mm} dr[\omega\sin(\phi)\sin(\delta)+\cos(\phi)\cos(\delta)\sin(\omega)]$$

Ra = extraterrestrial radiation (MJ / m2 /day)

Gsc = solar constant (MJ/m2/min)   

dr = 1 + 0.033$\cos$(2$\pi$J/365)  (inverse relative distance Earth-Sun)                         
J = number of the day of the year   

$\phi$ = $\pi$/180decimal degrees  (latitude in radians)     

$\delta = 0.409\sin((2\pi J/365)-1.39)\hspace{5mm}$ Solar decimation (rad)

$\omega = \pi/2-(\arccos(-\tan(\phi)\tan(\delta)) \hspace{5mm}$ sunset hour angle (radians)