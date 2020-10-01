# ADE Commander

ADE Commander (ADEC) is the companion boot.dsk for the AdamNet Drive Emulator (ADE) https://github.com/Kalidomra/AdamNet-Drive-Emulator. It is written in 100% Z80 assembler. To install, simply place the boot.dsk in the root of your ADE SD card. When the ADE is configured to automatically use boot.dsk, ADEC provides the ability to mount and run images on your ADE. It also provides a number of additional functions to help manage your images on the SD card. Although ADEC will work with current versions of the ADE code, the advanced functions will not be available. To use the advanced functions you will need to upgrade to ADE version 0.90 or higher. Just as the ADE itself, ADEC is limited to 300 files/directories per directory. 

## Commands:

### Escape/WP: Help
  Displays the help screen. Also contains the current versions of ADE and ADE Commander.

### Controllers: Move through the current directory
  Both controllers are supported. Move through the list with the joystick and press the fire button to select an image or directory. The 1-6 numbers on the controller work as function I-VI. * will return to the top of the list and # is the help screen.
  
### Arrow Keys: Move through the current directory
  The arrow keys will move through the current directory. Right and Left will jump a page at a time. Home will return to the top of the list.
 
### Return: Mount Highlighted and Reset or Change Directory
  Mount the currently highlighted image to the boot drive and reset the Adam. If the highlighted item is a directory, it will change the directory and load in the image names. When new directories are loaded in, the ADEC performs an alphabetic sort. To skip the sort, press any key. The current sort is saved when resetting the Adam from ADEC. The boot.dsk needs to be mounted to save. This will allow quick sorting of the current directory when ADEC is reloaded.

### 0-9 and A-Z: Alphabetical Jump
  Pressing the number or letter keys will jump the list to the first occurrence of that letter or number.

### I-IV : Mount Image to Drive
  Mount the currently highlighted image to the drive. The drive must be enabled to mount to it.
  
      I = Drive 1 (Device 4)
     II = Drive 2 (Device 5)
    III = Drive 3 (Device 6)
     IV = Drive 4 (Device 7)

### V : Drive Status
  The current drive status will be displayed. from this window you can unmount the images any of the drives.
  
### VI : Reset Adam
  Reset the Adam with the currently selected images.
 
### Control-B : Background Color
  Cycle through the available background colors. ADEC will automatically skip the current text color.

### Control-T : Text Color
  Cycle through the available text colors. ADEC will automatically skip the current background color.
 
### Control-S : Save Settings
  Save the existing color setup to the boot.dsk. The boot.dsk must mounted in the boot drive to save.

### Control-A : ADE Settings
  Displays the current ADE drive and debug setting. From here you can change the enabled drives and debug. Press VI to save the settings to the ADE. Be careful in disabling drives as it can render the ADE unusable and will require drive reconfiguration from the ADE itself.

### Control-F : Format Image
  Format the currently highlighted image. It will only erase the image. This is meant to replace the factory format command if it is disabled in the ADE configuration. In order to format for EOS or CP/M use you will need to use an alternate program. 

### Control-D : Delete Image or Directory
  Delete the currently highlighted image or directory. 
 
### Control-N : New Image or Directory
  Creates a new disk image or directory. From the window you can configure the file type, block size and name. 
  The block size is limited to 65,535 blocks. Any image larger than 64,205 blocks will have issues if the factory format command is not disable in the ADE. Addressing block 64, 206 (FACE hex) will initiate a format.

### Control-R : Rename Image or Directory
  Renames the currently highlighted image or directory. This will automatically assign the file extension. In the case of a cartridge file (.col, .bin or .rom) ADEC will assign the extension .rom.
  
### Control-X/C/V : Cut/Copy/Paste
  
  Control-X - Sets the current highlighted image as the image to be moved.
  Control-C - Sets the current highlighted image as the image to be copied.
  Control-X - Copies or Moves the image to the current directory and reloads the image file list.
  


