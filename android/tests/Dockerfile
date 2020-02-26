FROM truenightxyz/android:latest

LABEL maintainer="mike@truenight.xyz"

# Download system image
RUN sdkmanager "system-images;android-29;google_apis;x86"

# Create emulator
RUN echo no | avdmanager create avd --force -n emulator -k 'system-images;android-29;google_apis;x86'