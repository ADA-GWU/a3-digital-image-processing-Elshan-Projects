# Task 1 - Noise removal and reconstruction
The notebook containing my solution is: *Task_1_Chemical.ipynb*
### inchi2.png
* __Dilation + Erosion:__ This approach has managed to only slightly remove the pepper noise with kernel sizes set to 3 for both operations. Larger kernels resulted in significant artifacts with the letters.
* __Addition of Vertical Line and Horizontal Line Convolutions:__ This approach fully removed the pepper noise however some lines became less defined. The kernel size was set to 2 since larger kernels erase digonal lines.
* __Complex Cleaning - *Addition of Horizontal and Vertical + Dilation:*__ 2 dilation operations (kernel size = 2) were performed to make the lines more pronounced. This approach has proved to be the best one with all the noise removed and  both letters and lines decently being decently discernable.
