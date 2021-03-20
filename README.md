# qtCvFrameLearn
Qt-based opencv plugin framework qtCvFrameLearn.

@[TOC](基于QT的opencv插件框架qtCvFrameLearn)
# 目录  
#  0 结果展示
项目链接: [基于QT的opencv插件框架qtCvFrameLearn](https://github.com/pengguanjun/qtCvFrameLearn).
![基于QT的opencv插件框架qtCvFrameLearn](https://img-blog.csdnimg.cn/20210320225659838.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
# 1 参考链接
链接: [Qt-5-and-OpenCV-4-Computer-Vision-Projects](https://github.com/PacktPublishing/Qt-5-and-OpenCV-4-Computer-Vision-Projects).
链接: [qt5.13配置opencv4.2环境 mscv版](https://editor.csdn.net/md/).


# 2 文件目录结构
![qt插件框架qtCvFrameLearn](https://img-blog.csdnimg.cn/20210320223405607.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)![qt插件框架qtCvFrameLearn](https://img-blog.csdnimg.cn/20210320223250544.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
# 3 项目配置文件ImageEditor.pro
```cpp
######################################################################
# Automatically generated by qmake (3.1) Sun Nov 11 20:07:20 2018
######################################################################


TEMPLATE = app
TARGET = ImageEditor
DESTDIR = ../App

QT += core gui network
greaterThan(QT_MAJOR_VERSION, 4): QT += widgets

## use your own path in the following config
#unix: !mac {
#    INCLUDEPATH += /home/kdr2/programs/opencv/include/opencv4
#    LIBS += -L/home/kdr2/programs/opencv/lib -lopencv_core -l opencv_imgproc
#}

#unix: mac {
#    INCLUDEPATH += /path/to/opencv/include/opencv4
#    LIBS += -L/path/to/opencv/lib -lopencv_world
#}

#win32 {
##    INCLUDEPATH += c:/path/to/opencv/include/opencv4
##    LIBS += -lc:/path/to/opencv/lib/opencv_world
#    INCLUDEPATH += C:/opencv451/include/opencv2
##    LIBS += -lC:/opencv451/vc15/opencv_world
#}

# The following define makes your compiler warn you if you use any
# feature of Qt which has been marked as deprecated (the exact warnings
# depend on your compiler). Please consult the documentation of the
# deprecated API in order to know how to port your code away from it.
DEFINES += QT_DEPRECATED_WARNINGS

# You can also make your code fail to compile if you use deprecated APIs.
# In order to do so, uncomment the following line.
# You can also select to disable deprecated APIs only up to a certain version of Qt.
#DEFINES += QT_DISABLE_DEPRECATED_BEFORE=0x060000    # disables all the APIs deprecated before Qt 6.0.0

# Input
HEADERS += mainwindow.h editor_plugin_interface.h
SOURCES += main.cpp mainwindow.cpp

# opencv config
INCLUDEPATH += C:/opencv451/include
DEPENDPATH += C:/opencv451/include

win32:CONFIG(release, debug|release): LIBS += -LC:/opencv451/vc15/lib/ \
opencv_aruco451.lib  \
opencv_bgsegm451.lib  \
opencv_bioinspired451.lib  \
opencv_ccalib451.lib  \
opencv_core451.lib  \
opencv_cudaarithm451.lib  \
opencv_cudabgsegm451.lib  \
opencv_cudacodec451.lib  \
opencv_cudafilters451.lib  \
opencv_cudaimgproc451.lib  \
opencv_cudalegacy451.lib  \
opencv_cudaobjdetect451.lib  \
opencv_cudaoptflow451.lib  \
opencv_cudastereo451.lib  \
opencv_cudawarping451.lib  \
opencv_cudev451.lib  \
opencv_cvv451.lib  \
opencv_datasets451.lib  \
opencv_dnn451.lib  \
opencv_dpm451.lib  \
opencv_face451.lib  \
opencv_flann451.lib  \
opencv_fuzzy451.lib  \
opencv_gapi451.lib  \
opencv_hfs451.lib  \
opencv_highgui451.lib  \
opencv_imgcodecs451.lib  \
opencv_imgproc451.lib  \
opencv_mcc451.lib  \
opencv_ml451.lib  \
opencv_objdetect451.lib  \
opencv_optflow451.lib  \
opencv_photo451.lib  \
opencv_plot451.lib  \
opencv_quality451.lib  \
opencv_rapid451.lib  \
opencv_reg451.lib  \
opencv_rgbd451.lib  \
opencv_saliency451.lib  \
opencv_shape451.lib  \
opencv_stereo451.lib  \
opencv_stitching451.lib  \
opencv_superres451.lib  \
opencv_text451.lib  \
opencv_tracking451.lib  \
opencv_video451.lib  \
opencv_videoio451.lib  \
opencv_videostab451.lib  \
opencv_ximgproc451.lib  \
opencv_xobjdetect451.lib  \
opencv_xphoto451.lib
else:win32:CONFIG(debug, debug|release): LIBS += -LC:/opencv451/vc15/lib/  \
opencv_aruco451d.lib  \
opencv_bgsegm451d.lib  \
opencv_bioinspired451d.lib  \
opencv_ccalib451d.lib  \
opencv_core451d.lib  \
opencv_cudaarithm451d.lib  \
opencv_cudabgsegm451d.lib  \
opencv_cudacodec451d.lib  \
opencv_cudafilters451d.lib  \
opencv_cudaimgproc451d.lib  \
opencv_cudalegacy451d.lib  \
opencv_cudaobjdetect451d.lib  \
opencv_cudaoptflow451d.lib  \
opencv_cudastereo451d.lib  \
opencv_cudawarping451d.lib  \
opencv_cudev451d.lib  \
opencv_cvv451d.lib  \
opencv_datasets451d.lib  \
opencv_dnn451d.lib  \
opencv_dpm451d.lib  \
opencv_face451d.lib  \
opencv_flann451d.lib  \
opencv_fuzzy451d.lib  \
opencv_gapi451d.lib  \
opencv_hfs451d.lib  \
opencv_highgui451d.lib  \
opencv_imgcodecs451d.lib  \
opencv_imgproc451d.lib  \
opencv_mcc451d.lib  \
opencv_ml451d.lib  \
opencv_objdetect451d.lib  \
opencv_optflow451d.lib  \
opencv_photo451d.lib  \
opencv_plot451d.lib  \
opencv_quality451d.lib  \
opencv_rapid451d.lib  \
opencv_reg451d.lib  \
opencv_rgbd451d.lib  \
opencv_saliency451d.lib  \
opencv_shape451d.lib  \
opencv_stereo451d.lib  \
opencv_stitching451d.lib  \
opencv_superres451d.lib  \
opencv_text451d.lib  \
opencv_tracking451d.lib  \
opencv_video451d.lib  \
opencv_videoio451d.lib  \
opencv_videostab451d.lib  \
opencv_ximgproc451d.lib  \
opencv_xobjdetect451d.lib  \
opencv_xphoto451d.lib
else:unix:!macx: LIBS += -LC:/opencv451/vc15/lib/ -lopencv_core451 \
-lopencv_*451

DISTFILES += \
    plugins/.gitkeep \
    plugins/AffinePlugin.dll \
    plugins/CartoonPlugin.dll \
    plugins/ErodePlugin.dll \
    plugins/RotatePlugin.dll \
    plugins/SharpenPlugin.dll
```

# 4 项目配置文件AffinePlugin.pro
```cpp
######################################################################
# Automatically generated by qmake (3.1) Fri Nov 30 20:56:01 2018
######################################################################
#QT       += widgets

TARGET = AffinePlugin
TEMPLATE = lib
DESTDIR = ../App/plugins
INCLUDEPATH +=../ImageEditor


## use your own path in the following config
#unix: !mac {
#    INCLUDEPATH += /home/kdr2/programs/opencv/include/opencv4
#    LIBS += -L/home/kdr2/programs/opencv/lib -lopencv_core -l opencv_imgproc
#}

#unix: mac {
#    INCLUDEPATH += /path/to/opencv/include/opencv4
#    LIBS += -L/path/to/opencv/lib -lopencv_world
#}

#win32 {
#    INCLUDEPATH += C:/opencv451/include
#    LIBS += -lC:/opencv451/vc15/lib/ \
#            -lopencv_core451d
#            -lopencv_imgproc451d
#}

# The following define makes your compiler warn you if you use any
# feature of Qt which has been marked as deprecated (the exact warnings
# depend on your compiler). Please consult the documentation of the
# deprecated API in order to know how to port your code away from it.
DEFINES += QT_DEPRECATED_WARNINGS

# You can also make your code fail to compile if you use deprecated APIs.
# In order to do so, uncomment the following line.
# You can also select to disable deprecated APIs only up to a certain version of Qt.
#DEFINES += QT_DISABLE_DEPRECATED_BEFORE=0x060000    # disables all the APIs deprecated before Qt 6.0.0

# Input
HEADERS += affine_plugin.h
SOURCES += affine_plugin.cpp


# opencv config
INCLUDEPATH += C:/opencv451/include
DEPENDPATH += C:/opencv451/include

win32:CONFIG(release, debug|release): LIBS += -LC:/opencv451/vc15/lib/ \
opencv_aruco451.lib  \
opencv_bgsegm451.lib  \
opencv_bioinspired451.lib  \
opencv_ccalib451.lib  \
opencv_core451.lib  \
opencv_cudaarithm451.lib  \
opencv_cudabgsegm451.lib  \
opencv_cudacodec451.lib  \
opencv_cudafilters451.lib  \
opencv_cudaimgproc451.lib  \
opencv_cudalegacy451.lib  \
opencv_cudaobjdetect451.lib  \
opencv_cudaoptflow451.lib  \
opencv_cudastereo451.lib  \
opencv_cudawarping451.lib  \
opencv_cudev451.lib  \
opencv_cvv451.lib  \
opencv_datasets451.lib  \
opencv_dnn451.lib  \
opencv_dpm451.lib  \
opencv_face451.lib  \
opencv_flann451.lib  \
opencv_fuzzy451.lib  \
opencv_gapi451.lib  \
opencv_hfs451.lib  \
opencv_highgui451.lib  \
opencv_imgcodecs451.lib  \
opencv_imgproc451.lib  \
opencv_mcc451.lib  \
opencv_ml451.lib  \
opencv_objdetect451.lib  \
opencv_optflow451.lib  \
opencv_photo451.lib  \
opencv_plot451.lib  \
opencv_quality451.lib  \
opencv_rapid451.lib  \
opencv_reg451.lib  \
opencv_rgbd451.lib  \
opencv_saliency451.lib  \
opencv_shape451.lib  \
opencv_stereo451.lib  \
opencv_stitching451.lib  \
opencv_superres451.lib  \
opencv_text451.lib  \
opencv_tracking451.lib  \
opencv_video451.lib  \
opencv_videoio451.lib  \
opencv_videostab451.lib  \
opencv_ximgproc451.lib  \
opencv_xobjdetect451.lib  \
opencv_xphoto451.lib
else:win32:CONFIG(debug, debug|release): LIBS += -LC:/opencv451/vc15/lib/  \
opencv_aruco451d.lib  \
opencv_bgsegm451d.lib  \
opencv_bioinspired451d.lib  \
opencv_ccalib451d.lib  \
opencv_core451d.lib  \
opencv_cudaarithm451d.lib  \
opencv_cudabgsegm451d.lib  \
opencv_cudacodec451d.lib  \
opencv_cudafilters451d.lib  \
opencv_cudaimgproc451d.lib  \
opencv_cudalegacy451d.lib  \
opencv_cudaobjdetect451d.lib  \
opencv_cudaoptflow451d.lib  \
opencv_cudastereo451d.lib  \
opencv_cudawarping451d.lib  \
opencv_cudev451d.lib  \
opencv_cvv451d.lib  \
opencv_datasets451d.lib  \
opencv_dnn451d.lib  \
opencv_dpm451d.lib  \
opencv_face451d.lib  \
opencv_flann451d.lib  \
opencv_fuzzy451d.lib  \
opencv_gapi451d.lib  \
opencv_hfs451d.lib  \
opencv_highgui451d.lib  \
opencv_imgcodecs451d.lib  \
opencv_imgproc451d.lib  \
opencv_mcc451d.lib  \
opencv_ml451d.lib  \
opencv_objdetect451d.lib  \
opencv_optflow451d.lib  \
opencv_photo451d.lib  \
opencv_plot451d.lib  \
opencv_quality451d.lib  \
opencv_rapid451d.lib  \
opencv_reg451d.lib  \
opencv_rgbd451d.lib  \
opencv_saliency451d.lib  \
opencv_shape451d.lib  \
opencv_stereo451d.lib  \
opencv_stitching451d.lib  \
opencv_superres451d.lib  \
opencv_text451d.lib  \
opencv_tracking451d.lib  \
opencv_video451d.lib  \
opencv_videoio451d.lib  \
opencv_videostab451d.lib  \
opencv_ximgproc451d.lib  \
opencv_xobjdetect451d.lib  \
opencv_xphoto451d.lib
else:unix:!macx: LIBS += -LC:/opencv451/vc15/lib/ -lopencv_core451 \
-lopencv_*451


```

# 5 代码梳理
##  5.1 插件加载

```cpp
void MainWindow::loadPlugins()
{
    QDir pluginsDir(QApplication::instance()->applicationDirPath() + "/plugins");
    QStringList nameFilters;
    nameFilters << "*.so" << "*.dylib" << "*.dll";
    QFileInfoList plugins = pluginsDir.entryInfoList(
        nameFilters, QDir::NoDotAndDotDot | QDir::Files, QDir::Name);
    foreach(QFileInfo plugin, plugins) {
        QPluginLoader pluginLoader(plugin.absoluteFilePath(), this);
        EditorPluginInterface *plugin_ptr = dynamic_cast<EditorPluginInterface*>(pluginLoader.instance());
        if(plugin_ptr) {
            QAction *action = new QAction(plugin_ptr->name());
            editMenu->addAction(action);
            editToolBar->addAction(action);
            editPlugins[plugin_ptr->name()] = plugin_ptr;
            connect(action, SIGNAL(triggered(bool)), this, SLOT(pluginPerform()));
            // pluginLoader.unload();
        } else {
            qDebug() << "bad plugin: " << plugin.absoluteFilePath();
        }
    }
}
```

## 5.2 qt图像与opencv图像转换
```cpp
void MainWindow::pluginPerform()
{
    if (currentImage == nullptr) {
        QMessageBox::information(this, "Information", "No image to edit.");
        return;
    }

    QAction *active_action = qobject_cast<QAction*>(sender());
    EditorPluginInterface *plugin_ptr = editPlugins[active_action->text()];
    if(!plugin_ptr) {
        QMessageBox::information(this, "Information", "No plugin is found.");
        return;
    }

    QPixmap pixmap = currentImage->pixmap();
    QImage image = pixmap.toImage();
    image = image.convertToFormat(QImage::Format_RGB888);
    cv::Mat mat = cv::Mat(
        image.height(),
        image.width(),
        CV_8UC3,
        image.bits(),
        image.bytesPerLine());

    plugin_ptr->edit(mat, mat);

    QImage image_edited(
        mat.data,
        mat.cols,
        mat.rows,
        mat.step,
        QImage::Format_RGB888);
    pixmap = QPixmap::fromImage(image_edited);
    imageScene->clear();
    imageView->resetMatrix();
    currentImage = imageScene->addPixmap(pixmap);
    imageScene->update();
    imageView->setSceneRect(pixmap.rect());
    QString status = QString("(editted image), %1x%2")
        .arg(pixmap.width()).arg(pixmap.height());
    mainStatusLabel->setText(status);
}
```

## 5.3 各个插件中的opencv函数学习
![opencv中的Mat()函数](https://img-blog.csdnimg.cn/20210320222520596.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)



### 5.3.1 affine_plugin
```cpp
// affine_plugin
void AffinePlugin::edit(const cv::Mat &input, cv::Mat &output)
{

    cv::Point2f triangleA[3];
    cv::Point2f triangleB[3];

    triangleA[0] = cv::Point2f(0 , 0);
    triangleA[1] = cv::Point2f(1 , 0);
    triangleA[2] = cv::Point2f(0 , 1);

    triangleB[0] = cv::Point2f(0, 0);
    triangleB[1] = cv::Point2f(1, 0);
    triangleB[2] = cv::Point2f(1, 1);

    cv::Mat affineMatrix = cv::getAffineTransform(triangleA, triangleB);
    cv::Mat result;
    cv::warpAffine(
        input, result,
        affineMatrix, input.size(), // output image size, same as input
        cv::INTER_CUBIC, // Interpolation method
        cv::BORDER_CONSTANT  // Extrapolation method
        //BORDER_WRAP  // Extrapolation method
    );

    output = result;
}
```

#### getAffineTransform
```cpp
CV_EXPORTS_W Mat getAffineTransform( InputArray src, InputArray dst );
```

![opencv中的getAffineTransform()函数](https://img-blog.csdnimg.cn/20210320205708411.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)


#### warpAffine
```cpp
CV_EXPORTS_W void warpAffine( InputArray src, OutputArray dst,
                              InputArray M, Size dsize,
                              int flags = INTER_LINEAR,
                              int borderMode = BORDER_CONSTANT,
                              const Scalar& borderValue = Scalar());
```

![opencv中的warpAffine()函数](https://img-blog.csdnimg.cn/20210320210159382.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)


### 5.3.2 cartoon_plugin
```cpp
// cartoon_plugin
void CartoonPlugin::edit(const cv::Mat &input, cv::Mat &output)
{
    int num_down = 2;
    int num_bilateral = 7;

    cv::Mat copy1, copy2;
    cv::Mat image_gray, image_edge;

    copy1 = input.clone();
    for(int i = 0; i < num_down; i++) {
        cv::pyrDown(copy1, copy2);
        copy1 = copy2.clone();
    }

    for(int i = 0; i < num_bilateral; i++) {
        cv::bilateralFilter(copy1, copy2, 9, 9, 7);
        copy1 = copy2.clone();
    }

    for(int i = 0; i < num_down; i++) {
        cv::pyrUp(copy1, copy2);
        copy1 = copy2.clone();
    }

    if (input.cols != copy1.cols  || input.rows != copy1.rows) {
        cv::Rect rect(0, 0, input.cols, input.rows);
        copy1(rect).copyTo(copy2);
        copy1 = copy2;
    }

    cv::cvtColor(input, image_gray, cv::COLOR_RGB2GRAY);
    cv::medianBlur(image_gray, image_gray, 5);

    cv::adaptiveThreshold(image_gray, image_gray, 255,
        cv::ADAPTIVE_THRESH_MEAN_C, cv::THRESH_BINARY, 9, 2);

    cv::cvtColor(image_gray, image_edge, cv::COLOR_GRAY2RGB);

    output = copy1 & image_edge;

    /*
    cv::GaussianBlur(image_edge, image_edge, cv::Size(5, 5), 0);
    cv::Mat mask(input.rows, input.cols, CV_8UC3, cv::Scalar(90, 90, 90));
    mask = mask & (~image_edge);
    output = (copy1 & image_edge) | mask;
    */
}
```

#### pyrDown
```cpp
CV_EXPORTS_W void pyrDown( InputArray src, OutputArray dst,
                           const Size& dstsize = Size(), int borderType = BORDER_DEFAULT );
```
![opencv中的pyrDown()函数](https://img-blog.csdnimg.cn/20210320212319193.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)

#### bilateralFilter
```cpp
CV_EXPORTS_W void bilateralFilter( InputArray src, OutputArray dst, int d,
                                   double sigmaColor, double sigmaSpace,
                                   int borderType = BORDER_DEFAULT );
```
![opencv中的bilateralFilter()函数](https://img-blog.csdnimg.cn/20210320211218189.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)

#### pyrUp
```cpp
CV_EXPORTS_W void pyrUp( InputArray src, OutputArray dst,
                         const Size& dstsize = Size(), int borderType = BORDER_DEFAULT );
```

![opencv中的pyrUp()函数](https://img-blog.csdnimg.cn/20210320212740541.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
#### medianBlur
```cpp
CV_EXPORTS_W void medianBlur( InputArray src, OutputArray dst, int ksize );
```
![opencv中的medianBlur()函数](https://img-blog.csdnimg.cn/20210320214502594.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)


#### adaptiveThreshold
```cpp
CV_EXPORTS_W void adaptiveThreshold( InputArray src, OutputArray dst,
                                     double maxValue, int adaptiveMethod,
                                     int thresholdType, int blockSize, double C );
```
![opencv中的adaptiveThreshold()函数](https://img-blog.csdnimg.cn/20210320213504846.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
### 5.3.3 erode_plugin
```cpp
void ErodePlugin::edit(const cv::Mat &input, cv::Mat &output)
{
    erode(input, output, cv::Mat());
}
```
#### erode
```cpp
CV_EXPORTS_W void erode( InputArray src, OutputArray dst, InputArray kernel,
                         Point anchor = Point(-1,-1), int iterations = 1,
                         int borderType = BORDER_CONSTANT,
                         const Scalar& borderValue = morphologyDefaultBorderValue() );
```
![opencv中的erode()函数](https://img-blog.csdnimg.cn/20210320214834232.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
### 5.3.4 rotate_plugin
```cpp
void RotatePlugin::edit(const cv::Mat &input, cv::Mat &output)
{
    double angle = 45.0;
    double scale = 1.0;
    cv::Point2f center = cv::Point(input.cols/2, input.rows/2);
    cv::Mat rotateMatrix = cv::getRotationMatrix2D(center, angle, scale);

    cv::Mat result;
    cv::warpAffine(input, result,
        rotateMatrix, input.size(),
        cv::INTER_LINEAR, cv::BORDER_CONSTANT);
    output = result;
}
```
##### getRotationMatrix2D
```cpp
CV_EXPORTS Matx23d getRotationMatrix2D_(Point2f center, double angle, double scale);

inline
Mat getRotationMatrix2D(Point2f center, double angle, double scale)
{
    return Mat(getRotationMatrix2D_(center, angle, scale), true);
}
```
![opencv中的getRotationMatrix2D()函数](https://img-blog.csdnimg.cn/20210320215633652.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)
### 5.3.5 sharpen_plugin

```cpp
void SharpenPlugin::edit(const cv::Mat &input, cv::Mat &output)
{
    int intensity = 2;
    cv::Mat smoothed;
    cv::GaussianBlur(input, smoothed, cv::Size(9, 9), 0);
    output = input + (input - smoothed) * intensity;
}
```
#### GaussianBlur
```cpp
CV_EXPORTS_W void GaussianBlur( InputArray src, OutputArray dst, Size ksize,
                                double sigmaX, double sigmaY = 0,
                                int borderType = BORDER_DEFAULT );
```
![opencv中的GaussianBlur()函数](https://img-blog.csdnimg.cn/20210320220023642.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhbnR1Z3VpZ3V6aVBHSg==,size_16,color_FFFFFF,t_70)


