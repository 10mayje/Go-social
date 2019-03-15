# Go-social

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/fbf9f8e1bb7b4d2cbb1ca569014ed45b)](https://app.codacy.com/app/shehand/Go-social?utm_source=github.com&utm_medium=referral&utm_content=shehand/Go-social&utm_campaign=Badge_Grade_Dashboard)

Community of today used to use mobile phones to make their life easier and community based mobile applications are famous among them. There are several kind of community based applications in use and most of them are relating to a specific domain. But core components have similar features. Address this issue and saving development time by introducing a common app template with customizable components for community based mobile applications, is the main purpose of this project.

## setup the project

> NOTE : If you don't have installed react-native yet use [this link](https://facebook.github.io/react-native/docs/getting-started) to install and configure react-native. **Make sure to use react-native cli rather than using expo cli**.


## Configure Go-social

*  clone the project

    `git clone https://github.com/scorelab/Go-social.git`

*  change the directory to the project folder

    `cd Go-social`

*  install the node modules with following command

    `npm install`
### configer the config.example.js file (IMPORTANT)

> Open the project in any text editor you would use. Open the `config.example.js` file in the `config` folder. And follow the following steps

*  Use [this link](https://console.firebase.google.com/u/0/) to **create a firebase** project for the Go-social application. It is free for everyone.

*  Use [this link](https://cloud.google.com/maps-platform/) to **generate google map api key** for the map view in G-social. This is not necessary. You can use the given api key. But it is not guaranteed that the given key will always work. It is better to have your own key. Enable all maps, routes, places in your key.

*  Now you need a **facebook app id** if you want to enable facebook login for Go-social. Use [this link](https://developers.facebook.com/) for that. And make sure to enable both email/password and facebook sign in method in firebase/

So place you firebase details and google map api key in **config.example.js** file and **rename it** to **config.js**.

*In order to work google map and facebook login you have to do some extra works. Follow these steps.*

1.  find the file name `AndroidManifest.xml` which is located in `android/app/src/main` path. Place you **google map api key** in there.

    > Ex : <meta-data
        android:name="com.google.android.geo.API_KEY"
        android:value=**"AIzaSyDmwJddIPTcALyZtj7p9mFFlkMvpMkati8"**/>
        
1.  Find the file name as `strings.xml` located in  `android/app/src/main/res/values`. Place your **facebook app id** in there.

    > Ex: <string name="facebook_app_id">**2349388348405699**</string>
        
So now your are ready to run Go-social.
## Run Go-social



*  run the app 

    `react-native run-android`