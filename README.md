# home-assistant-ikohs-fan-card
A custom card to integrate ikohs fan into the Home Assistant lovelace UI. 

## Inspiration
This custom card is based on the code from the [xiaomi fan card](https://github.com/OliverHi/home-assistant-xiaomi-fan-card).
It has been tested with an ikohs windcalm DC only using both localtuya & the official Tuya integration. 

## Installation
You can manually install this card by adding the ikohs-fan-card.js to your `<config>/www/` folder.

This card can also be installed via the [HACS]() community store. Install HACS and click the button on the top right. Select "Custom repositories" and add the URL `(https://github.com/Damazinho/home-assistant-ikohs-fan-card)`. Now you should be able to find and install this card as `home-assistant-ikohs-fan-card` via HACS.

## Usage
The card has to be added via the raw configuration editor as yaml. You need to provide the entity id itself and the list of speed modes available in your fan version.

```
- type: custom:ikohs-fan-card
  entity: fan.ikohs_fan_windcalm
  speed_modes:
    - 1
    - 2
    - 3
    - 4
    - 5
    - 6

```

![plafondventilator](https://user-images.githubusercontent.com/70435713/223839999-18330173-dc6f-49b0-9324-250b349b875f.PNG)

You can also add the same optional configurations as in the linked xiaomi vacuum card. I personally use the image config to add a background image to the card.
```
- type: 'custom:ikohs-fan-card'
  entity: fan.ikohs_fan_windcalm
  image: /local/img/ikohs_fan.jpg
```

This image has to be saved in the `<config>/www/img` folder of your Home Assistant installation.

The card shows the power state (on/off), the direction of the rotation (forward or backward) and the fan speed (in percentage).
The buttons can be used to power the fan on or off (first button), to change the direction (second button), or set the fan speed levels.

## TODO

- Change the speed in the card to show the speed list and not the percentage.

## Disclaimer
This project is not affiliated, associated, authorized, endorsed by, or in any way officially connected with the ikohs nor with Home Assistant. The integration is delivered as-is and any feedback is welcome. 

