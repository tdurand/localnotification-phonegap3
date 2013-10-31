#Installation

## IOS

NOT IMPLEMENTED YET, feel free to send pull request

## Android

*NB: the java code can be improved, this version still require a lot to do manually, i'm open to pull request*

Install via phonegap 3 CLI or plugman: 

    phonegap local plugin add https://github.com/tdurand/localnotification-phonegap3
    
Line 14 , remplace _PACKAGE_ by the correct import :
    
    import _PACKAGE_.R;
    
Line 67 , remplace by your mainactivity:

    Intent notificationIntent = new Intent(context, _PACKAGE_._MAINACTIVITY_.class);
    
Be sure AlarmReceiver.java around line 67 where R.drawable.ic_launcher is referenced so it matches an icon in your project

    final Notification notification = new Notification(R.drawable.ic_launcher, tickerText,
                System.currentTimeMillis());
