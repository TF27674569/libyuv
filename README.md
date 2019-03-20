## libyuv
1 [下载libyuv](https://chromium.googlesource.com/external/libyuv)<br/>
2 clone到本地 <br/>
3 将libyuv重命名为jni <br/>
4 修改Android.mk <br/>
```java
LOCAL_MODULE := libyuv #这里名字去掉后戳
LOCAL_MODULE_TAGS := optional

include $(BUILD_SHARED_LIBRARY) #这里改为生成动态库默认是静态库
```
5 进入与jni同级的目录，注意不是jni目录里面 <br/>
6 执行ndk-build 等待编译完成 <br/>
## 注意
编译会自动生成libs文件夹so在此文件夹内<br/>
头文件在jni/include里面<br/>
我这里的环境为mac，linux环境也是一样<br/>
编译如图则是成功了![chenggong](https://github.com/TF27674569/libyuv/blob/master/image/yuv.jpg)
