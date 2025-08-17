# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.


## Other commands and notes

npm start


npx expo login

npx create-expo-app <app name>

npm run reset-project

## EAS (building mobile project)
## ---------------------
eas init
eas build --platform android

## Appwrite
git clone https://github.com/appwrite/starter-for-react-native
cd starter-for-react-native


EXPO_PUBLIC_APPWRITE_PROJECT_ID=temp-notes-app
EXPO_PUBLIC_APPWRITE_PROJECT_NAME="Assab temp Notes app"
EXPO_PUBLIC_APPWRITE_ENDPOINT=https://fra.cloud.appwrite.io/v1

3. Run the app on a connected device or simulator using npm install followed by npm run android, then click the Send a ping button to verify the setup.

admin1@test.com | Password1

## Using an emulator

Yes — you’ll need to run npx react-native run-android (after starting your Android emulator) so Metro can send your app’s JavaScript to it.

Here’s the full walkthrough:

1️⃣ Install Android Studio & Setup SDK

If you haven’t already:

Install Android Studio (includes emulator and SDK tools).

In Android Studio → Settings → Appearance & Behavior → System Settings → Android SDK:

Install the Android SDK Platform for the Android version you want.

Install Android SDK Build-Tools and Platform Tools.

Add SDK tools to your system PATH (so adb works). Typically:

C:\Users\<YourName>\AppData\Local\Android\Sdk\platform-tools


or on Mac/Linux:

~/Library/Android/sdk/platform-tools

2️⃣ Start an Android Emulator

Open Android Studio → Tools → Device Manager.

Create a Virtual Device (Pixel 6 or similar) with a supported API level (React Native usually works well with API 33 or 34).

Start the emulator — wait until it’s fully booted.

3️⃣ Start Metro Bundler

In your React Native project folder:

npm start


or

npx react-native start


This is the Metro server you saw at localhost:8081.

4️⃣ Build and Install the App

With Metro running in a separate terminal, open a new terminal window and run:

npx react-native run-android


What this does:

Compiles the native Android code.

Installs the APK on the emulator.

Connects the app to Metro bundler for live reload.

5️⃣ Verify & Use

Your app should open automatically in the emulator.

Any JavaScript changes will reload instantly via Metro.

✅ Pro Tip:
If you want to skip manually starting Metro, you can just run:

npx react-native run-android


It will:

Start Metro automatically (if not running).

Build & install the app.

If you want, I can also give you ADB commands to check that your emulator is detected before running the build — that way we avoid the classic "No connected devices" error.
Do you want me to include that check?

You said:
yes
ChatGPT said:

Alright — here’s how to check that your emulator is properly detected before running npx react-native run-android.

ADB Device Check Steps
1️⃣ Ensure ADB is on Your PATH

If you installed Android Studio and SDK, adb (Android Debug Bridge) should be in:

Windows

C:\Users\<YourName>\AppData\Local\Android\Sdk\platform-tools


Mac/Linux

~/Library/Android/sdk/platform-tools


Make sure this folder is in your PATH so you can run adb from any terminal.

2️⃣ Start Your Emulator

Open Android Studio → Tools → Device Manager → start the device.

Or start it via command line:

emulator -avd <Your_AVD_Name>

3️⃣ Check for Connected Devices

In a terminal:

adb devices


You should see something like:

List of devices attached
emulator-5554   device


If it says offline, unauthorized, or the list is empty:

Make sure the emulator is fully booted.

Restart ADB:

adb kill-server
adb start-server
adb devices

4️⃣ Run Your App

Once the emulator shows as a device, run:

npx react-native run-android


This will:

Start Metro (if not already running).

Build & install your app on the emulator.

Connect to Metro for live reload.

💡 Quick One-Liner
If you want to do everything in one go:

adb devices && npx react-native run-android


That way, if ADB can’t see the device, you’ll know before the build even starts.

If you want, I can also give you a diagram of how Metro, ADB, and the emulator interact so the whole process is crystal clear. That way, you’ll understand why each step matters.
