---
title: Introduction
hide:
  - toc
---

<div class="hero" markdown>

# W4Studica

**2027 WPILib on the Studica VMX-pi.** A community project, currently in beta.

[Get started](guides/vmx-pi/vmx-pi-setup.md){ .md-button .md-button--primary }
[GitHub](https://github.com/W4Studica){ .md-button }

</div>

<div class="grid cards" markdown>

- :material-language-cpp: **Write C++ on your PC**

    Build with GradleRIO and deploy to the VMX-pi over the network with `./gradlew deploy`.

- :material-chip: **WPILib classes on VMX hardware**

    Digital I/O, analog input and encoders work through WPILib. Studica devices such as the Titan use Studica's API with W4Studica helper classes.

- :material-shield-check: **Titan safety**

    The enable guard turns the Titan off when the robot is disabled, E-stopped, or the program stops.

- :material-lan-connect: **Wired or Wi-Fi**

    Connect by cable or through the VMX-pi's own Wi-Fi hotspot, the way you would at a competition.

</div>

## Why we started

Studica has ended support for its WPILib 2020 environment. VMX-pi teams needed a way to use a newer WPILib release without staying on the old setup.

Instead of writing every hardware driver again, this project uses the driver code Studica uses with ROS 2 to connect VMX-pi hardware. Reusing that code reduces duplicate work and keeps device support together, making it easier to maintain. W4Studica connects those drivers to WPILib so teams can keep a familiar way to write and deploy robot code.

## How it works

Write and build C++ robot code on a PC, then deploy it to the VMX-pi with GradleRIO. On the VMX-pi, a W4Studica extension connects WPILib to the hardware drivers.

## Current status

!!! info "Beta, based on 2027.0.0-alpha-7"

    C++ build and deployment, digital I/O, analog input, encoders, and Titan control have been checked on a VMX-pi.

!!! warning "Not available yet"

    Some IMU behavior still needs verification. WPILib hardware support for PWM, DutyCycle, and I2C is not available yet. Java robot programs are not supported.

We are documenting what works and expanding support over time. W4Studica is a community project and is not an official Studica or WPILib distribution.
