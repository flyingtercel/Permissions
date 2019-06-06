# RxPermissions

```
    申明：项目来自于 https://github.com/tbruyelle/RxPermissions
    因为在接入mpaas框架中使用的时候，项目必须继承框架中的BaseActivity,而BaseActivity
    的顶层父布局是app包下的Activity，Fragment也只能使用app包下的Fragment，所以我们在使用的时候，
    必须传入app包下的Activity或Fragment对象，但是RxPermissions权限申请
    只能传入在v4包中的FragmentActivity或Fragment对象，所以
    才对RxPermissions重新打包编译，生成依赖，在项目中使用，也方便以后在接入mpaas框架的时候能快速依赖。

    使用方式与https://github.com/tbruyelle/RxPermissions中完全一致，只是传递的Activity对象稍有区别。

```
## 在项目的builder.gradle中
```
allprojects {
	repositories {
			...
		maven { url 'https://jitpack.io' }
	}
}
```
## 在module的builder.gradle中
```
    dependencies {
    	implementation 'com.github.flyingtercel:RxPermissions:1.0.2'
    }
```