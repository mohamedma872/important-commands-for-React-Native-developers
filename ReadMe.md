
### **1. Environment Setup Commands**
- **Check Node version**:
  ```bash
  node -v
  ```
- **Check npm version**:
  ```bash
  npm -v
  ```
- **Install Yarn (alternative to npm)**:
  ```bash
  npm install -g yarn
  ```
- **Install Expo CLI globally**:
  ```bash
  npm install -g expo-cli
  ```
- **Install React Native CLI globally**:
  ```bash
  npm install -g react-native-cli
  ```

---

### **2. Project Initialization Commands**
- **Create a React Native project with React Native CLI**:
  ```bash
  npx react-native init MyProject
  ```
- **Create a React Native project with Expo CLI**:
  ```bash
  npx create-expo-app MyProject
  ```

---

### **3. Running the Project**
- **Run on Android emulator/device**:
  ```bash
  npx react-native run-android
  ```
- **Run on iOS simulator/device**:
  ```bash
  npx react-native run-ios
  ```
- **Start the Metro bundler**:
  ```bash
  npx react-native start
  ```
- **Run an Expo project**:
  ```bash
  npm start
  # Or:
  expo start
  ```

---

### **4. Dependency Management**
- **Install a new dependency**:
  ```bash
  npm install <package-name>
  ```
  OR
  ```bash
  yarn add <package-name>
  ```
- **Install a dependency with a specific version**:
  ```bash
  npm install <package-name>@<version>
  ```
- **Remove a dependency**:
  ```bash
  npm uninstall <package-name>
  ```
  OR
  ```bash
  yarn remove <package-name>
  ```

---

### **5. Linking Native Modules**
- **For older React Native versions (pre-0.60)**:
  ```bash
  react-native link <package-name>
  ```
- **Unlink a package (if necessary)**:
  ```bash
  react-native unlink <package-name>
  ```

---

### **6. CocoaPods for iOS**
- **Navigate to the iOS folder**:
  ```bash
  cd ios
  ```
- **Install iOS dependencies**:
  ```bash
  pod install
  ```
- **Update CocoaPods repository**:
  ```bash
  pod repo update
  ```
- **Clean and reinstall Pods**:
  ```bash
  pod deintegrate
  pod install
  ```

---

### **7. Debugging and Testing**
- **Enable debugging** (e.g., Chrome Debugger or React DevTools):
  Press `Cmd + M` (Android) or `Cmd + D` (iOS) in the simulator/emulator and select "Debug".
- **Run Jest unit tests**:
  ```bash
  npm test
  ```
- **Run ESLint to check code quality**:
  ```bash
  npx eslint .
  ```

---

### **8. Version Management**
- **Upgrade React Native version**:
  ```bash
  npx react-native upgrade
  ```
- **Check React Native version**:
  ```bash
  npx react-native --version
  ```

---

### **9. Common Android Commands**
- **Kill all running Metro processes**:
  ```bash
  kill -9 $(lsof -t -i:8081)
  ```
- **Clear Gradle build cache**:
  ```bash
  cd android && ./gradlew clean
  ```
- **Rebuild Android project**:
  ```bash
  cd android && ./gradlew assembleDebug
  ```

---

### **10. Common iOS Commands**
- **Clean Xcode build folder**:
  ```bash
  rm -rf ~/Library/Developer/Xcode/DerivedData
  ```
- **Rebuild iOS project**:
  ```bash
  xcodebuild clean build
  ```

---

### **11. Clear Caches**
- **Clear npm cache**:
  ```bash
  npm cache clean --force
  ```
- **Clear Yarn cache**:
  ```bash
  yarn cache clean
  ```
- **Clear React Native cache**:
  ```bash
  npx react-native-clean-project
  ```

---

### **12. Building the App**
- **Build APK (Android)**:
  ```bash
  cd android && ./gradlew assembleRelease
  ```
- **Build iOS app**:
  Open the iOS project in Xcode and archive it via `Product > Archive`.

---

### **13. Expo Commands**
- **Eject from Expo**:
  ```bash
  expo eject
  ```
- **Build an app for production**:
  ```bash
  expo build:android
  expo build:ios
  ```

---

### **14. Linting and Formatting**
- **Run Prettier**:
  ```bash
  npx prettier --write .
  ```
- **Run ESLint**:
  ```bash
  npx eslint .
  ```

---

