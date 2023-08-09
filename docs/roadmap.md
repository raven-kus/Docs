---
description: Roadmap To v0.1.0
---

# Roadmap

#### Website

Ya... Let's not talk about it, it's bad currently, is mostly there just to hold the blog and link to the documentation sites. Put simply... it needs to be replaced. Anyone interested in helping with this, or giving the Admin Dashboard a face life, please reach out in [Discord](https://discord.gg/S85mDy2qxE)

#### Forge Cloud

Once v0.1.0 is available the plan is to launch a service for hosting multiple Forge4Flow-Core environments with central management dashboard similar to Forge Manager

#### Forge Manager

* [ ] Admin Dashboard
* [x] Verify/Install Docker Installation
* [ ] Launch Docker Images For Manager
* [ ] Launch Docker Images For Forge4Flow-Core Environments
* [ ] Manage SSL Certs
* [ ] Proxy Traffic Through Manager To Environments

#### Forge4Flow-Core

**Auth4Flow**

* [x] Blockchain Native Login w/ Client & Server Sessions
* [ ] Walletless Onboarding w/ Client & Server Sessions
  * [ ] Transaction Signing APIs
  * [ ] Parent/Child Account Linking
  * [ ] Forced Hybrid Authentication (Creating Flow Child Accounts for Blockchain Native Accounts)
* [x] Blockchain FT/NFT/Event Gated Access Control
* [ ] .find Name and Profile Integration
* [ ] GO Server SDK
* [x] [JS SDK](https://github.com/Forge4Flow/Forge4Flow-JS)
* [x] [Node SDK](https://github.com/Forge4Flow/Forge4Flow-Node)
* [x] [React SDK](https://github.com/Forge4Flow/Forge4Flow-React)
* [x] [Next.js](https://github.com/Forge4Flow/Forge4Flow-NextJS)
* [x] [Swift SDK](https://github.com/Forge4Flow/Forge4Flow-Swift)
* [ ] Kotlin SDK
* [x] Multi-Tenant Support

**Alerts4Flow**

* [x] Custom Event Monitors
* [x] Websocket Support
* [ ] API Route To Configure Webhook Subscriptions To Events

#### Ecosystem SDKs

* Flow Ecosystem
  * FLOAT
    * [x] [Swift (iOS)](https://github.com/Forge4Flow/FLOAT-Swift-SDK)
    * [ ] JS, Node
    * [ ] Go
  * .find
    * [x] [Swift (iOS)](https://github.com/Forge4Flow/FIND-Swift-SDK)
    * [ ] JS, Node
    * [ ] Go
  * Flow NFT Catalog
    * [ ] Swift (iOS)
    * [ ] Go
* Mobile Platforms
  * Swift (iOS)
    * [x] NFT.storage
    * [x] SwiftIPFS-Image
* General Purpose
  * [x] [GCP KMS authorizer (signer)](https://github.com/Forge4Flow/GCP-KMS-Flow-Authorizer)

See the [open issues](https://github.com/Forge4Flow/Forge4Flow-Core/issues) for a full list of proposed features (and known issues).
