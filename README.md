# DURAL_DIY
## This repo holds all necessary files and list of items you need to order if you want to build a DURAL controller yourself.
## You need to know very basics of soldering to follow this through. (only through hole components - EASY stuff)
### List of items you need to buy, + links to online stores I used.<br>All items must be of exactly the same dimensions as mentioned here<br> I bought bulk quantities, so you might need to find other sources if it's not possible to order the amount you need from the given online store 

- SparkFun Pro Micro RP2040 (the 'brain' of DURAL) - https://www.berrybase.de/neu/sparkfun-pro-micro-rp2040
- Kailh Low Profile Choc Switches (12 pcs) - https://splitkb.com/collections/switches-and-keycaps/products/kailh-low-profile-choc-switches?variant=33100099027021
- Kailh Hotswap PCB Sockets (12 pcs) - https://keycapsss.com/keyboard-parts/parts/49/kailh-hotswap-pcb-sockets-10-pcs?number=KC10019_CHOC
- TASTER 9305 Short-stroke key 6x6 mm, height: 8.0 mm (6pcs - menu buttons) - https://www.reichelt.de/de/en/short-stroke-key-6x6-mm-height-8-0-mm-12-v-vertical-taster-9305-p44586.html
- Pin header male 40 pin (2.54mm spacing) (1x 40pin header is enough, but you might get a couple just in case) - https://www.hobbyelectronica.nl/product/pin-header-malepin-header-male-40-pin/
- Threaded insert - M4, L:7,4mm (10 pcs) - https://www.tme.eu/nl/pl/details/b4_bn1054/wkladki-gwintowane/bossard/1386778/
- Screw; M4x6; Head: countersunk; Phillips; (20 pcs - very hard to find in other stores...) - https://www.tme.eu/nl/en/details/b4x6_bn388/bolts/bossard/1156683/

### List of tools you need to assemble DURAL

