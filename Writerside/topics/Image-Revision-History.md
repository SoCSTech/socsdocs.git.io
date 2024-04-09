# Image Revision History

## Overview
Below is a table of our system images, current and past. **Bold** denotes and image currently in use.

## Naming Schema
The image names do actually have a meaning!

### Example
2324SEMB1
* 2324: The **academic** year the image is built for.
* SEMB: The semester the image is built for, we have 3 Semesters, A,B, and, C - this would translate to SEMA, SEMB, and, SEMC (rarely used).
* 1: The revision index, increment by 1 for every time we make a major change. 0 is for testing only - **do not deploy a version 0 image.** 
  * Sometimes you will see EX; this means lots of versions have taken place in a semester, and this is the final silver bullet
* When making an image, you will need to capture separate versions for SATA and NVMe drives due to partition differences, append the following to the image name:
  * -S: SATA machines
  * -NV: NVMe machines

## Versions and Changelog
| Image Version  | Date Captured | Locations          | Release Notes                                                                                                                                                                          |
|----------------|---------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **2324SEMB1**  | Late Jan '24  | All Computing Labs | - This image added software required for Semester B<br/>- Updated Windows Version to 23H2                                                                                              |
| **2324GL1**    | Late Jan '24  | The Games Lab      | - Initial Release for the Games Lab PCs<br/>- Image created solely for Games Dev and testing<br/>- Smaller compared to the general use image to allow for bigger asset stores          |
| **2324SEMAEX** | Late Oct '23  | All Computing Labs | - Fixed NVidia Driver issues under Windows that prevented VR and UE working correctly<br/>- Fixed issues with the System and Env path<br/>- Removed Anaconda and moved to pure Jupyter |
