# udev-hid-bpf
This repository is to be used with the hid-bpf tool found at
https://gitlab.freedesktop.org/libevdev/udev-hid-bpf
as that is how the files can be installed on a linux system.

The first file here is a fix for the Thrustmaster TCA Yoke Boeing joystick.
This joystick by default shows a "phantom" axis on linux system. A phantom axis is one where it is seen on the system. 
But a physical control can never be assigned to it.

This file therefore modifies the hid descriptor to remove this phantom axis and matches all physical control to axes.

A further fix in the file is to change the Rz axis  to a throttle. This has no impact on the behaviour of the joystick.

