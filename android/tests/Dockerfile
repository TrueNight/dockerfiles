FROM truenightxyz/android:latest

LABEL maintainer="mike@truenight.xyz"

# Libs for emulator
RUN sudo apt-get update && sudo apt-get install libpulse0:amd64 libnss3-dev libxcomposite1 libxcursor-dev \
    libasound2-dev

# Virtualization
RUN sudo apt-get install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virtinst libvirt-daemon virt-manager -y

ARG emulator_image="system-images;android-R;google_apis_playstore;x86_64"
# Download system image 
RUN sdkmanager $emulator_image
# Create emulator
RUN avdmanager create avd -n emulator -d pixel -k $emulator_image