# Hexagonal 18 Cell Power Bank
Assembly guide and 3D printing models for my modular 18 cell power bank.

Licence: GPLv3

_This was entirely designed in [Blender](https://blender.org), with heavy use of the "Geometry Nodes" feature. See the [.blend file](Battery-Box-MK2_01.blend) which is the source of all the STL files. I supply this file "as is"._

![image](./images/banner-sml3.jpg)

0. ## Contents
	1. [Warnings and Disclaimers](#Warnings-and-Disclaimers)
	2. [Introduction](#Introduction)
	3. [Bill of Materials](#bill-of-materials)
	4. [Assembly](#Assembly)
		1. [Casing](#Casing)
		2. [Cell Cage](#cell-cage)
		3. [Lid Section](#lid-section)
		4. [Install lid module onto Case](#installing-lid-onto-case)
		5. [Handle Options](#handles)
		6. [Port Covers](#port-covers)
		7. [Decorative Base](#decorative-base)
	5. [Charging](#Charging)

0. ## Warnings and Disclaimers
	First and Foremost - **You are responsible for your own safety**. I am not liable for the outcomes if you follow this guide. 
	
	It is assumed that you have competency in (but not limited to) the following: handling Lithium batteries, electronics, soldering, spot welding, 3D printing, use of adhesives, etc.
	
	### Safety Advisories:
	* BATTERIES ARE ALWAYS LIVE!!!
		- You can't turn batteries off.
		- It is extremely easy to short circuit batteries and cause sparks.
		- Electrical shorts can do the following:
			+ Damage your tools
			+ Burn your skin
			+ Start fires
	* The nickel strips you will be spot welding with are sharp and it is too easy to cut yourself.  
		- If you have to remove a Nickel strip that has been spot welded, use tools rather than fingers, BUT BEWARE OF ELECTRICAL SHORTS!
	* When spot welding, wear safety glasses.
	* When soldering or using adhesives, have a well ventilated environment.

1. ## Introduction
	I'll keep this brief. The main use for this is to recharge RC vehicle batteries when you're out in the field, and because there was space, I threw in a bunch of USB outlets and a wireless charging pad.
	
	Did I need to make this? Not really, but I find the process incredibly therapeutic. I believe a lot of us in the FPV hobby get the same effect. You know what I'm talking about!
	
	I never intended to release plans for this project. However, it was gratifying to receive all the positive attention on the various Facebook groups I posted to. So much so, that various people have ended up contributing to tweaks of the design (I apologize for not keeping a list of all your names).
	
	So, here's a guide as a **THANK YOU** to everyone!
	
	If you're wondering what the capacity of this unit is - well that depends on the type of cells you use! It's built for 21700 cells because they can have higher capacity than 18650 (On a side note, I invite people to come and modify the design for 18650!). Anyway, in my build, I used 5Ah cells configured in 3S6P. When fully charged, that's 12.6V with 30Ah, which comes to **378Wh of energy**. Some people prefer to quote the nominal voltage, but I'm more interested in knowing how much energy I have when it's fully charged! Anyway, if you want the nominal stats, it's 10.5 V, multiplied by 30Ah, gives 315Wh. I'm not aware of any 21700 cells that are greater than 5Ah, so this is probably the highest capacity this model is going to get. Please let me know if any higher capacity 21700s hit the market!

1. ## Bill of Materials (BOM)
	To the best of my recollection, here's what you need to reproduce my build.

	* **18x 21700 Lithium Ion Batteries**.
		- I used `Bak N21700CG-50`. They are 5 Amp Hours each and rated for 10 Amp discharge. Use whatever you can procure, just make sure they're all identical!
	* **3D printing filament**.
		* That's up to you. I haven't calculated the total mass of material, but let's just say it's only a few hundred grams.
	* **Screws**:
		- 6x M3.5x75mm bolts
		- 5x M2x25mm bolts
		- 2x M2x10mm bolts
		- 2x M2 washers
		- 2x M2 nuts
	* **Adhesives**:
		- Cyanoacrylate (e.g., Gorilla Glue), used for places where the prints needs to be permanently bonded.
		- E6000. This stuff holds on very hard. It sets like rubber so can be peeled off if needed. Best of both worlds.
	* **Electronic Modules**:
		- Battery Management System (BMS)  
			+ There are a lot of options out there, and so you'll have to get something that suits your battery configuration. My build was 3S6P with cells rated for 10 Amps. I used a 40 Amp BMS which meant that the cells would never get too taxed.
			+ [BMS 3S 40A BMS board 11.1V 12.6V 18650 lithium battery protection board, drive drill 40A current](https://www.aliexpress.com/item/32956650573.html)  
			+ ![image](./images/02.jpg)
		- Wireless charging module (optional)
			+  [20W High Power 5V 13.5V Fast Charging Wireless Charger Transmitter Module Type-c USB + Coil Qi Universal For Phone Battery](https://www.aliexpress.com/item/1005002996173955.html)  
			+ ![image](./images/03.jpg)
		- Quickcharge / Apple Fast charge USB A Module (Qty 3)
			+  [5PCS USB DC-DC Buck Converter Charging Step Down Module Fast Quick Charger 6-32V 9V 12V 24V to 3V 5V 12V Circuit Board](https://www.aliexpress.com/item/32908913001.html)  
			+ ![image](./images/04.jpg)
		-  USB C Power Delivery Module (Qty 3)
			+  [Type-C 20W Quick Charging Module QC 3.0 PD3.0 5V 9V 12V Overvoltage/Over Temperature Protection For 18650 Battery Power Bank](https://www.aliexpress.com/item/1005003733377372.html?spm=a2g0o.order_list.0.0.54fb1802LUxs8j)  
			+ ![image](./images/05.jpg)
		- Battery Meter
			+ My configuration was 3S, so I got a 3S battery meter, and the lid is structured to match this part. If you go, say 6S, you'll have to figure out your own solution to the battery meter.
			+ [1S 2S 3S 4S Single 3.7V 18650 Lithium Battery Capacity Indicator Module Percent Power Level Tester LED display board](https://www.aliexpress.com/item/1005001962183752.html)
			+ ![image](./images/06.jpg)
		- USB Lithium Charging Module
			+ You can regard this as optional, but I liked the idea of being able *trickle charge* this from any old phone charger. 
			+ [Type C BMS 2S 3S 4S Charger 21700 18650 Polymer Li-Ion 7.4V 11.1V 14.8V to 8.4V 12.6V 16.8V 1A 2A 4A Boost Power Bank Charging](https://www.aliexpress.com/item/1005003680813897.html)
			+ ![image](./images/07.jpg)
	- Electrical connections
		+ 18 gauge wire for charging modules
		+ 16 gauge wire for main power buses
		+ Nickel Strip (thickness will depend on your spot welder)
		+ Any kind of 2 pin male-female connector pair (for the wireless pad)
		+ XT60E-M (male panel mount)
		+ XT60-F
		+ XT60-M
		+ JST-XH 4 pin, (2x male)
		+ JST-XH 4 pin female lead. (Assuming a 3S configuration)
		+ Self adhesive heat sinks (e.g. for a Raspberry Pi) for BMS cooling.
		+ [Mini Racewire](https://www.flyingtech.co.uk/cables-connectors/tbswhitenoisefpv-x-tbs-race-wire-pcb-full-mini-set-6#:~:text=Race%20Wire%20is%20the%20perfect,of%20the%20Race%20Wire%20board.) - optional but useful for connecting all the modules together in parallel.
		+ 30cm Velcro battery strap (This is an optional part for one of the handle mounts) 	
	- **Consumables**
		+ Variety of shrink tube
		+ Electrical Tape
		+ Solder and flux
		+ Bandages (*Just joking. No really, have bandages*)

1. ## Assembly
	1. ### Casing
		`Print:` [case-FINAL.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/case-FINAL.stl).
	
		This is the largest single piece. This is what everything else attaches to, so no other instructions needed!
		
		![image](./images/08.png)
	1. ### Cell Cage
		`Print:` [Cell-Holder-Plate.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Cell-Holder-Plate.stl), Qty 2.
		
		`Print:` [Cell-Holder-Strut.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Cell-Holder-Strut.stl), Qty 12.
		
		`Electronic parts: BMS and heat sinks.`
		
		`Other materials: glue, batteries, nickel strips, kapton tape, shrink tube, 16 gauge wire, 3S balance lead, XT60 (female) connector.`
		
		`Tools: Spot welder, rubber mallet (optional), soldering iron, scissors, wire snips, exacto knife or wire strippers.`
		
		1. First, print two copies of [Cell-Holder-Plate.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Cell-Holder-Plate.stl).   
		
		1. Then stand your batteries in one of the prints, and slot the second one around the top of the cells. Depending on the tolerances of your printer and the thickness of the shrink wrap on the batteries, a some gentle *percussive persuasion* may be needed (rubber mallet is good for this).  
		![image](./images/10.jpg)
		
		1. Print twelve copies of [Cell-Holder-Strut.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Cell-Holder-Strut.stl).
		
		1. Place the battery assembly on its side, ready to place the struts into the slots. Before placing each strut, add a **tiny** drop of cyanoacrylate (gorilla!) glue. Depending on your printer tolerances, the rubber mallet may be needed to get the struts all the way into their slots   
		![image](./images/11.jpg)
		
		1. Leave the assembly on some paper towel (or other disposable surface), and leave a few hours for the glue to set.
		
		1. #### Wiring
			`Print: ` [Strip-cover.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Strip-Cover.stl)
		
			`Requirements: 16awg wire, nickel strip, spot welder, soldering iron and solder, shrink tube.`
		
			1. This is where we start spot welding. I will assume you have experience of this. When I built my pack, I set my cells in a 3S6P configuration, but you may be using something else (6S3P, 1S18P), so my advice here as guidance.
			
			1. Because of the hexagonal shape, battery placement is more complicated than a simple grid layout. The main concern is to keep equal voltages together in the same area. Otherwise, when you connect them in parallel there will be many places where short circuits (i.e. sparks) could happen. See the graphic below  
			![image](./images/wiring.png)
			
			1. Once the batteries are connected with nickel strips, we need to add wires that will then be connected to the BMS. My solution was solder the ends of the wires to a nickel strip, cover the solder joint with shrink tube, then spot weld the exposed strip to the strips we have welded to the batteries.  
			![image](./images/12.jpg)
			
			1. Once they are connected to the batteries, cover in kapton tape to prevent accidental short circuits. It should then look like this:  
			![image](./images/14.jpg) ![image](./images/13.jpg)
			
			1. Finally, print two copies of [Strip-cover.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Strip-Cover.stl). This is a thin layer of plastic to provide some stronger protection to the top and bottom of the cell assembly. Affix it with either a non-permanent glue or some electrical tape.  
			![image](./images/15.jpg)
		
		1. #### Add BMS
			`Requirements: BMS, heat sinks (optional), non-permanent glue (e.g. E6000), XT60 (female) connector, 3S balance lead`
		
			1. Solder two 16awg wires to a female XT60 connector (roughly 3" to 4"), and add the heat sinks to the BMS FETS if you expect to be pulling high current.
			
			1. Tin the pads on the BMS, and solder the XT60 lead to the P+ and P- pads.![image](./images/16.jpg)
			
			1. Next, glue the BMS to the top PLA cover sheet, positioned as shown in the next image (position matters for how it will be installed into the case later). I recommend spreading E6000 around with a spatula!  
			![image](./images/17.jpg)
			
			1. Next, you'll need to solder all the wires to the BMS. Here you can trim the wires to the optimum length. Some BMS boards have their pads labeled with their corresponding voltage, some have "B0/B-", "B1" "B2", "B3/B+". Just connect them up in ascending voltage order.
			
			1. If you want to be able to use an external balance charger, you'll also need to solder the balance lead to these pads too. See the previous image for an example.
		
		1. #### Installing into Case 
			`Print:` [Holding Bracket v4.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Holding%20Bracket%20v4.stl).
			
			`Requirements: Holding Bracket v4.stl, case-FINAL.stl, 5x M2x25mm bolts/screws, screwdriver (preferably powered).`
			
			1. Slide the battery cage (*can we call it the **POWER CORE**, please?*) into the case (`case-FINAL.stl`). If your tolerances are right, there should be a little friction, but not so much that cannot be overcome by the weight of the batteries.
			
			1. Lay the holding bracket (`Holding Bracket v4.stl`) on top top of the battery cage, around the BMS, and line up with the internal screw holes in the casing.
			
			1. Screw in the M2 bolts. I recommend a powered screw driver or drill, because for the first time the screws will be tapping into the plastic.  
			![image](./images/18.jpg)
			
			1. Make sure the pressure is evenly distributed, and that the battery cage is fully immobilized. As ever, be careful not to over tighten.  
			![image](./images/19.jpg)
		
	1. ### Lid Section
		The lid of this pack was made to be interchangeable. So far, I only have one design, so there's nothing to interchange it with! I invite you to redesign and create your own lid with all the ports and electronics that you need for your projects. I designed all of this in Blender, rather than a CAD package, simply because it's what I use in my day job, so it was the quickest way to get what I needed.

		1. #### Lower Lid
			`Print:` [lower-lid-FINAL.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/lower-lid-FINAL.stl) **OR** [lower-lid-no-cut-outs.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/lower-lid-no-cut-outs.stl) (modify this model to your own specs)

			The 'no cut outs' STL is supplied so that you can remix the design to whatever set of ports and electronic modules you wish to use in your build. For example, the configuration presented here has a 3S battery configuration. However, if you go for 1S or 6S, you will need either no balance port, or a 6s balance port. You may also use different USB charging modules. It's your choice.

		1. #### Cabling
			`Tools: Wire cutters, soldering iron, solder, heat gun.`

			`Requirements:`
			* E6000 Glue
			* 16 gauge wire
			* 18 gauge wire
			* Shrink tube (various sizes)
			* JST-XH 4 pin (2x male)
			* XT60E-M (male panel mount)
			* XT60-M
			* 2 pin power connector, male and female pair (for wireless charging module, type of connector doesn't matter).
			* All the electronic modules you have chosen for your own particular build. The default (i.e. my original build) is as follows (see BOM above):
				* 3x USB A Quick Charge Modules
				* 3x USB C Power Delivery Modules
				* USB C 3S charging module
				* Battery Meter

			Begin by creating a power cable with the XT60-M connector with 16 gauge wire. This will be how the lid section connects to the battery pack in the case. Connect this power cable to the Mini Racewire. We are using the race wire as a power bus - if you have a better idea for how to connect one power cable to many outputs in parallel in the fairly restricted volume of the lid section, then go for it!

			In order for the race wire to distribute power to all of its solder pads, you must make sure to bridge the pads adjacent to where the power cable has been attached.

			Now create the balance port (if you are using one). Take the two JST-XH (4pin) sockets, and connect them with 18 gauge wire. You should use shrink tube to cover the pins. This 'Male to Male' cable will connect to the balance cable from the battery pack, and the other end will be fitted into the lower lid section.

			Now solder 16 gauge wire to the XT60E-M panel mount port.

			Next, place all the electronic modules into the lower lid (without glue), and measure out the lengths of wire you will need. Then solder each of the required lengths of 18 gauge wire to the electronic modules.

			Before soldering everything to the race wire, make sure you have shrink tube slotted over the race wire.


			See the images below for reference:
			
			![image](./images/20.jpg) ![image](./images/21.jpg)

			![image](./images/22.jpg) ![image](./images/23.jpg)


		1. #### Mid Lid Extension
			`Print:` [Lid-extender.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Lid-extender.stl) (scale height to your own needs)`

			I created this section because I underestimated how much space would be needed for all the cables. With your own set up, you may scale the height to whatever, or not even include it at all.

		1. #### Upper Lid
			`Print:` [Upper Lid (no cut-out).stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Upper%20Lid%20(no%20cut-out).stl)

			or

			`Print:` [Upper Lid (cut-out).stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Upper%20Lid%20(cut-out).stl) **ON TOP OF** [wireless-logo.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/wireless-logo.stl).

			`Requirements:`
			* Wireless charging module
			* 18 gauge wire
			* Wire cutters
			* Solder
			* Soldering iron
			* E6000 glue
			* Double sided tape
			* Kapton tape
			* The other part of the 2 pin power connector (see cabling requirements).

			This might be your first adventure into two-color 3D printing! To get the Wireless logo embedded into the lid as shown below, first print the wireless-logo.stl in one color. It should only be one layer height, i.e. 0.2mm.

			Next, without removing the wireless logo, load your second color into the printer, and start printing the version of the upper lid that has the wireless logo cutout. The printer will simply make the second print around the first print and they will fuse together.

			If you intend to use wireless charging, solder the 2 pin connector to its PCB, and then wrap the entire PCB in kapton tape. Next either use double sided tape or E6000 glue to fix the wireless charging coil into the circular receptacle in the upper lid. **Be sure to have the black ferrite pad facing inwards!**

			Finally, use double sided tape or glue to fix the PCB to the underside of the charging coil.

			![image](./images/24.jpg) ![image](./images/25.jpg)

			![image](./images/26.jpg) ![image](./images/27.jpg)

		1. #### Lid Assembly
			`Print:` [JST Glue in Support.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/JST%20Glue%20in%20Support.stl), [Meter-Holder.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Meter%20Holder.stl), [Meter-button-cover.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Meter-button-cover.stl)
			
			`Requirements:`
			* Lower Lid (4.3.1)
			* Cabling Harness (4.3.2)
			* Mid lid extension (4.3.3)
			* Upper Lid (4.3.4)
			* M2 Nuts, bolts and washers
			* E6000 glue
			* Cyanoacrylate (gorilla) glue
			* M3 long bolts
			* Rotary tool with a 3mm diameter drill bit.

			Start by milling out the screw holes in the three lid sections until the long M3 bolts can freely slot through them. (This makes screwing the entire lid section to the case much easier).

			Fit the battery meter into its 3d printed holder and slot the button cover over the brass button. The print may need some adjustments with either a cutting wheel, or soldering iron, to make the battery meter fit correctly.

			For each USB module in turn, apply some E6000, slot the module into its lower-lid slot, and hold with some pressure while the glue adheres.

			Apply Cyanoacrylate (gorilla) glue to the lower lid where the battery meter holder will go, and press the holder (with the meter installed) into place. Again, hold for a moment while the glue sets.

			Take the "JST Glue in Support.stl" that you just printed and use Cyanoacrylate glue to fix it to one end of the male-to-male JST cable you created earlier. Once glued together, then add some glue to the base of the 3D printed support, and slot it into place in the lower lid and hold while the glue sets.

			Take the M2 nuts and bolts and washers, and use them to screw the XT60E panel mount connector into the lower lid.

			Now place the mid-lid-extension on top of the lower lid section. You may omit the extension if your wiring harness is more compact than I made mine! You may even find that you need two extensions, or a height-scaled extension.

			Once the extension is over the lower section, plug the wireless charging module into the cable harness, via the 2 pin connector.

			Finally, place the upper-lid on top of the rest of the lid assembly. All the sections should fit flush to each other, without putting excessive pressure on the electronics inside. To hold this section together, loosely slot the long M3 bolt through all size holes.

			Please see the photos below for reference.

			![image](./images/28.jpg) ![image](./images/29.jpg) ![image](./images/30.jpg)
			![image](./images/31.jpg) ![image](./images/32.jpg)


	1. ### Installing lid onto case
		`Requirements: Power drill with M3 Hex bit, or a M3 Allen key and lots of patience and a strong arm.`

		Well done, you've made it this far!

		Start by connecting the XT60 and JST balance leads of both the lid section and the power core (there, I named it!). Next place the lid section over the case, and slide it down the bolts so that it is flush to the case.

		Now, take your power drill (or Allen key if you're a masochist), and drill each bolt down half way. Make sure everything is lining up still, and drill them down the rest of the way.

		**Warning!!!** If bolts are drilled at high speed all at one go, lots of heat will be generated through friction. This is okay but not ideal. It's best to take things slow and steady!

		![image](./images/41.jpg) ![image](./images/42.jpg)



	1. ### Handles
		If you would like to fit a carrying handle we have two options. The heavy duty handle creates a large handle that makes the pack easy to pick up and go. The 'flexible' handle gives you two strong loops through which to thread a Velcro strap, or rope, or anything you want. The 'flexible' option has the advantage of leaving room up top to place a phone for wireless charging!

		In each case, the handles are fitted on top of the lid section and held in place by the existing M3 long bolts.

		1. #### Heavy Duty
			`Print:` [HeavyDutyHandle.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/HeavyDutyHandle.stl)

			![image](./images/33.jpg) ![image](./images/34.jpg)

		1. #### Flexible Handle Mounts
			`Print:` 2x [fleximount.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/fleximount.stl)

			![image](./images/35.jpg) ![image](./images/36.jpg)
			![image](./images/banner-sml2.jpg)
		

	1. ### Port Covers
		`Print:` [xt60-cover.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/xt60-cover.stl) & [Balance-Cover.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/Balance-Cover.stl)

		These are optional covers to protect the live contacts from being short circuited.

		![image](./images/37.jpg) ![image](./images/38.jpg)

	1. ### Decorative Base
		`Print:` [shoe-batt-orange.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/shoe-batt-orange.stl) **ON TOP OF** [shoe-batt-black.stl](https://github.com/davidgilson/Hexagonal-Power-Bank/blob/main/STL/shoe-batt-black.stl)
		
		This is just a *for fun* Addition. Use the same two color approach as described for the wireless logo on the lid. Once printed, use gorilla glue to fix this onto the base of the power bank. There's no functional reason to do this, it's just an easter egg, and might hid any ugly first layer on your case.
	
		![image](./images/39.jpg) ![image](./images/40.jpg)

1. ## Charging
	![image](./images/charging-banner.jpg)

	This is the subject that most concerns me about letting this design out into the wild. You really need to be familiar with lithium battery charging, **AND** the specifications of the batteries you have selected.  Do your due diligence and proceed with caution - success or failure is on your shoulders, not mine. Note that 'failure' will involve fire and destruction of property and potentially life. So please be careful, and ***NEVER CHARGE WHILE UNATTENDED.***

	As a rule of thumb, always charge Lithium Ion cells at a **0.5 C rate**, no faster. In my example, I used 5Ah cells, in 3S6P configuration. This meant I had a total capacity of `6*5Ah=30Ah` (at 3S or 12.6V). Therefore, `0.5C * 30Ah = 15 Amps maximum charging rate`.

	_On last thing..._
	
	Because the XT60 DC In/Out socket is a male socket, you will need to create a small extension lead to connect to a standard LiPo charger. Use 16 AWG cable to connect two female XT60 connectors together. Additionally, you will need a balance lead. For example, in the 3S configuration I used, you'd need a cable with a female JST-XH 4 pin connector at each end (i.e. a 3S balance lead). See the image above!
