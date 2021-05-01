# uts_pengolahan_citra
Konversi RGB

![image](https://user-images.githubusercontent.com/56399756/116784623-6bdc3080-aabf-11eb-9403-741c758b024c.png)

![image](https://user-images.githubusercontent.com/56399756/116784636-7ac2e300-aabf-11eb-9a12-fb40f2d5883e.png)

sintak :

[filename, pathname] = uigetfile({'*.jpg','*.png'});
img = imread([pathname, filename]);
 
axes(handles.axes1);
imshow(img);
 
R = img(:,:,1);
G = img(:,:,2);
B = img(:,:,3);
 
Red = cat(3,R,G*0,B*0);
Green = cat(3,R*0,G,B*0);
Blue = cat(3,R*0,G*0,B);
 
axes(handles.axes2);
imshow(Red);
 
axes(handles.axes3);
imshow(Green);
 
axes(handles.axes4);
imshow(Blue);

