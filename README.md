# Sun at Light Speed

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

This is a deliberately nonphysical visualization. Gravity, relativistic effects, and Earth's rotation are excluded; a real Sun cannot move at light speed. The displayed sky position follows the toy geometric model, rather than a full retarded-light rendering.

Constants: c = 299,792.458 km/s; 1 AU = 149,597,870.7 km. The animation runs at 100 times real time; calculated measurements use the selected speed without that multiplier.

At c, one orbit takes approximately 52 minutes 15 seconds, horizon to horizon takes 26 minutes 8 seconds, and sunlight crosses 1 AU in about 8 minutes 19 seconds.

## GitHub Pages

In repository Settings > Pages, choose Deploy from a branch, select main and /(root), and save.

## Source

Recovered from the original Sun at Light Speed Site on November 3, 2026. The application HTML is unchanged. Site-specific hosting metadata and Git credentials are excluded.
