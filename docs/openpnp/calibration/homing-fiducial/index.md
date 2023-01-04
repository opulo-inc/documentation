# Homing Fiducial

Now that fisheye calibration is complete, we can set up the datum board. The datum board is a reference point for everything else you'll do with the machine. The center dot of the datum board will be the most important calibration point for the machine. It'll be used to fine-tune the LumenPnP's XY position after homing to account for any errors in the limit switches.

!!! danger "If Your Machine Is v2"
    If you are setting up a v2 LumenPnP kit, your datum board is not yet mounted to the Staging Plate.

    Use four M3x16mm screws and four M3 nuts to secure the datum board and datum board mount to the staging plate on the rear of the bottom camera, through holes: B18, A19, A21, B22. The the fisheye calibration pattern should be facing down, and the gold grid lines and fiducial in the center of the Opulo logo facing upwards. Tighten this down securely.
    ![the mounting location for the datum board and holder](images/Screen Shot 2022-01-11 at 12.51.47 PM.png)


1. In the "Machine Controls" pane in the lower left, connect to the LumenPnP by pressing the power button (if you haven't already).
  ![Connect to the LumenPnP](images/connect-to-machine-power-button.png)

1. Run a rough home routine by pressing the Home button (shaped like a house). The machine will move to the X, Y, and Z zero positions. Note that the home icon will turn yellow, as the LumenPnP has homed to it's end stops, but hasn't completed its full homing routine. You will may still get one of two error messages: `FIDUCIAL-HOME no matches found.` or `Nozzle tip calibration: not enough results from vision. Check pipeline and threshold` This is normal; ignore the errors for now.
  ![Home the machine](images/Connect-and-home.png)

## Tuning the Homing Fiducial

3. Click on the `Machine Setup` tab in the top right pane.
  ![](images/Machine-Setup-Tab-3.png)

4. Click on the "Expand" checkbox to open all of the features about your machine.
  ![Expanding the Machine Config options](images/Expand-Checkbox-3.png)

5. Click on `Heads > ReferenceHead H1`.
  ![Reviewing the ReferenceHead options](images/Select-reference-head-H1.png)
  
6. In the bottom right details pane, change the `Homing Method` to `ResetToFiducialLocation`. This will set OpenPnP to use the top camera to look for the homing fiducial to more precisely home the XY gantry, instead of only using the limit switches.
  ![Switch to using the homing fiducial](images/Select-ResetToFiducialLocation.png)

7. Click `Apply` to save this change.
  ![Save the homing technique](images/Homing-fiducial-apply.png)

8. Click on the "Position Camera over location" icon button show below. This will move the top camera to approximately where your datum board is mounted.
  ![Position top camera over homing fiducial](images/Position-camera-over-homing-fiducial.png)

9. In the bottom left Machine Controls pane, Select the `Actuators` tab.
  ![Switch to the Actuators Tab](images/Actuators-tab.png)

10. Turn on the LED ring lights by pressing the `LED` button (if they're not already on).
  ![Turn on the LEDs](images/Turn-on-LEDs.png)

11. Rotate the Top Camera lens until the board is sharply in focus. If you're having trouble, try using the community-created [lens adjustment tool](https://www.printables.com/model/208453-lumen-pnp-lens-adjustment-tool).
  ![the homing fiducial in focus](images/In-focus-homing-fiducial.png)

    !!! info "Tip"
        Right click on the camera feed to change the Reticle style to see the center of the camera image. You can also use the scroll wheel to zoom in on the feed for more precision.
        ![Change the reticle that appears on the camera feed](images/Switch-reticle-type.png)

1.  Go back to the `Jog` tab in the "Machine Controls" pane.
  ![Switch to the jog tab](images/Jog-tab.png)

1.  Set the `Distance` slider to `0.1` for more precise movements.
  ![Make the jog controls more precise](images/Distance-slider-0pt1.png)

1.  Manually jog the head so that the reticle in the center of the Top Camera feed in your top camera view is perfectly centered on the Homing Fiducial in the center of the Opulo logo.
  ![use the jog controls to move the machine](images/jog-controls.png)
  ![Center the homing fiducial in the camera view](images/Homing-fiducial-centered.png)

## Double-Check Camera Exposure

As before, we're going to double-check our camera exposure.

15. Navigate to the `Machine Setup` tab.
  ![](images/Machine-Setup-Tab-4.png)

16. Click the "Expand" checkbox if necessary.
  ![Expanding the Machine Config options](images/Expand-Checkbox-4.png)

17. Navigate to `Heads > ReferenceHead H1 > Cameras > OpenPnPCaptureCamera Top`.
  ![Finding the Top Camera Settings](images/Top-camera-settings-4.png)

18. In the lower detail pane, switch to the `Device Settings` tab.
  ![Switching to the camera device settings](images/Top-camera-device-settings-4.png)

19. Right click on the camera feed to enable the image info card. This will give you the brightness histogram of the image. In the next step, you'll want to tune your exposure and other camera settings so the image isn't too bright or too dark. The histogram can help: make sure the graph isn't going all the way to the edges of the X axis in the histogram, and that will make sure all of the image's details are available for the computer to use when it is looking for the homing fiducial.
  ![enable the image histogram](images/show-image-info.png)
  ![a good histogram](images/good-histogram.png)
  ![a bad histogram](images/bad-histogram.png)

1.  Adjust the exposure and other camera settings. The goal is to make the image clear and have a lot of contrast, without being too bright or too dark overall. In some cases you can simply check the `Auto` checkbox for `Exposure`, then uncheck it to save the automatically set value.
  ![Top camera properly exposed with the auto-exposure turned on](images/Auto-exposure-on.png)

    !!! danger "For Mac Users"
        Due to an issue with the camera driver in OpenPnP, some Mac users might notice that the image settings are greyed out for you. There's a fantastic open-source application called [CameraController](https://github.com/Itaybre/CameraController) that can be used to edit these settings.

## Apply Homing Fiducial Changes

21. Double-check that:
    * The Homing Fiducial is in the center of the reticle in the camera feed.
    * The camera image is in sharp focus.
    * The camera image is properly exposed.

22. Go back to Machine Setup and select `Heads > ReferenceHead H1`.
  ![Return to the homing fiducial location settings](images/Select-Reference-Head-H1-5.png)

1.  Click on the "Capture Location" icon button to save the location where OpenPnP will start searching for the Homing Fiducial.
  ![Capture the location of the homing fiducial](images/Capture-homing-fiducial-location.png)

1.  Click `Apply` to save your changes.
  ![Save homing fiducial location](images/Homing-fiducial-apply-2.png)

1.  Click on the "Home" button in the `Machine Controls Pane > Jog Tab` and watch your machine home using the limit switches, then move the top camera over the homing fiducial and find its exact location. You may still get an error about `nozzle tip calibration`, which is normal. We'll be working on that next.
  ![Home the machine](images/Connect-and-home.png)

1.  If your machine positions correctly over the homing fiducial but you receive the error: `FIDUCIAL-HOME no matches found.`, you should double-check your camera settings. If they seem alright, you may need to adjust your [vision pipeline](../../../misc/troubleshooting/vision-pipeline-adjustment/index.md).
  ![A first attempt at homing the LumenPnP](images/Cant-find-homing-fiducial.png)

## Next Steps

Next is the [MM/Pixel Calibration.](../mm-per-pixel/index.md)
