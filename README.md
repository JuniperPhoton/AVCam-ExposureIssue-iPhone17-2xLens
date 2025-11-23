# Exposure issue on iPhone 17 Pro using 2x lens

In the following conditions, the output photo will be using -2eV while the settings and the preview will be 0 eV, resulting in a much darker image than the preview.

1. `AVCapturePhotoOutput`'s `isAutoDeferredPhotoDeliveryEnabled` should be set to `false`.
2. `AVCapturePhotoSettings`'s `photoQualityPrioritization` is set to `quality`.
3. Using 2x zoomed lens for the dedicated wide/telephoto or the fusion camera.
4. Using iPhone 17 Pro + iOS 26.1. On the other hand, iPhone 16 Pro + iOS 26.1 works as expected in this case.

This repo builds on top of the official [AVCam](https://developer.apple.com/documentation/avfoundation/avcam-building-a-camera-app) repo. See the latest commit to see the changes to reproduce this issue.

To illustrate this issue:

<img width="540" height="558" alt="image" src="https://github.com/user-attachments/assets/abfda23b-da7c-40a4-b10d-5c561d8d6d31" />
