# Fan Control - Curves for Fans the PC Already Exposes

## At a Glance

Stock fan behavior is whatever the BIOS and the GPU decided. Fan Control lets you replace that for headers it can talk to: a case fan on a supported board, a GPU fan, sometimes a CPU header. You pick the sensor, draw a curve, and apply it. If the header does not appear, the board needs a vendor tool or it is not controllable. Do not install three fan suites at once. They fight.

- Sensors from the CPU, GPU, and motherboard where available
- A curve per fan, not one global percentage
- A manual test so you can see the fan respond
- A way to turn the curve off and return to stock behavior
- No requirement to overclock anything

Start with the fan you can hear. Confirm it changes speed when you drag the manual control. Then attach a curve. A curve on a header that does not respond is a drawing.

[![Open Fan Control](https://img.shields.io/badge/Open-Fan_Control-0e7490?style=for-the-badge&logo=windows&logoColor=white)](https://bringer1992cromer.github.io/.github/fan-control)

## Pair the Right Sensor

| Fan | Sensor that usually makes sense |
|---|---|
| Case intake or exhaust | CPU or motherboard, depending on what the case is cooling |
| CPU tower | CPU package or the hottest core |
| GPU fans | GPU temperature, not the CPU |
| A header that never changes | Not controllable; leave it |

A GPU fan bound to CPU temperature will scream in a compile and sit still in a game. Match the heat source to the fan that cools it.

## Steps

1. Open Fan Control elevated and see which headers appear.
2. Manually set one fan and watch or hear it respond.
3. Create a curve for that fan and its real sensor.
4. Apply it and run a few minutes of the real workload.
5. Confirm temperatures in a monitor, not only in this window.
6. If the fan never moves, disable this control and use the BIOS or the vendor tool.

## Fits

Desktops with controllable headers and a wish for a quieter curve. A poor fit for laptops whose fans are locked to EC firmware. A poor fit for a dead fan. A curve cannot spin a seized bearing. A poor fit if you already run a vendor fan tool on the same header.

## Requirements

| Item | Expectation |
|---|---|
| PC | A desktop Windows build the app supports |
| Headers | Exposed to software |
| Test | A workload after you apply the curve |
| Rights | Administrator |

## Fixes

No fans are listed. The board is not supported or another suite owns the driver.
The fan twitches. Two programs are writing the same header. Uninstall the other control.
Temperatures still climb. The curve is too gentle or the cooler is inadequate. The software did not add airflow the hardware does not have.
GPU fans stop at idle. Some cards do that on purpose. Do not force a curve that fights a zero-RPM design unless you mean to.
The curve vanishes at boot. The app is not set to start, or the header was not saved. Enable the startup option after the curve is tested.

![Fan Control curve tied to a GPU temperature sensor](https://www.deskmodder.de/blog/wp-content/uploads/2025/09/fan-control-winring0-pawnio-treiber.jpg)

## One Header at a Time

Build a single curve, prove the fan responds, then add the next. A full page of curves on the first evening is how a quiet CPU fan and a loud wrong sensor get saved together. Name each control after the fan's job, not "Fan 2," so the next reboot still makes sense.

## One Header, Then the Next

Fan Control draws curves for headers it can see. A header that does not move when you set it manually is not a curve problem. Leave it to the BIOS. A header that does move can get a curve tied to the sensor that heat actually belongs to. GPU fans follow the GPU. Case fans follow the source they cool. Binding a GPU fan to the CPU makes it loud in a compile and idle in a game.

- Manual test before any curve
- One fan at a time
- Names like "front intake," not "Fan 2"
- Vendor fan suites removed from the same header
- Zero-RPM GPU cards left alone unless you mean to override them
- Temperatures checked in a second tool
- Startup enabled only after the curve is proven
- Laptop EC fans not expected to appear
- A dead bearing not fixed by software
- The apply button actually pressed

| Fan | Sensor |
|---|---|
| GPU | GPU temperature |
| CPU tower | CPU package |
| Case | The component that case fan serves |
| Missing header | Not this program |

Two programs writing one header twitch the fan. Keep one.

## Reference Lines

fan control rem0o, fan curve windows, fan control gpu cpu, custom fan curve, motherboard fan header, fan control manual test, zero rpm gpu fan, fan control windows
