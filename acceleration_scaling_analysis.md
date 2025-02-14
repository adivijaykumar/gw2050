## Scaling analysis for acceleration (and higher order derivatives thereof) constraints

For GWs from CBCs, the best measured mass scale is the detector-frame (or "redshifted") chirp mass $`M^{\rm det}_{\rm chirp}`$. In the discussion that follows, let's assume that the cosmological redshift and its derivatives are negligible (i.e. the source is quite nearby). It is easy to add in the cosmological redshift later, and the derivatives of the cosmological redshift will be negligible/immeasurable at most epochs in the Universe. Under these assumptions, one can write

```math
M^{\rm det}_{\rm chirp} = M^{\rm src}_{\rm chirp} (1 + z_{\rm dop}) \ .
```

The doppler shift $z_{\rm dop} = v / c$. This means that acceleration will essentially generate a time-dependent doppler shift. Let's Taylor expand $z_{\rm dop}$:

$$z_{\rm dop} = \frac{v}{c} = \frac{v_0}{c} + \frac{a}{c} t + \frac{\dot{a}}{c} \frac{t^2}{2} + \frac{\ddot{a}}{c} \frac{t^3}{6} + \ldots $$

A constant doppler shift is _completely_ degenerate with the measurement of chirp mass. In any case, $v_0$ would be small, so let's just ignore that term.

$$ z_{\rm dop} = \frac{a}{c} t + \frac{\dot{a}}{c} \frac{t^2}{2} + \frac{\ddot{a}}{c} \frac{t^3}{6} + \ldots $$

As mentioned earlier, $`M^{\rm det}_{\rm chirp}`$ is quite well measured. Many studies have calculated the measurability of a (time-constant) $`M^{\rm det}_{\rm chirp}`$. Let's denote the uncertainty estimate obtained using such a measurability analysis as $`{\sigma_{\rm chirp}}`$. This is given by (see e.g. [Cutler and Flanagan 1994](https://arxiv.org/abs/gr-qc/9402014)):

```math
\frac{\sigma_{\rm chirp}}{M^{\rm det}_{\rm chirp}} = \alpha_{\rm chirp} \ \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{5/3} \  \frac{10}{\rm SNR} \, ,
```
where $\alpha_{\rm chirp}$ is a constant that depends on the properties of the detector power spectral density (PSD). [Cutler and Flanagan 1994](https://arxiv.org/abs/gr-qc/9402014) say that $\alpha_{\rm chirp} = 1.2 \times 10^{-5}$ for Advanced LIGO.

Typically, $\alpha_{\rm chirp}$ is quite small, especially for low frequency detectors. If the time variation of the doppler shift causes a change in chirp mass by more than $\sigma_{\rm chirp}$, such a doppler shift can be measured! Mathematically, this condition boils down to:

```math
M^{\rm src}_{\rm chirp} |\frac{a}{c} T + \frac{\dot{a}}{c} T^2/2 + \frac{\ddot{a}}{c} T^3/6| \geq \sigma_{\rm chirp}
```

Here, $T$ is the in-band duration of the signal. We know from GW emission timescales that 

```math
\frac{T}{\rm sec} \approx  10^3 \ \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{-8/3} \left( \frac{M^{\rm det}_{\rm chirp}}{M_\odot} \right)^{-5/3}
```

To start with, let's assume $\dot{a}$, $\ddot{a}$ are negligible. This gives us a simpler condition:

```math
\frac{|a|}{c} T \geq \frac{\sigma_{\rm chirp}}{ M^{\rm src}_{\rm chirp}} \approx \alpha_{\rm chirp} \ \frac{10}{\rm SNR} \ \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{5/3}
```

This can be further reduced to:
```math
\frac{|a|}{c}  \geq \frac{10^{-3}}{\rm sec} \ \alpha_{\rm chirp} \  \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{8/3} \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{10/3} \  \frac{10}{\rm SNR}
```

This is the scaling law we need. As is evident, the minimum measureable acceleration depends on a strong power of chirp mass and minimum frequency. This makes sense, since both these quantities affect the estimation of chirp mass. **NOTE: correct this statement because alpha also depends on flow**.

Let's assume we are near a supermassive black hole of mass $M_{\rm SMBH}$. For simplicitly, let the distance $r$ be expressed in terms of the gravitational radius i.e. $r = n \ R_g = n \  G\ M_{\rm SMBH}/c^2$. Therefore, $a(r) =  G M_{\rm SMBH} / r^2 = c^4 ( G M n^2)^{-1}$. Combining this with the above scaling law:

```math
\frac{2 \times 10^{-5}}{\rm sec} \ \left(\frac{M_{\rm SMBH}}{10^6\,M_\odot}\right)^{-1} \left(\frac{n}{100}\right)^{-2}    \geq \frac{10^{-3}}{\rm sec} \ \alpha_{\rm chirp} \  \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{8/3} \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{10/3} \  \frac{10}{\rm SNR}
```

```math
 \left(\frac{n}{100}\right)^{-2}  \geq 50 \ \alpha_{\rm chirp} \  \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{8/3} \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{10/3} \ \left(\frac{M_{\rm SMBH}}{10^6\,M_\odot}\right) \ \frac{10}{\rm SNR}
```

```math
\frac{n}{100}  \leq ( 50 \ \alpha_{\rm chirp})^{-1/2}  \  \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{-4/3} \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{-5/3} \ \left(\frac{M_{\rm SMBH}}{10^6\,M_\odot}\right)^{-1/2} \ \left(\frac{\rm SNR}{10}\right)^{1/2}
```

For Advanced LIGO, assuming the value of $\alpha_{\rm chirp}$ from [Cutler and Flanagan 1994](https://arxiv.org/abs/gr-qc/9402014), and $f_{\rm low} = 10 {\rm Hz}$:

```math
\frac{n}{4100}  \leq  \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{-5/3} \ \left(\frac{M_{\rm SMBH}}{10^6\,M_\odot}\right)^{-1/2} \ \left(\frac{\rm SNR}{10}\right)^{1/2}
```

If instead we were interested in general gravitational potentials that predicted enclosed mass $M_{\rm enc}(R)$ in an orbit of radius $R$, the scaling law would be modified as follows (adding back dependence on $\alpha_{\rm chirp}$ and $f_{\rm low}$):

```math
\frac{R}{40\, {\rm au}} \leq \left(\frac{\alpha_{\rm chirp}}{1.2 \times 10^{-5}}\right)^{-1/2}  \  \left(  \frac{f_{\rm low}}{\rm 10\, Hz}\right)^{-4/3} \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{-5/3} \left(\frac{M_{\rm enc}(R)}{10^6\,M_\odot}\right)^{1/2} \left(\frac{\rm SNR}{10}\right)^{1/2}
```
For DECIGO, assuming $\alpha_{\rm chirp} = 2.3 \times 10^{-9}$ and $f_{\rm low} = 0.1 {\rm Hz}$,

```math
\frac{R}{6.5\, {\rm pc}} \leq   \left(\frac{M^{\rm det}_{\rm chirp}}{M_\odot}\right)^{-5/3} \left(\frac{M_{\rm enc}(R)}{10^6\,M_\odot}\right)^{1/2} \left(\frac{\rm SNR}{10}\right)^{1/2}
```
