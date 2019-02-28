## Luminance Adjustment

### Overview
Adjust luminance of an image.

### Usage
```
$ python adjust_luminance.py
==============================
     Luminance Adjustment
       Tomomasa Uchida
         2019/02/28
==============================

USAGE   : $ python adjust_luminance.py [input_image_data] [input_image_data(LR=1)]
EXAMPLE : $ python adjust_luminance.py [input_image.bmp] [input_image_LR1.bmp]
```

### Example
```
==============================
     Luminance Adjustment
       Tomomasa Uchida
         2019/02/28
==============================

Input image data (args[1])       : images/IMAGE_DATA/kabuto_alpha02_LR200_black.bmp
Input image data(LR=1) (args[2]) : images/IMAGE_DATA/kabuto_alpha02_LR1_black.bmp


====================================
 STEP1 : Get max pixel value (LR=1)
====================================
Input image (RGB)                : (512, 512, 3)
N_all                            : 262144 (pixels)
N_all_non_bgcolor                : 176317 (pixels)
Max pixel value                  : 173 (pixel value)
Mean pixel value                 : 54.7 (pixel value)

Max pixel value (LR=1)           : 255 (pixel value)
Mean pixel value (LR=1)          : 134.4 (pixel value)
Num. of max pixel value (LR=1)   : 19 (pixels)
Ratio of max pixel value (LR=1)  : 0.01 (%)
Most frequent pixel value (LR=1) : 204 (pixel value)


================================================
 STEP2 : Search for reference pixel value (LR=1)
================================================
Reference pixel value (LR=1)     : 233 (pixel value)
Reference section (LR=1)         : 233 ~ 255 (pixel value)
Ratio of reference section (LR=1): 1.07 (%)


=============================
 STEP3 : Correct pixel value
=============================
p_final                          : 2.39
Ratio of reference section       : 1.12 (%)
```

## Image

### Input image
![sample1](resources/sample/ookabuto/input.bmp)

### Input image (LR=1)
![sample2](resources/sample/ookabuto/LR1.bmp)

### Adjusted image
![sample2](resources/sample/ookabuto/adjusted_2.39.bmp)

### Figure
![sample2](resources/sample/ookabuto/figure_2.39.png)