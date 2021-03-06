PRUNED NON-LOCAL MEANS (PNLM)

Authors     : Garvit Mohata, Sanjay Ghosh, and Kunal Narayan Chaudhury.
Reference   : S. Ghosh, A. K. Mandal, and K. N. Chaudhury, "Pruned Non-Local Means", IET Image Processing, vol. 11, no. 5, pp. 317-323, April 2017.

Installation
---------------------------------------------------------------------------
The mex files can be built and compiled using an already installed compiler for C, or by downloading one if no supported SDK or compiler is present. To be able to use the mex file, first setup your compiler with "mex -setup" and then build it by typing "mex GUI_mex.c" on the command line window. 

Note that the mex file needs to be built separately before using the GUI. 

Description
---------------------------------------------------------------------------

Functions:

    demo_pnlm.m : This is a demo file to show the functioning of the mex file.

    actual.m    : This is the function that operates and handles the GUI interface. A mex file GUI_mex.c is also being called by this function with required input parameters.

        USER INPUTS (for GUI Interface):
        -------------------------------     
        Sigma (σ)                  : Double  (Range 0-100)    % Noise level of the noisy image
        Search window parameter (S): Integer (Usually = 10)   % Width/extension of the search window of pixel i in any direction from it.
        Patch size parameter (K)   : Integer (Usually = 3)    % Width/extension of the patch of pixel i in any direction from it.
        Smoothing parameter (h)    : Double  (Usually = 10 σ)
    
Mex files:

    GUI_mex.c: This is the mex file that actually performs the computation intensive part for processing through pnlm. The PNLM-processed denoised image and the sum of the partial derivative terms of it are computed in this function.


How to use the GUI
---------------------------------------------------------------------------
1. Type the name of the function "actual" on the command line window or click "Run" button in the Run section of the Editor tab of MATLAB to run the function after opening it. A GUI interface named "actual" appears in a new window on the screen. 

2. Click "Browse" to browse through the folders or directories to select an image. After selecting an image, the full path for its location is shown in the box ahead of "Path" and the image is displayed above the "(A) Clean Image" caption.

3. Type the noise level you wish to add in the clean image in the box ahead of "Noise (σ)" and click "Add Noise". An image with the added noise appears above the "(B) Noisy Image" caption and the PSNR value for this image gets displayed.

4. Enter the values of the parameters "S", "K" and "h" in the boxes in the "Parameters" section. The recommended values have been given above in "Description".

5. Click "Run" to output the PNLM-processed denoised image and its method noise above their respective captions, namely "(C) PNLM" and "(D) Method Noise (B-C)". The PSNR value for the denoised image also gets displayed.

6. Finally, you can save either of the four images or all of them by selecting the required option in the "Save" drop-down list.

7. Click "Close" to close the GUI.