# Cisco-IOS-XR-MTU
IOS XR MTU Explained

In our first IOS XR testing we have had a ton of weird issues:
- Errors on ports
- Discards/Drops on ports (Drops for unrecognized upper-level protocol)
- Packet drops

This is all due to the fact that IOS XR manages MTU differently than IOS XE and trunk port settings on the switch facing the IOS XR device.

To avoid the drops, on the switch facing the IOS XR device, only allow VLANs that the IOS XR device is part of (has a do1q interface enabled for
ie: switchport trunk allow vlan 1,3-100
