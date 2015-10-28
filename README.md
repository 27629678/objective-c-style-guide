### Objective-C Style Guide

[DropBox](https://dl.dropboxusercontent.com/s/5utnlwhr18ax05c/style-guide.html?dl=0)

-----------

Always use NSCAsserts for assertions

We will use NSCAsserts instead of asserts or NSAsserts for doing assertions.

> Reasoning: NSAssert is a macro that actually internally references self. In other words, when used in a block, you may unintentionally cause the block to retain self. We could alternatively use NSAsserts in cases where we are actually okay with using self, but since NSAssert and NSCAssert do roughly equivalent things (they both include file name, method name + line number, though NSCAssert does not print the actually type of self), we will keep things simple and always use NSCAssert.

------------

Never convert general integral values / object pointers to BOOL

Common mistake: casting the length of an array into a BOOL

> Reasoning: even if the number is > 0, it may still cast to NO if the low bits are 0.

[Google](http://google-styleguide.googlecode.com/svn/trunk/objcguide.xml)

[Apple Coding Guide for Cocoa](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)
