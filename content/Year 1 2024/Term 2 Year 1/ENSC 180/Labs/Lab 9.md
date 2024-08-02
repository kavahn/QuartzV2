# Lab 9 of [[ENSC 180]]

## Code:
```function main

% Read and show the original 'cameraman.pgm' image

originalImage = imread('cameraman.pgm');

imshow(originalImage);

title('Original Image');

disp('Original Size:');

disp(size(originalImage));

% Display the last 2x2 block of the original image

disp('Last 2x2 block of the Original Image:');

disp(originalImage(end-1:end, end-1:end));

% Calling the upsampling function

upsampledImage1 = upsampleImage(originalImage);

figure, imshow(upsampledImage1);

title('Upsampled Image x2');

disp('Upsampled Size x2:');

disp(size(upsampledImage1));

% Display the last 4x4 block of the upsampled image

disp('Last 4x4 block of the Upsampled Image x2:');

disp(upsampledImage1(end-3:end, end-3:end));

% Save the output image

imwrite(upsampledImage1, 'cameraman2.pgm');

% Repeat the upward sampling process

upsampledImage2 = upsampleImage(upsampledImage1);

figure, imshow(upsampledImage2);

title('Upsampled Image x4');

disp('Upsampled Size x4:');

disp(size(upsampledImage2));

% Display the last 8x8 block of the second upsampled image

disp('Last 8x8 block of the Upsampled Image x4:');

disp(upsampledImage2(end-7:end, end-7:end));

% Save the output image

imwrite(upsampledImage2, 'cameraman4.pgm');

end

function outputImage = upsampleImage(inputImage)

% Convert the input image to double

inputImage = double(inputImage);

% Create an all-zero matrix of double size

[rows, cols] = size(inputImage);

outputImage = zeros(2*rows, 2*cols);

% Copy the input image to the new matrix with a step size of 2

outputImage(1:2:end, 1:2:end) = inputImage;

% Row interpolation

% For odd-indexed row

outputImage(1:2:end, 2:2:end-1) = (outputImage(1:2:end, 1:2:end-2) + outputImage(1:2:end, 3:2:end))/2;

% For the last column of each row, copy its left neighbor's value

outputImage(1:2:end, end) = outputImage(1:2:end, end-1);

% Column interpolation

% For the newly created columns and the original ones except the last row

outputImage(2:2:end-1, :) = (outputImage(1:2:end-2, :) + outputImage(3:2:end, :))/2;

% For the last row, copy its above neighbor's value

outputImage(end, :) = outputImage(end-1, :);

% Convert the output image to uint8

outputImage = uint8(outputImage);

end
```

## Output:
![[Lab 9-20240322031908736.webp|388]]
![[Lab 9-20240322031936850.webp|394]]
![[Lab 9-20240322032009788.webp|397]]
### Term out
![[Lab 9-20240322032044199.webp]]