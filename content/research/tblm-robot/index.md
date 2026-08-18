---
title: Automated tBLM Preparation Robot
summary: A custom liquid-handling platform that automates the solvent-exchange protocol for forming tethered bilayer lipid membranes across a full 96-well plate.
date: 2026-08-18
draft: true
---

**A custom liquid-handling platform for high-throughput tethered bilayer lipid membrane formation**

## Overview

Tethered bilayer lipid membranes (tBLMs) are robust, long-lived model membranes formed by anchoring a lipid bilayer to a gold electrode via synthetic tethering molecules. Unlike conventional black lipid membranes, which typically survive only minutes to hours, tBLMs remain intact for months — making them a powerful platform for studying ion channels, membrane proteins, and peptide-membrane interactions by AC impedance spectroscopy.

Historically, tBLM formation has relied on manual pipetting: a timed solvent-exchange protocol in which an ethanolic lipid solution is deposited into each well, incubated for a fixed period, and then exchanged for aqueous buffer without ever letting the membrane dry out. This works well at small scale but becomes a bottleneck when scaling to a 96-well plate format.

This project develops a purpose-built robot that automates the entire solvent-exchange protocol across a full 96-well plate, replacing manual pipetting with a programmable, repeatable process.

## The client & collaboration

The project is being delivered for **Charles Cranfield** (University of Technology Sydney / SDx Tethered Membranes Pty Ltd), whose lab pioneered the tBLM solvent-exchange method described in Cranfield et al. (2015), *"The Assembly and Use of Tethered Bilayer Lipid Membranes (tBLMs)"*, *Methods in Membrane Lipids*, Methods in Molecular Biology vol. 1232. The robot is being built to work with a custom 96-well electrode-plate device developed by Surgical Diagnostics Pty Ltd, extending the original 6-channel benchtop format to a full microplate scale suitable for higher-throughput screening.

## Engineering approach

The platform is built around a modified Cartesian 3D-printer motion system (Creality Ender 3 chassis) running **Klipper firmware** on a BTT Manta M8P controller with a CB1 compute module. Rather than syringe-pump dispensing, the design centres on a repurposed **Gilson Microman positive-displacement pipette**, mounted directly on the print-head carriage and driven by a dedicated stepper axis:

- **XYZ gantry** — positions the pipette tip precisely over any of the 96 wells, plus three reagent reservoirs and a tip rack, using a custom-designed plate holder and locating fixture.
- **Piston axis** — a dedicated stepper drives the pipette plunger for aspirate, dispense, and tip-eject actions, controlled through Klipper as a standard extruder axis.
- **Custom G-code macro suite** — implements the full protocol: tip pickup, aspiration, timed well-by-well dispensing, controlled incubation windows, buffer exchange, rinse cycles, and tip disposal — all without a laptop dependency once deployed.
- **Touchscreen interface** — an onboard display and (in progress) a simplified control menu are being developed so the instrument can run as a standalone lab device.

A key engineering challenge has been achieving reliable **droplet release** from the pipette tip into each well: the tip geometry is too wide to reach the well floor in the compact 96-well format, so a "pendant-drop touchdown" technique — a slow, controlled retract that lets surface wetting overcome tip adhesion — is being used in place of the operator's manual touch-off technique.

## Current status

- Core motion hardware (XYZ gantry, piston axis, pipette mount, plate holder, reagent and tip-rack layout) is built and calibrated.
- The Klipper macro suite is substantially complete and under active refinement, with current work focused on reliable, drip-free dispensing into the 96-well format.
- Remaining work includes finalising dispense parameters, audio/status feedback, a physical touchscreen enclosure, and a simplified on-device control menu — all aimed at making the instrument fully standalone for routine use.

## Why it matters

By automating a protocol that is currently manual, timing-sensitive, and difficult to scale, this project aims to turn tBLM formation from a low-throughput technique into one compatible with routine screening — supporting applications from ion-channel biosensing to membrane-protein and peptide research, and contributing to a translational commercialisation pathway for the underlying platform.

---

*Prototype development led by Alexander Mason (University of Wollongong) for Charles Cranfield (UTS / SDx Tethered Membranes Pty Ltd).*