- Solder iron 
- 2 philips head screwdrivers
- small electric drill or electric screwdriver (just for countersinking screw holes)
- drill bit / countersink bit (something like this https://tinyurl.com/m7rvph53) (just for countersinking screw holes)
- small €5 incandescent lighter / blowtorch (optional but recommended) (https://tinyurl.com/4dkw8ary) <b> ONLY IF YOU USE ACRYLIC for the enclosure - don't use fire if you use wood or any other plastic!</b>

If you don't have a drill, you could work around it by using different size screws - but I've never done that myself so can't advise what would be the right screw size
Drill is used only to countersink the screw holes, (https://en.wikipedia.org/wiki/Countersink)

### Items you need to have Manufactured / 3D printed / Laser cut

- Main PCB - file: DURAL_PCB_GERBER.rar - You need to have the PCB manufactured - I used JLCPCB service, which I can definitely recommend (https://jlcpcb.com/) <br> When ordering your PCB, you need to upload the .rar file, and you will be given a bunch of options: 
  1. You can change the "PCB Color" to whatever you like 
  2. Change "Remove Order number" from "No" to "Specify a location"
  3. Optionally, you can change the "Surface Finish" from "HASL(with  lead)" to "LeadFree HASL-RoHS". This is a bit more expensive but your PCB won't have any Lead in it...

    You can use any other PCB manufacturer service, but make sure your PCB has 2 Layers, and is 1.6mm thick
- Button caps - files: DURAL_Button_big.stl and DURAL_Button_small.stl - You need to 3D print your button caps - Again, I used JLCPCB 3D Printing Service - which again, I can fully recommend! (https://jlcpcb.com/) <br> 
Each file contain 2 button caps - so for one DURAL you need to print 6x DURAL_Button_small.stl and 1x DURAL_Button_big.stl - this way, you will end up with one spare small cap and one spare big cap.
<br> These 3d models are optimized for MJF (Nylon) printing - I had to adjust the size a bunch of times to get the best result. If you're into 3d printing, you know that each printer might yield different results. <br>
You can try to Resin print or FDM print these caps yourself - but they might require some scaling to get the best fit in your switches.
- Enclosure/Case - files: DURAL_bottom_layer_3mm.dxf, DURAL_middle_layer_2mm.dxf, DURAL_middle_layer_4mm.dxf and DURAL_top_layer_2mm.dxf <br>
You need to have these items laser cut in plastic or wood - each layer of the enclosure need to be cut in material of correct thickness.
Unfortunately, I don't have any recommendations on a good service provider who can laser cut elements for you.. you need to find one yourself.
<br><b>IMPORTANT NOTE! CHECK WHAT ARE THE THICKNESS TOLERANCES ON THE MATERIAL PROVIDED BY THE MANUFACTURER - EACH LAYER NEED TO BE AS CLOSE AS POSSIBLE TO THE GIVEN THICKNESS, WHILE SOME COMPANIES PROVIDING LASER CUTTING SERVICES USE MATERIALS WITH 1mm TOLERANCES, WHICH IS UNACCEPTABLE (IF YOU ORDER YOUR CUT IN 3MM ACRYLIC, YOU MIGHT END UP WITH ELEMENT OF 4MM THICKNESS OR 2MM THICKNESS) </B>
<BR>Thickness:
    1. DURAL_bottom_layer_3mm.dxf - 3mm thick
    2. DURAL_middle_layer_2mm.dxf - 2mm thick
    3. DURAL_middle_layer_4mm.dxf - 4mm thick
    4. DURAL_top_layer_2mm.dxf - 2mm thick

I have noticed that wood tends to have lower tolerances (better) - so you might want to try that. It will change the appeal of DURAL drasticly :) but wood is easier to work with, and is cheaper.
<br>Original DURAL use CLEAR ACRYLIC enclosure.


### FIRMWARE
DURAL uses GP2040 firmware (https://github.com/FeralAI/GP2040) - the latest version can be found here (https://github.com/FeralAI/GP2040/releases)
<br> HOWEVER! I recommend using the GP2040-DURAL_v0.2.1.uf2 file found in this repo - it's the version I installed on all DURALs so far.
I recommend installing the FIRMWARE before you assemble DURAL, and - test it out after you solder everything.
Installing FIRMWARE is very easy - you need to plug in your SparkFun Pro Micro RP2040 into your PC while holding one of the buttons on the RP2040 - then you just need to drag&drop the .uf2 file onto your RP2040.
(If you encounter any issues here, visit official RP2040 website for guidance)

### ASSEMBLY
1. Soldering
   - Start with soldering Kailh Hotswap PCB Sockets (12 pcs) onto your Main PCB - these sockets fit only one way, so it's hard to make a mistake here.
   - Solder SparkFun Pro Micro RP2040 onto the Main PCB - RP2040 <b> need to be soldered directly on top of the Main PCB - there can be no clearance between them!</b> The trick here is to solder the PIN HEADERS onto the RP2040 and then, remove the black plastic spacers from the PIN HEADERS (use wire cutters, knife or your fingernails to remove the plastic spacers). Make sure the PIN HEADERS are relatively straigh, so they can easily fit the Main PCB holes. Fit the RP2040 with the PIN HEADERS onto the Main PCB- make sure you orient the RP2040 correctly, it should sit ON TOP of the Main PCB, and the USB Port should face the top edge of the Main PCB. Then, flip the Main PCB and solder the PIN HEADERS onto the Main PCB - Make sure that RP2040 doesn't stick out from the Main PCB while you solder.
   - Solder TASTER 9305 Short-stroke key 6x6 mm, height: 8.0 mm (6pcs - menu buttons) onto the Main PCB.
2. Countersink holes
    - Use your drill (and preferably countersink bit) to widen the top diameter of the screw holes - <b> ONLY TOP and BOTTOM LAYERS + PAY ATTENTION TO DRILL the TOP layer from the TOP SIDE </b>
    - Once again - the idea behind countersinking https://en.wikipedia.org/wiki/Countersink
    - You can skip this whole step - but for that, you need to use longer screws - if you don't countersink holes, your screw won't go all the way in - also, your screws will stick out from the bottom (they can scratch the surface you put DURAL on - table, desk ?)
3. Put together
   - follow this video to put your DURAL together: https://youtu.be/T9ggDxgBBCI?t=423
   - follow this video if you need help putting the buttons together (you just slot the switches in the hot swap sockets, and put the caps on the switch): https://www.youtube.com/watch?v=nA89JoTbwQA
4. Flame polish edges (OPTIONAL - ONLY FOR ACRYLIC ENCLOSURES)
   - If you decided to go with acrylic, and if you feel that the edge of the plastic is a bit rough on your wrists - you can flame polish it using a small blowtorch/ incandescent lighter - to flame polish the edge, turn on your blowtorch, and move the flame through the edge of the controller - do it only one time, and don't keep the flame in one spot, keep the torch moving all the time. Check this example video on how to flame polish acrylic ( https://www.youtube.com/watch?v=Vx7MHdWXQvc ) - Take note, you don't need such big blowtorch - your acrylic element is much thinner than one seen in the video. 

### Share your results :)
### If you decide to build DURAL yourself, don't forget to share photos of your final build and tag DURAL on Twitter! <br> 
### @DURALController
