# image-display
resizing images, viewing in color and grey



import cv2,os

img=os.listdir("pup")
for i in  img:
    
    new_img=cv2.imread(".\\pup\\{}".format(i),0)
    resized_img=cv2.resize(new_img,(300,200))
    cv2.imshow(".\\grey\\{}".format(i),resized_img)
    print(resized_img)
    key = cv2.waitKey(0)
if key==100:
        cv2.destroyAllWindows()
