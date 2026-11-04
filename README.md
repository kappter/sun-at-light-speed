# Sun and Moon at Light Speed

Kenneth Kapptie's interactive classroom thought experiment: hold Earth fixed, place the Sun or Moon on a circular path around Earth's center, and give the selected body an adjustable orbital speed.

Original hosted app: https://light-speed-sky.kappter.chatgpt.site

## Run

Open \`index.html\` in a modern browser. No installation, dependencies, API keys, or build step are required. Alternatively run \`python3 -m http.server 8000\` in this directory and open http://localhost:8000.

## Explore

- Adjust the orbital speed from zero to the speed of light using the slider or numeric input.
- Compare the overhead orbit with the equatorial observer's sky.
- Pause or reset the animation.
- Read the orbital period, horizon-to-horizon time, angular speed, disk-crossing time, and light-travel delay.

## Model and assumptions

This is a geometric thought experiment, not a physically possible orbit. Earth is stationary at the center of a circular path. The orbit radius is fixed at the selected center-to-center distance:

- **Sun mode:** $r = 1\,\mathrm{AU} = 149{,}597{,}870.7\,\mathrm{km}$, the nominal mean Earth–Sun distance used by the model.
- **Moon mode:** $r = 384{,}400\,\mathrm{km}$, the Moon's mean semimajor axis / average Earth–Moon distance.

The speed input is the body's tangential speed along that circle. Gravity, Earth's rotation, orbital eccentricity and inclination, relativistic effects, and changes in the Earth–body distance are excluded. A massive Sun or Moon cannot travel at the speed of light. The sky view treats the observer as located at Earth's equator in the orbit plane; it shows the body's earlier position when its light reaches Earth. The Moon is drawn as a visible marker, without lunar phases or illumination.

The overhead diagram fits each selected orbit to the same graphic size. It therefore does **not** show Sun and Moon distances to a common scale.

## Orbital math

Let $r$ be the fixed orbital radius, $v$ the selected speed, and $c$ the speed of light. For a circular path:

$$
C_{\mathrm{orbit}} = 2\pi r
\qquad
T = \frac{C_{\mathrm{orbit}}}{v} = \frac{2\pi r}{v}
\qquad
\omega = \frac{v}{r}
$$

Here $C_{\mathrm{orbit}}$ is the distance around one full circle, $T$ is the time for one revolution, and $\omega$ is angular speed in radians per second. At $v=0$, the period is infinite and angular speed is zero.

For the idealized equatorial observer, the body is above the horizon for half a revolution. Therefore:

$$
t_{\mathrm{horizon\ to\ horizon}} = \frac{T}{2} = \frac{\pi r}{v}
\qquad
\text{angular speed in degrees/minute} =
\frac{v}{r}\,\frac{180}{\pi}\,60
$$

The one-way light-travel delay is set by distance and light speed, not by the body's orbital speed:

$$
t_{\mathrm{light}} = \frac{r}{c}
$$

At a steady orbital speed, the apparent angular lag is:

$$
\Delta\theta = \omega t_{\mathrm{light}}
= \frac{v}{r}\,\frac{r}{c}
= \frac{v}{c}\text{ radians}
$$

Thus, at $v=c$, the observed position trails the current position by exactly $1$ radian, or $57.2958^\circ$, for either radius. The radius cancels; this is why the Sun and Moon have the same angular lag at light speed even though their periods and light delays are very different.

### Results at the speed of light

The app uses $c = 299{,}792.458\,\mathrm{km/s}$ (the exact SI value $299{,}792{,}458\,\mathrm{m/s}$, converted to km/s).

| Quantity | Sun at 1 AU | Moon at 384,400 km |
|---|---:|---:|
| Orbit circumference, $2\pi r$ | 939,951,143.168 km | 2,415,256.432 km |
| Full-orbit period, $2\pi r/c$ | 3,135.3395 s = **52 min 15.34 s** | 8.05643 s |
| Horizon-to-horizon, $\pi r/c$ | 1,567.6698 s = **26 min 7.67 s** | 4.02821 s |
| Angular speed, $c/r$ | 6.88921°/min | 2,681.09°/min |
| Light-travel delay, $r/c$ | 499.0048 s = **8 min 19.00 s** | 1.28222 s |
| Apparent angular lag, 1 radian | 57.2958° | 57.2958° |

Values are rounded for display. The calculations use the listed radii and the unrounded SI speed of light.

### Apparent disk crossing

The “across its own width” readout is the apparent angular diameter divided by angular speed. The Sun uses the model's fixed apparent diameter of $0.533^\circ$. For the Moon, the app estimates angular diameter from its $3{,}474\,\mathrm{km}$ physical diameter and the fixed center-to-center distance:

$$
\delta_{\mathrm{Moon}} =
2\tan^{-1}\!\left(\frac{3{,}474\,\mathrm{km}}{2r}\right)
\approx 0.517805^\circ
\qquad
t_{\mathrm{disk}} = \frac{\delta}{\omega}
$$

At $c$, the model gives about **4.642 s** to move across the Sun's $0.533^\circ$ apparent width and **0.01159 s (11.59 ms)** across the Moon's modeled apparent width. These are idealized angular-crossing times; they do not model a real observer's changing distance, atmospheric effects, or relativistic appearance.

## Playback and delayed sky view

The **Real time (1×)** checkbox selects one simulated second per real second. When unchecked, animation uses 100× time-lapse. These playback settings affect only animation speed; the metric calculations always use the entered orbital speed.

The overhead view shows the current position. The sky view uses the position at emission time, approximately $r/c$ earlier. Changing speed is added to the motion history, so its effect reaches the sky view after the corresponding light-travel delay. Reset initializes a steady orbit at the selected speed.

## Reference values

- Speed of light: [NIST, speed of light in vacuum](https://physics.nist.gov/cgi-bin/cuu/Value?c%7Csearch_for=c) — exactly 299,792,458 m/s.
- Astronomical unit and light time: [JPL Solar System Dynamics, Astrodynamic Parameters](https://ssd.jpl.nasa.gov/astro_par.html) — 1 au = 149,597,870,700 m and light time for 1 au = 499.004783836 s.
- Mean lunar distance: [JPL Solar System Dynamics, Lunar Distance glossary](https://ssd.jpl.nasa.gov/glossary/LD.html) — mean semimajor axis 384,400 km. NASA also describes 384,400 km as the average Earth–Moon distance in [Moon by the Numbers](https://science.nasa.gov/moon/by-the-numbers/).
- Lunar diameter: [NASA/JPL, Comparing Apparent Sizes of Moons](https://science.nasa.gov/resource/illustration-comparing-apparent-sizes-of-moons/) — 3,474 km.
- Sun apparent diameter used by this model: 0.533° (a fixed model input).

## GitHub Pages

In repository Settings > Pages, choose **Deploy from a branch**, select \`main\` and \`/(root)\`, and save.

## Source

Recovered from the original Sun at Light Speed site on November 3, 2026. The application HTML is unchanged. Site-specific hosting metadata and Git credentials are excluded.
