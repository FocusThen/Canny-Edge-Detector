# Canny Edge Detector

### Orginal image
![sunflower](https://user-images.githubusercontent.com/47830409/63924154-7293e400-ca50-11e9-854a-25f133625d74.jpg)

### we need rgb to gray
```sh
gray = cv2.cvtColor(image_copy, cv2.COLOR_RGB2GRAY)

plt.imshow(gray, cmap="gray")
```
### we need lower and upper for Canny
```sh
lower = 120
upper = 240

edges = cv2.Canny(gray, lower, upper)
plt.imshow(edges, cmap="gray")
```
#### More details for [Canny](https://docs.opencv.org/3.1.0/da/d22/tutorial_py_canny.html)

![ss2](https://user-images.githubusercontent.com/47830409/63924662-50e72c80-ca51-11e9-9fb4-fdf22b3e74a0.PNG)

### Different wide and tight
```sh
wide = cv2.Canny(gray, 30, 100)
tight = cv2.Canny(gray, 180, 240)

f, (ax1, ax2) = plt.subplots(1,2, figsize=(20,10))

ax1.imshow(wide, cmap="gray")
ax1.set_title("Wide")

ax2.imshow(tight, cmap="gray")
ax2.set_title("Tight")
```

![ss3](https://user-images.githubusercontent.com/47830409/63924688-6197a280-ca51-11e9-80cb-595da20ce6ef.PNG)
