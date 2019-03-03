The code in this repository is based on the Embedded Provisioner described in [this forum post](https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2018/05/31/bt_mesh_embeddedpro-qoHB) on the Silicon Labs forum

To use this project:
1. Use Help->Update Software and the Product Updates tab of the Package Manager to update all Simplicity IDE files to the latest revision
2. Use the Help->Update Software Package Manager to update install the following Mesh and Bluetooth SDK versions:
   1. Mesh SDK/ADK 1.4.0
   2. Bluetooth SDK 2.11.2.0
3. Checkout this repository locally in your ~/SimplicityStudio/vX_workspace folder.
4. Build and program on a BRD4104A radio/dev board.
5. On boot, hold down the PB0 or PB1 buttons to factory reset any existing mesh configuration.
6. Open a serial terminal on the provisioner device.
7. Setup 1 or more devices with Bluetooth Mesh software (for instance, the switch or light example projects) for provisioning.
   1. Hold down the PB0 or PB1 buttons on power-up to clear any existing mesh configuration
8. Power on the device to be provisioned
   1. You should be prompted on the serial terminal of the provisioner to confirm the addition of this part to the network with a message like:
   ```
    Unprovisioned beacon, UUID: 53696c6162734465762d60f2b5570b00 (f2 60)type: PB-ADV
    -> confirm? (use buttons or keys 'y' / 'n')`
   ```
   1. The value in parenthesis (f2 60) should match the bluetooth address printed on the display.
9. Enter "y" in the terminal or press push button PB1 to confirm.
   1. Look for a `configuration complete` message to confirm provisioning was successful.


