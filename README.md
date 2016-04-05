Showcases the 'feature' that causes Android to upscale bitmaps to native resolution unless it is
put in drawable-nodpi.

On my Nexus 6P the hdpiExample uses 63 mb RAM, while nodpiExample 'only' uses 28 mb. The only
difference is what folder the drawable is placed in.

It only gets worse if you have a viewpager with n views that all have high resolution backgrounds.
Unknowingly you will crash the app for a lot of users due to java.lang.OutOfMemoryError, just
because you use high resolution background images and placed them in the wrong folder.