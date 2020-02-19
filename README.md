# Facebook-app-launch-by-button-click
Launch facebook app using OnClickListener() on Android

##Follow those Step::
---

***Step 1:***
Create a Project first in Android Studio.

***Step 2:***
Create a below method-
```
public static Intent hitApp(Context context) {

    try {
        context.getPackageManager()
                .getPackageInfo("com.facebook.katana", 0);
        return new Intent(Intent.ACTION_VIEW,
                Uri.parse("fb://profile/100009032309681"));
            //For FB Page    Uri.parse("fb://page/100009032309681"));
    } catch (Exception e){

        return new Intent(Intent.ACTION_VIEW,
                Uri.parse("http://www.facebook.com/alam5238"));
    }


}
```
***Step 3:***
call that `hitApp()` method by `OnClickListener()` in your button using this code.

```
  Intent facebookIntent = openFacebook(MainActivity.this);
  startActivity(facebookIntent);
```

***Step 4:***
Build, Run and Enjoy!!


