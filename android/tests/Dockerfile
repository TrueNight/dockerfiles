FROM truenightxyz/android:latest

LABEL maintainer="mike@truenight.xyz"

# Download system image
sdkmanager "system-images;android-29;google_apis;x86"

# Create emulator
avdmanager create avd -n emulator-29 -k "system-images;android-29;google_apis;x86"