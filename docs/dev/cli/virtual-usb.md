---
id: virtual-usb
title: Virtual USB CLI Reference
sidebar_label: General Usage
---

Virtual USB (vUSB) is an app debugging tool that simulates connecting a Sauce Labs real device directly to your local machine with a USB cable. This section outlines the required and optional parameters for the vUSB client test runner.

## What You'll Need

* Your mobile app file.
* Have the vUSB client downloaded and installed.
* Prior to using vUSB, navigate (`cd`) to the specific folder directory on your local machine where you downloaded and placed your Virtual USB client (`virtual-usb-client.jar`).

## CLI Structure

The command line structure for all vUSB requests is as follows: `<main class> [options] [command] [command options]`.

## `--help` Option

You can view all vUSB options by running the `--help` flag:
```java
java -jar virtual-usb-client.jar --help
```

For user cases and step-by-step vUSB instructions, see [Virtual USB Testing on Real Mobile Devices](/mobile-apps/virtual-usb).
