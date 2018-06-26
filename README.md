# OnboardScreen
OnBoard / Introduction Screen App

It is simple Introduction Screen app which can be integrated with your android project easily. In this app it is having 3 pages/screens which provide general information which can be edited in strings.xml file.

After integration if you want it to be displayed at first run only then you've to use shared preference code.

You've to place it in onCreate method MainActivity

In this MainActivity is OnBoard Screen Activity and FirstLauch is next Activity you want to display.

```
Boolean isFirstRun = getSharedPreferences("PREFERENCE", MODE_PRIVATE)
            .getBoolean("isFirstRun", true);

    if (isFirstRun) {
        //show start activity

        startActivity(new Intent(MainActivity.this, FirstLaunch.class));
        Toast.makeText(MainActivity.this, "First Run", Toast.LENGTH_LONG)
                .show();
    }

       getSharedPreferences("PREFERENCE", MODE_PRIVATE).edit()
                .putBoolean("isFirstRun", false).commit();
  ```

It is built to work on Android 5.1 & above

Technologies used: Android, Java, XML

IDE: Android Studio 3.1.1
