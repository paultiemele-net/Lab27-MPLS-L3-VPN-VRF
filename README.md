# Lab27-MPLS-L3-VPN-VRF
This repository contains an advanced MPLS Layer 3 VPN lab demonstrating how VRF, MPLS, OSPF, and MP-BGP are used together to provide traffic separation and controlled connectivity between multiple customer sites across a shared service provider backbone.

Lab Overview

The topology simulates a service provider MPLS core with multiple Provider Edge (PE) and Provider (P) routers.
Each customer site is placed into a dedicated VRF, ensuring traffic isolation while allowing selective route sharing using Route Targets (RTs).

The goal of the lab is to achieve the following communication paths:

R1 ↔ R7

R2 ↔ R8

R3 ↔ R9

while using a single MPLS backbone.

Key Technologies Used

MPLS (Label Switching)

VRF (Virtual Routing and Forwarding)

MP-BGP (VPNv4) for VPN route exchange

OSPF as the IGP inside the provider core

Static routing at the customer edge

Route Distinguisher (RD) and Route Targets (RT)

Dynamic NAT, Static NAT, and PAT (Internet access extension)

Architecture Details

Customer Edge Routers (CE): R1, R2, R3, R7, R8, R9

Provider Edge Routers (PE): R4 and R6

Provider Core Router (P): R5

IGP: OSPF running inside the MPLS core

BGP AS: 100 (Service Provider)

VRF Design

VRF R1-R7 → Shared access between R1 and R7 (with optional inter-VRF communication)

VRF R2-R8 → Isolated communication between R2 and R8

VRF R3-R9 → Isolated communication between R3 and R9

Each VRF uses:

Unique Route Distinguisher (RD)

Controlled Route Target (RT) import/export policies

Learning Objectives

Understand how VRFs isolate customer routing tables

Configure MPLS in a service provider core

Use MP-BGP (VPNv4) to transport customer routes

Control inter-VRF communication using Route Targets

Combine MPLS VPN with NAT for Internet access

Gain hands-on experience with real ISP-style architectures
