# Image Comparison Node JS in Test automation using simple Image Processing method
## Please be aware this code is not maintained, but can be used as a reference.
## Why Image Comparison is important in Testing

Testing a website, or an application, does not only require testing major functionnalities (for instance testing if buttons or an input box field works). In some cases, before sending our product into production, it is also important to verify if an element of the page has disappeared, if elements on the result page are what are expected, or if any color changes were made. The npm program below uses a simple image processing method that compares two images and outputs their differences, as well as automatically fails a test if any difference is observed. The program also resizes the images so that the calculation between the matrices is possible.  

### Download
To download the npm, type in your terminal : 

    npm install @uuduru/compareimages

To use the dependency in your programs, type : 

    ImageCompare = require('@uuduru/compareimages');

### Usage in testing
Before testing if the baseline screenshot has differences with the next screenshot, we must first run our first test. Two screenshots that need to be compared must both have the same name and type (.png or .jpg). The function ImageCompare receives in argument the path file of the screenshots. For example : 

    ImageCompare('C:/Users/ugoduru/Image1.png')

If this is our first test with an image named Image1.png, the output console indicates that a first test was ran, and the program saves Image1.png under the folder named node_modules/@uuduru/compareimages/screenshots_compare for future comparisons. The next time ImageCompare('C:/Users/ugoduru/Image1.png') is called, a comparison pixel by pixel between the image in the function's argument and the image in screenshots_compare will be done. The result image is saved under the folder node_modules/@uuduru/compareimages/ComparedImageFolder.

### Test passed or Test failed
The program automatically stops your test if any differences between your screenshots are visible. If not, nothing is done and the console outputs a success.


![My Image](Paris.png)
![My Image](Paris2.png)
![My Image](Image.png)

The slight difference between these two images is shown in the third image.

## Author : DURU Ugochukwu
