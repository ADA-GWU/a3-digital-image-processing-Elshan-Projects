# Task 1 - Noise removal and reconstruction
* The notebook containing my solution is: *Task_1_Chemical.ipynb*/\
* The results of this task are saved in the _Results/Chemical_ folder with a separate subfolder for every processed image.
### inchi2.png
* __Dilation + Erosion:__ This approach has managed to only slightly remove the pepper noise with kernel sizes set to 3 for both operations. Larger kernels resulted in significant artifacts with the letters.
* __Addition of Vertical Line and Horizontal Line Convolutions:__ This approach fully removed the pepper noise however some lines became less defined. The kernel size was set to 2 since larger kernels erase digonal lines.
* __Complex Cleaning - *Addition of Horizontal and Vertical + Dilation:*__ 2 dilation operations (kernel size = 2) were performed to make the lines more pronounced. This approach has proved to be the best one with all the noise removed and  both letters and lines decently being decently discernable.
### inchi6.png
* __Dilation + 3 x Erosion__: After dilating the image with a 4-pixel kernel, 3 erosions (kernel size = 2) were required to reduce the granular size of the pepper noise with the letters and lines fully intact.
* __Addition of Vertical Line and Horizontal Line Convolutions:__ This approach fully removed the pepper noise while disrupting the diagonal lines.
* __Complex Cleaning - Addition of Horizontal and Vertical + Dilation:__ The discontinous lines from the convolution operations were fixed by dilating them with a 3-pixel kernel resulting in a decent final result where all the noise was removed with the lines intact.
### inchi7.png
* __Dilation + 2 x Erosion:__ Dilation with its kernel size set to 4 was followed by 2 erosion operations (kernel sizes = 3 and 2). The granular size of pepper noise was reduced, however the pepper dots are still visible. Further erosions introduce discontinuities within the lines.
* __Addition of Vertical Line and Horizontal Line Convolutions:__ 2-pixel kernels with vertical and horizontal lines fully removed the pepper noise but disrupted most of the lines around the OH and NH groups.
* __Complex Cleaning - Addition of Horizontal and Vertical + Dilation:__ Dilation with a 3-pixel kernel after the line convolutions fixed the lines to a decent degree while preserving the noise removal success of the previous line convolutions. This approach is combined the best feature of the previous attempts.
# Task 2 - Speckle removal
