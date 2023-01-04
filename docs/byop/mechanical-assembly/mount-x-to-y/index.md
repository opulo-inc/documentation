---
title: "Mounting the X Gantry to the Y Gantry"
linkTitle: "Mounting the X Gantry to the Y Gantry"
weight: 50
description: >
  Attaching the X gantry to the Y gantry
---

Now that we have both gantries assembled, it's time to put them together.

## X Gantry Tensioner Bars

| Qty | Part                            |
|----:|---------------------------------|
|   2 | V-slot roller wheel             |
|   2 | FDM-0043 (X Gantry Tension Bar) |
|   2 | M5x40 machine screw             |
|   2 | M5 Hex Nut                      |
|   4 | M3x30 machine screw             |

1. Fit the X gantry on top of the Y gantry rail. Make sure the X motor is on the left side with the front of the X gantry facing you.
  {{< alert color="warning" title="Note" >}}
  You'll find that it's hard to fit the X gantry onto the rail. This is because of a few protrusions on the back plate that hold the belt at the right distance. Loosening the M5x40mm bolts holding the two halves of the X gantry together will help it slot onto the rail.
  {{< /alert >}}
  ![](images/Mounting-X-To-Y-Step-1.png" alt="Proper orientation of the newly attached X-axis gantry" >}}

2. Prepare two V-slot rollers. You may need to align one or both of the interior washers inside the rollers, as they can shift in shipping and block the hole for the screw. Simply push the washers back into place with a screwdriver tip.

3. With the top roller bolts still loose, slide the two {{<tooltip "X Gantry Tension Bars" "FDM-0043">}} onto the bottom of the {{<tooltip "X Gantry prints" "FDM-0012 and FDM-0011">}}. Slide two rollers in between them, ensuring that the holes in them line up with the holes in the {{<tooltip "X Gantry Tension Bars" "FDM-0043">}}.
  ![](images/Mounting-X-To-Y-Step-3.png" alt="Sliding on the X Gantry Tensioner Bars" >}}
  ![](images/Mounting-X-To-Y-Step-3-2.png" alt="Slotting two V-Slot Rollers in-between the Tensioner Bars" >}}

4. Now we can secure the stack in place using two M5x40mm bolts. Pass them through the holes, and loosely tighten them into two M5 nuts in the slots on the {{<tooltip "X Gantry Back" "FDM-0012">}}. Don't tighten all the way yet; we still have some adjustment to do first.
  ![](images/Mounting-X-To-Y-Step-4.png" alt="Securing the tensioner bars with M5 screws" >}}
  ![](images/Mounting-X-To-Y-Step-4-4.png" alt="Loosely threading the M5 screws into M5 nuts to hold the Tensioner Bars on." >}}
  ![](images/Mounting-X-To-Y-Step-4-3.png" alt="Cutaway view of the new M5 screws going through the tensioner bars and V-Slot rollers and ending in the M5 nuts." >}}

5. Tighten the **top** roller bolts now that everything is in its place.
  ![](images/Mounting-X-To-Y-Step-5.png" alt="Tightening the two top roller sandwiches" >}}

6. Now we add tension screws. These are what hold the {{<tooltip "X Gantry Tension Bars" "FDM-0043">}} in the correct position to have proper tension along the rail. Take four M3x30mm screws and pass them through the holes in the {{<tooltip "X Gantry Tension Bars" "FDM-0043">}}, and thread into the M3 nuts inserted into the {{<tooltip "X Gantry prints" "FDM-0012 and FDM-0011">}}, as shown below. Make sure each screw is tightened the same amount, and that the X gantry can still move freely, but doesn't have any wiggle on the rail.
  ![](images/Mounting-X-To-Y-Step-6.png" alt="Installing four M3 screws to tension the X Tension Bars" >}}
  ![](images/Mounting-X-To-Y-Step-6-2.png" alt="Installing four M3 screws to tension the X Tension Bars side view" >}}

7. Tighten the M5x40mm bolts that run through the bottom set of rollers (installed in the previously) so that their position is locked.
  ![](images/Mounting-X-To-Y-Step-4.png" alt="Securing the tensioner bars with M5 screws" >}}

## Camera and Ring Light

| Qty | Part                        |
|----:|-----------------------------|
|   1 | USB Camera (Top)            |
|   1 | FDM-0015 (Top Light Mount)  |
|   1 | FDM-0014 (Top Camera Mount) |
|   1 | Top Ring Light PCB          |
|   4 | M2.5x20 machine screw       |
|   2 | M3x14 machine screw         |
|   1 | Super Lube                  |

{{< alert color="info" title="Note" >}}
There's a piece of black electrical tape on the back of the camera PCB. Don't remove it; it is there to help isolate the camera sensor from light shining through vias in the PCB.
{{< /alert >}}

8. Before mounting the camera, you'll need to make sure you can rotate the lens and adjust the camera's focus. First carefully remove the set screw on the side of the lens assembly that is holding the lens in place. Next, unscrew the lens from the camera. You might need a light grip with pliers (preferably with soft grips) to get it to turn. With the lens removed, use a cotton swab to apply a **very small** amount of Super Lube to the lens threads. Be careful not to get any of the lubricant inside or on the lens. Wipe off any excess with a cotton swab or microfiber cloth. If necessary, you can clean the lens itself using a microfiber cloth. Screw the lens back into the camera and work the lubricant into the threads. Save the lubricant as you'll use it again later. Finally, add the set screw back to the side of the lens assembly. Tighten the set screw just enough to keep the lens in place but not so much that it prevents you from adjusting the lens with a little force, as you'll need to adjust the lens after the camera is mounted.

9. Place the ring light facing downwards into the {{<tooltip "Top Light Mount" "FDM-0015">}}. The LEDs will shine down, and the white plastic wire connector will face upwards.
  ![](images/IMG_0771.JPG" alt="Installing the Top Light into the Top Light Mount" >}}
  ![](images/IMG_0772.JPG" alt="Installing the Top Light into the Top Light Mount side view" >}}

10. Place the {{<tooltip "Top Camera Mount" "FDM-0014">}} on top of the {{<tooltip "Top Light Mount" "FDM-0015">}} ensuring that the tab from the {{<tooltip "Top Light Mount" "FDM-0015">}} fits onto the side opposite the arms on the {{<tooltip "Top Camera Mount" "FDM-0014">}}. These two prints will pinch the top ring light in place.
  ![](images/Mounting-X-To-Y-Step-9-ALT.png" alt="Attaching the Top Light Mount to the Top Camera Mount" >}}

11. Install the Top Camera into the {{<tooltip "Top Camera Mount" "FDM-0014">}}. Make sure the connector on the back side of the camera is between the two arms of the {{<tooltip "Top Camera Mount" "FDM-0014">}}.
  ![](images/Mounting-X-To-Y-Step-11.png" alt="Inserting the Top Camera into the Top Camera Mount" >}}
  ![](images/Mounting-X-To-Y-Step-11-2-MANUAL.png" alt="Correct location of the wire connector for the Top Camera" >}}

12. Secure the whole stack in place with four M2.5x20mm screws in the outer four holes (not the ones with a metal circle around them). Tighten them down so that all parts are tightly held together, but don't over-torque; these screws are threading into the plastic of the {{<tooltip "Top Light Mount" "FDM-0015">}}.
  ![](images/Mounting-X-To-Y-Step-12.png" alt="Screwing in the Top Camera" >}}

13. Use two M3x14mm screws to mount the Top Camera and Light subassembly onto the back of the {{<tooltip "X Gantry Back" "FDM-0012">}}.
  ![](images/Mounting-X-To-Y-Step-13.png" alt="Attaching the Top Camera assembly" >}}

## Next steps

Continue to [mounting the Y Gantry to the Frame]({{< relref "mount-y-to-frame" >}}).
