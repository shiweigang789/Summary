[JNI开发流程与引用数据类型的处理](https://www.jianshu.com/p/3f7efe54a0ce)

[FFmpeg 5.0 编译 so 库](https://juejin.cn/post/7101453781107703815)



javah 生成头文件
javah -classpath . -jni com.swg.ndk.Crypto


日志宏定义
#ifndef ANDROID_LOG
#define ANDROID_LOG

#include <android/log.h>

#define TAG "Crypto"

static bool debug = true;

void setDebug(bool isDebug) {
    debug = isDebug;
}

#define LOGV(...) if (debug) __android_log_print(ANDROID_LOG_VERBOSE, TAG, __VA_ARGS__)

#endif
