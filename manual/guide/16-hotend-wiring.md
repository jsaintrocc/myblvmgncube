# My BLV MGN Cube - Step 16 Hotend Wiring

## [Step 16 BoM Spreadsheet Link](https://docs.google.com/spreadsheets/d/e/2PACX-1vTVx7BvB3V7CozF2l4eWkNntWrHSjOawmrsi_bRSVxQLIGVlfZTYEGp8a6fHpENV6hV2cn9PrDLHHl0/pubhtml?gid=1647615114&single=true)

### Assembly
1. Check your fan connectors for the correct polarity. -/Black and +/Red should be in the JST-XH connector as pictured. My blower fan was wired backwards. It's easy to remove the female pins and swap them in the connector if you need to. Aliexpress cheap but...

    ![](img/16-FanJSTPinout.JPG)\
    *fig 16.1*

2. Make extension wires for the both fans using 1m lengths of the 22AWG silicone wire and 2pin male connectors.
    1. Cut pieces of heat shrink tubing for each wire and slide over the wires. Use a larger piece of heat shrink tubing to cover all the wires. *Nothing is more annoying than realizing you forgot to put the heat shrink tubing on a wire after you're done attaching the connectors*

        ![](img/16-HeatShrinkPrep.JPG)\
        *fig 16.2*

    2. Strip the ends of the wires. Only strip a little because we are going to crimp the ends with female JST-XH connectors.

        ![](img/16-StripWires.JPG)\
        *fig 16.3*

    3. Attach female JST-XH crimps to the ends of the wires using the crimper. *The IWS-2820M worked much better than the fancy ratcheting ones for me. It's not fast but I got much better crimps.*

        ![](img/16-CrimpWires.JPG)\
        *fig 16.4*

    4. Setup the male connector in your helping hands and use the female crimps to attach to the back the connector. This will make soldering them MUCH easier. Also make sure to attach something to the connector to help dissipate the heat when you solder it (I used a spare fan). The connectors are really small and you're likely to melt it if you don't dissipate the heat somehow.

        ![](img/16-PrepForSolder.JPG)\
        *fig 16.5*

    5. Solder the female connectors to make it permanent. You shouldn't need much. Be quick to avoid melting the connector.

        ![](img/16-SolderMale.JPG)\
        *fig 16.6*

    6. Slide the heat shrink tubing over each connection and use the torch to shrink it. I wave the torch back and fourth to keep the heat even and to avoid melting/burning things.

        ![](img/16-SmallHeatShrink.JPG)\
        *fig 16.7*

        ![](img/16-BigHeatShrink.JPG)\
        *fig 16.8*

3. Make an extension wire for the limit switch using 1m lengths of the 22AWG silicone wire and a 3pin female connector. Preferably green for signal and black for common.

    ![](img/16-FemaleSwConnector.JPG)\
    *fig 16.9*

4. Test the fans for proper operation.
    1. Temporarily wire up the power supply. **CAUTION: You're messing with mains power here and it can kill you. Use your own common sense here and consult a professional if you are unsure on how to do this**

        ![](img/16-PStestHookup.JPG)\
        *fig 16.10*

    2. Select the correct mains voltage on the power supply (Red Switch on Side)

        ![](img/16-SelectMainsVoltage.JPG)\
        *fig 16.11*

    3. Connect up the fans and power on the supply to check that they are working correctly. The hotend cooling fan should be sucking in air through the front grill and the part cooling fan should be blowing air around the nozzle.

        ![](img/16-FanCheck.JPG)\
        *fig 16.12*

5. Test hotend compents and wires.
    1. Test the X-axis limit switch using the multimeter contunity tester. The switch should be wired as normally closed. If the switch wiring breaks or is disconnected it will automatically trigger the switch. Here you see the switch is depressed and my multimeter has registered the circuit as open.

        ![](img/16-XLimitSWTest.JPG)\
        *fig 16.13*

    2. Test the hotend heater cartridge using the multimeter set to read resistance. You're really just looking for a finite resistance, probably 12-13 Ohms. If you are interested in the math V*V/R=W so in my case 24V*24V/12.8Ohms=45W.

        ![](img/16-HeaterTest.JPG)\
        *fig 16.14*

    3. Test the hotend thermistor. Standard thermistors, like mine, are in the 100K Ohm range. This math is non-trivial so be happy with something finite.

        ![](img/16-ThermistorTest.JPG)\
        *fig 16.15*