### **15. Performance Optimization**
- **Enable Hermes (for Android)**:
  Edit `android/app/build.gradle`:
  ```gradle
  enableHermes: true
  ```
  Then rebuild the project:
  ```bash
  cd android && ./gradlew clean && npx react-native run-android
  ```

---

### **16. Additional Tools**
- **React Native Debugger**:
  Start React Native Debugger and connect it to your app:
  ```bash
  open "rndebugger://set-debugger-loc?host=localhost&port=8081"
  ```
- **Check the list of connected devices (adb)**:
  ```bash
  adb devices
  ```

---

### **17. Clean and Reset Project**
- **Reset all React Native caches**:
  ```bash
  watchman watch-del-all
  rm -rf node_modules && npm install
  npm start --reset-cache
  ```

---

### **18. Useful Development Shortcuts**
- **Open Android emulator**:
  ```bash
  emulator -avd <emulator-name>
  ```
- **Open iOS simulator**:
  ```bash
  open -a Simulator
  ```

---

### **1. Managing Derived Data (iOS Development)**
- **Delete Xcode Derived Data**:
  ```bash
  rm -rf ~/Library/Developer/Xcode/DerivedData
  ```
- **Delete specific Derived Data for a project**:
  ```bash
  rm -rf ~/Library/Developer/Xcode/DerivedData/<YourProjectName>
  ```
- **View Derived Data path in Finder**:
  ```bash
  open ~/Library/Developer/Xcode/DerivedData
  ```

---

### **2. Node Version Manager (NVM)**
NVM is essential for managing multiple Node.js versions, especially for React Native developers.

#### **Install NVM**
- **For macOS/Linux**:
  ```bash
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
  ```
  Then reload your shell:
  ```bash
  source ~/.bashrc
  # or for macOS:
  source ~/.zshrc
  ```

#### **Common NVM Commands**
- **Check NVM version**:
  ```bash
  nvm --version
  ```
- **Install a specific Node.js version**:
  ```bash
  nvm install <version>
  # Example:
  nvm install 16
  ```
- **Use a specific Node.js version**:
  ```bash
  nvm use <version>
  # Example:
  nvm use 16
  ```
- **List installed Node.js versions**:
  ```bash
  nvm list
  ```
- **List all available Node.js versions**:
  ```bash
  nvm ls-remote
  ```
- **Set default Node.js version**:
  ```bash
  nvm alias default <version>
  ```
- **Uninstall a Node.js version**:
  ```bash
  nvm uninstall <version>
  ```

---

### **3. SD Card Management**
SD card management might be necessary for Android emulator setups or storing app data.

#### **Format and Manage SD Card (macOS/Linux)**
- **List all storage devices**:
  ```bash
  diskutil list
  ```
- **Unmount the SD card**:
  ```bash
  diskutil unmountDisk /dev/diskX
  # Replace `diskX` with the actual identifier of the SD card.
  ```
- **Format SD card (FAT32)**:
  ```bash
  diskutil eraseDisk FAT32 SDCARD MBRFormat /dev/diskX
  # Replace `diskX` with the actual identifier.
  ```
- **Eject the SD card**:
  ```bash
  diskutil eject /dev/diskX
  ```

#### **SD Card Setup for Android Emulator**
- **Create a new SD card image for the Android emulator**:
  ```bash
  mksdcard -l my_sdcard 512M my_sdcard.img
  ```
  - Replace `512M` with the desired size (e.g., `1G` for 1 GB).
- **Attach SD card image to an emulator**:
  Edit your AVD (Android Virtual Device) configuration and specify the path to `my_sdcard.img`.

#### **Windows Commands for SD Cards**
- **List drives**:
  ```cmd
  wmic logicaldisk get name
  ```
- **Format SD card**:
  ```cmd
  format X: /FS:FAT32
  ```
  - Replace `X:` with the drive letter of your SD card.

---

### **4. Miscellaneous Commands**

#### **General Cleanup Commands**
- **Clear npm cache**:
  ```bash
  npm cache clean --force
  ```
- **Clear yarn cache**:
  ```bash
  yarn cache clean
  ```
- **Clear React Native cache**:
  ```bash
  watchman watch-del-all
  rm -rf node_modules
  npm start --reset-cache
  ```

#### **Other Useful Commands**
- **Kill processes running on a port (e.g., Metro bundler on port 8081)**:
  ```bash
  kill -9 $(lsof -t -i:8081)
  ```
- **List all running Android emulators**:
  ```bash
  adb devices
  ```
