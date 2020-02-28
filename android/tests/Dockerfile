FROM truenightxyz/android:latest

LABEL maintainer="mike@truenight.xyz"

RUN apt-get update && apt-get install -y libpulse0:i386

# Download system image
RUN sdkmanager "system-images;android-29;google_apis;x86"

# Create emulator
RUN echo no | avdmanager create avd --force -n emulator -k 'system-images;android-29;google_apis;x86'