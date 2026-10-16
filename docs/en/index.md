---
title: Introduction
---

# W4Studica

W4Studica is a community project that brings 2027 WPILib to the Studica VMX-pi. The project is currently in beta.

## Why we started

Studica has ended support for its WPILib 2020 environment. VMX-pi teams needed a way to use a newer WPILib release without staying on the old setup.

Instead of writing every hardware driver again, this project uses the driver code Studica uses with ROS 2 to connect VMX-pi hardware. Reusing that code reduces duplicate work and keeps device support together, making it easier to maintain. W4Studica connects those drivers to WPILib so teams can keep a familiar way to write and deploy robot code.

## How it works

Write and build C++ robot code on a PC, then deploy it to the VMX-pi with GradleRIO. On the VMX-pi, a W4Studica extension connects WPILib to the hardware drivers.

Digital I/O, analog input, and encoders can be used through WPILib. Studica devices such as the Titan use Studica's API together with W4Studica helper classes.

## Current status

W4Studica is in beta, based on **2027.0.0-alpha-7**. C++ build and deployment, digital I/O, analog input, encoders, and Titan control have been checked on a VMX-pi.

Some IMU behavior still needs verification. WPILib hardware support for PWM, DutyCycle, and I2C is not available yet. We are documenting what works and expanding support over time.

W4Studica is a community project and is not an official Studica or WPILib distribution.
