Cold White + Warm White Light
=============================

.. seo::
    :description: Instructions for setting up Cold White + Warm White lights.
    :image: brightness-medium.png

The ``cwww`` light platform creates an Cold-White+Warm-White
light from 2 :ref:`float output components <output>` (one for each channel). The two
channels will be mixed using the color temperature configuration options.

.. code-block:: yaml

    # Example configuration entry
    light:
      - platform: cwww
        name: "Livingroom Lights"
        cold_white: output_component1
        warm_white: output_component2
        cold_white_color_temperature: 6536 K
        warm_white_color_temperature: 2000 K

Configuration variables:
------------------------

- **name** (**Required**, string): The name of the light.
- **cold_white** (**Required**, :ref:`config-id`): The id of the float :ref:`output` to use for the cold white channel.
- **warm_white** (**Required**, :ref:`config-id`): The id of the float :ref:`output` to use for the warm white channel.
- **cold_white_color_temperature** (**Required**, float): The color temperate (in `mireds <https://en.wikipedia.org/wiki/Mired>`__ or Kelvin)
  of the cold white channel.
- **warm_white_color_temperature** (**Required**, float): The color temperate (in `mireds <https://en.wikipedia.org/wiki/Mired>`__ or Kelvin)
  of the warm white channel.
- **effects** (*Optional*, list): A list of :ref:`light effects <light-effects>` to use for this light.
- **id** (*Optional*, :ref:`config-id`): Manually specify the ID used for code generation.
- All other options from :ref:`Light <config-light>`.

See Also
--------

- :doc:`/components/output/index`
- :doc:`/components/light/index`
- :doc:`/components/light/rgb`
- :doc:`/components/light/rgbw`
- :doc:`/components/power_supply`
- :doc:`/components/output/ledc`
- :doc:`/components/output/esp8266_pwm`
- :doc:`/components/output/pca9685`
- :apiref:`cwww/cww_light_output.h`
- :ghedit:`Edit`
