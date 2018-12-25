# Localize-Key
A convenient tool for editing local keys in iOS development

**中文介绍可以看这里：**
https://www.jianshu.com/p/087260ea13a0

![img](https://github.com/CoconutGZ/Localize-Key/blob/master/20181224-164023.png)



Function introduction
-------------------
- **checkout**: Powerful synchronization function, export. h file or. swift file from. strings file.
- **insert**: Add a new key to. string file and output file.

Installation
--------------------
Download the installation package(`Localize Key.dmg`) in the project and install it on the computer.

product
----------------------
swift project. Example：
``` swift
/**#LocalizeKey*/
enum LocalizeKey: String {

/*#keys-Localize*/
	/// Invalid key. Never use
	case invalidKey = "invalidKey"
	case buttonTitle = "buttonTitle"
	case toolbarTitle1 = "toolbarTitle1"
	//case toolbarTitle2 = "toolbarTitle2"
	//case toolbarTitle3 = "toolbarTitle3"
	case toolbarTitle4 = "toolbarTitle4"
	case haha = "haha"
/*#end-keys-Localize*/


	/**#home*/
	enum home: String {

	/*#keys-home*/
			case title = "home_title"
			//case titleLabel = "home_titleLabel"
			case wow = "home_wow"
	/*#end-keys-home*/

	/*#end-home*/
	}


	/**#my*/
	enum my: String {

	/*#keys-my*/
			case button = "my_button"
			//case button3 = "my_button3"
			case titleLabel = "my_titleLabel"
	/*#end-keys-my*/

	/*#end-my*/
	}

/*#end-Localize*/
}

```

Objective-C project. Example：
``` Objective-C

/*#Localize-swift*/
	static NSString * const LocalizeKey_buttonTitle = @"buttonTitle";
	static NSString * const LocalizeKey_toolbarTitle1 = @"toolbarTitle1";
	//static NSString * const LocalizeKey_toolbarTitle2 = @"toolbarTitle2";
	//static NSString * const LocalizeKey_toolbarTitle3 = @"toolbarTitle3";
	static NSString * const LocalizeKey_toolbarTitle4 = @"toolbarTitle4";
	static NSString * const LocalizeKey_haha = @"haha";
	/// 分享按钮的文案
	static NSString * const LocalizeKey_shareButtonTitle = @"shareButtonTitle";
/*#end-Localize*/


/*#subset-home*/
	static NSString * const LocalizeKey_home_title = @"home_title";
	static NSString * const LocalizeKey_home_titleLabel = @"home_titleLabel";
	static NSString * const LocalizeKey_home_wow = @"home_wow";
/*#end-home*/


/*#subset-my*/
	//static NSString * const LocalizeKey_my_button = @"my_button";
	//static NSString * const LocalizeKey_my_button3 = @"my_button3";
	static NSString * const LocalizeKey_my_titleLabel = @"my_titleLabel";
/*#end-my*/

```

Usage
------------------
swift project. Example：
``` swift
	let str = NSLocalizedString(LocalizeKey.home.title.rawValue, comment: "")
```

Objective-C project. Example：
``` Objective-C
	NSString * str = NSLocalizedString(LocalizeKey_home_title, @"");
```
