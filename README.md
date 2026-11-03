# Sun and Moon at Light Speed

Kenneth Kapptie's interactive classroom thought experiment: hold Earth and the Sun one astronomical unit apart, keep Earth stationary, and give the Sun an adjustable orbital speed.

Original hosted app: https://light-speed-sky.kappter.chatgpt.site

## Run

Open `index.html` in a modern browser. No installation, dependencies, API keys, or build step are required. Alternatively run `python3 -m http.server 8000` in this directory and open http://localhost:8000.

## Explore

- Adjust the speed from zero to the speed of light using the slider or numeric input.
- Compare the overhead orbit and the equatorial observer's sky.
- Pause or reset the animation.
- Read orbital period, horizon-to-horizon time, angular speed, solar-diameter crossing time, and sunlight travel delay.

## Model

This is a deliberately nonphysical visualization. Gravity, relativistic effects, and Earth's rotation are excluded; a real Sun cannot move at light speed. The overhead view shows the Sun's current position. The sky view uses the position at emission time, approximately 499 seconds earlier, for a central observer at fixed 1 AU. Speed changes propagate through this history after that delay. Finite Earth/Sun size, aberration, Doppler shifts, and relativistic appearance are not modeled.

Constants: c = 299,792.458 km/s; 1 AU = 149,597,870.7 km. The Real time (1×) checkbox selects actual elapsed-time playback; unchecked uses 100× time-lapse. Calculated measurements use the selected orbital speed without the playback multiplier. Reset initializes a steady orbit at the selected speed.

At c, one orbit takes approximately 52 minutes 15 seconds, horizon to horizon takes 26 minutes 8 seconds, and sunlight crosses 1 AU in about 8 minutes 19 seconds.

## GitHub Pages

In repository Settings > Pages, choose Deploy from a branch, select main and /(root), and save.

## Source

Recovered from the original Sun at Light Speed Site on November 3, 2026. The application HTML is unchanged. Site-specific hosting metadata and Git credentials are excluded.

## Moon mode

Select Moon to use NASA's average center-to-center Earth–Moon distance of 384,400 km. Moon mode automatically selects real-time playback. At c, one orbit is approximately 8.06 seconds, the visible half-orbit is 4.03 seconds, and light travel time is 1.28 seconds. The sky view uses that delayed motion history. Each orbit is fitted independently to the overhead diagram; it does not show Sun/Moon distances to a common physical scale. The Moon is a visible marker; lunar phases and illumination, surface parallax, gravity, and relativity are excluded.

Distance source: https://science.nasa.gov/moon/by-the-numbers/
