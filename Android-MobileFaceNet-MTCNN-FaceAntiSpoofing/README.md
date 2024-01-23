# MobileFaceNet-Android
The project involves 3 models.  
  
MTCNN(pnet.tflite, rnet.tflite, onet.tflite), input: one Bitmap, output: Box. Use this model to detect faces from an image.  
  
FaceAntiSpoofing(FaceAntiSpoofing.tflite), input: one Bitmap, output: float score. Use this model to determine whether the image is an attack.  
  
MobileFaceNet(MobileFaceNet.tflite), input: two Bitmaps, output: float score. Use this model to judge whether two face images are one person.  


  
# BUILD
After putting .tflite in your assets directory, remember to add this code to your gradle:  
aaptOptions {  
　　noCompress "tflite"  
}  
  
