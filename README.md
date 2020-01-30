# Images-Processing
I have a small project i have to separate an object in a picture, im am beginner in matlab  i don't have much knowledge i'm learning now. The original picture is gray so i convert it again and i wanted to calculate the pixel of the object to separte in my image but i cannot continue futher if someone can help thanks 
here is the code: 
% Object recognition in a CFK-Layer Process 

clear ALL
clc;

% Load picture

img = imread('Foil.png');

% Show original picture 

subplot(4,3,1);
imshow(img);

% Convert into lab

labimg = rgb2lab( repmat(img, [1 1 3]) );

% Adjust and show color channels

subplot(4,3,2);
imshow(labimg(:,:,1),[]);

subplot(4,3,3);
imshow(labimg(:,:,2),[]);
subplot(4,3,4);
imshow(labimg(:,:,2),[]);

% % Define classes
foil = img(159:205, 178:307, :);
backgr = img (151:213, 173:316, :);

%  % Save averages from classes in a matrix
% classes = [[mean2(foil(:,:,2)), mean2(foil(:,:,3))]', [mean2(backgr(:,:,3)), mean2(backgr(:,:,2))]']; // here is the error 

% [height, width, channels] = size(labimg);
% 
% classimg = zeros(height,width);
% 
% for i = 1:height
%     for j = 1:width
%         classimg(i,j) = nearestNeighbour2d(labimg(i,j,1:1), classes); // here is the error 
%     end
% end
% 
% % Show class-image 
% subplot(4,3,5);
% imshow(classimg, []);