- **Open Android AVD Manager**:
  ```bash
  emulator -avd
  ```
- **Open iOS Simulator**:
  ```bash
  open -a Simulator
  ```


### Setting Up React Native and Using `.zshrc` File on macOS (or Linux)

Here’s a detailed guide for setting up React Native and managing your environment using the `.zshrc` file.

---

### **1. React Native Setup**

#### **Step 1: Install Required Dependencies**
1. **Install Homebrew** (macOS):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install Node.js and Watchman**:
   ```bash
   brew install node
   brew install watchman
   ```

3. **Install JDK (Java Development Kit)**:
   React Native requires JDK for Android development. Install it using Homebrew:
   ```bash
   brew install --cask adoptopenjdk
   ```

4. **Install Android Studio**:
   Download and install [Android Studio](https://developer.android.com/studio). After installation:
   - Open **Android Studio**.
   - Go to **SDK Manager** → **SDK Platforms** and install:
     - Android 12 (API 31) or later.
     - Android SDK Tools.
   - Go to **SDK Tools** and install:
     - Android SDK Build-Tools.
     - Android Emulator.
     - Android Platform-Tools.
     - Intel HAXM or Android Emulator Hypervisor Driver (for hardware acceleration).

---

#### **Step 2: Install React Native CLI**
You can either use **React Native CLI** or **Expo CLI**. For a full native experience, we’ll focus on React Native CLI:

Install React Native CLI globally:
```bash
npm install -g react-native-cli
```

---

#### **Step 3: Create a New React Native Project**
```bash
npx react-native init MyReactNativeApp
cd MyReactNativeApp
```

---

#### **Step 4: Run the Application**
1. **Run on Android Emulator/Device**:
   ```bash
   npx react-native run-android
   ```

2. **Run on iOS Simulator** (macOS only):
   ```bash
   npx react-native run-ios
   ```

3. **Start Metro Bundler** (if it doesn’t start automatically):
   ```bash
   npx react-native start
   ```

---

### **2. Configure the `.zshrc` File**

The `.zshrc` file is used to configure your shell environment when using **Zsh** (default shell on macOS).

#### **Step 1: Locate or Create the `.zshrc` File**
- Open your terminal and locate the `.zshrc` file in your home directory:
  ```bash
  ls -a ~
  ```
- If it doesn’t exist, create it:
  ```bash
  touch ~/.zshrc
  ```

#### **Step 2: Open `.zshrc` for Editing**
Use your preferred text editor (e.g., `nano`, `vim`, or `code`):
```bash
nano ~/.zshrc
```

#### **Step 3: Add Environment Variables**
Add the following configurations for React Native, Node.js, and Android SDK:

```bash
# Node.js and NVM configuration
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # Load nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # Load nvm bash_completion

# Add Android SDK to PATH
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$ANDROID_HOME/platform-tools:$PATH

# Java Home for Android
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH=$JAVA_HOME/bin:$PATH

# Alias for clearing Metro cache
alias react-native-clear="watchman watch-del-all && rm -rf $TMPDIR/react-* && npm start --reset-cache"
```

#### **Step 4: Apply Changes**
Reload the `.zshrc` file to apply the changes:
```bash
source ~/.zshrc
```

---

### **3. Verify Setup**

#### **Check Node and NPM**
```bash
node -v
npm -v
```

#### **Check Android SDK Configuration**
```bash
echo $ANDROID_HOME
```

#### **Check Java Version**
```bash
java -version
```

---

### **4. Useful `.zshrc` Aliases for React Native Developers**
Here are some useful aliases to make your workflow easier:
```bash
# Open Android emulator
alias android-emulator="~/Library/Android/sdk/emulator/emulator -list-avds && ~/Library/Android/sdk/emulator/emulator -avd"

# Clean React Native project
alias react-native-clean="watchman watch-del-all && rm -rf node_modules && npm install && npm start --reset-cache"

# Start Metro Bundler
alias metro-start="npx react-native start"

# Run iOS project
alias ios-run="npx react-native run-ios"

# Run Android project
alias android-run="npx react-native run-android"
```

Reload `.zshrc` after adding these:
```bash
source ~/.zshrc
```

---

### **5. Troubleshooting**

#### **Error: Command Not Found**
If you encounter issues like `nvm` or `react-native` not being recognized:
1. Make sure the environment variables in `.zshrc` are correct.
2. Restart the terminal or reload `.zshrc`:
   ```bash
   source ~/.zshrc
   ```

---

