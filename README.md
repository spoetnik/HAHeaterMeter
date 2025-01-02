# HeaterMeter smoker controller package for Home Assistant
HeaterMeter smoker controller package for HA.

## Whats this
This is a Home Assistant package for managing your Heatermeter smoker comtroller. It let's you set the Pit Target Temperature (Setpoint) and the high- and lowtemperature alarms for the 3 probes.

## Installation
1) Copy the ```packages\heatermeter``` folder to your Home Assistant configuration folder.
2) Add the following to your Home Assistant configuration (configuration.yaml).
```
homeassistant:
  packages: !include_dir_named packages
```
3) Edit your Home Assistant dashboard, and add a new View to it. Copy the contents of the 'lovelace-ui.yaml' in the new view by choosing the option 'Edit in YAML'.
4) Add the hostname, or IP-address of your heatermeter in the configuration card of the new view.
5) Add API-key your heatermeter in the configuration card of the new view.
6) Restrt your Home Assistant

## Next steps
Use the dashboard to change the setpoint of your heatermeter

Change the alarms for the Low and High temperatures for the different food probes
The package exposes the following sensors:
```
sensor.heater_meter_pit_temperature
sensor.heater_meter_probe_1_temperature
sensor.heater_meter_probe_2_temperature
sensor.heater_meter_probe_3_temperature

sensor.heater_meter_pit_high
sensor.heater_meter_pit_low
sensor.heater_meter_probe_1_high
sensor.heater_meter_probe_1_low
sensor.heater_meter_probe_2_high
sensor.heater_meter_probe_2_low
sensor.heater_meter_probe_3_high
sensor.heater_meter_probe_3_low

sensor.heater_meter_alarm
sensor.heater_meter_fan
sensor.heater_meter_lid
sensor.heater_meter_setpoint
```

You can build your own automations with these sensors. Get a push notification when an alarm triggers. Or let your homespeaker notify you when the Cook is done.