![Mirror Logo](https://i.imgur.com/ikP9eYs.png)

[![Download](https://img.shields.io/badge/asset_store-brightgreen.svg)](https://assetstore.unity.com/packages/tools/network/mirror-129321)
[![Documentation](https://img.shields.io/badge/docs-brightgreen.svg)](https://mirror-networking.com/docs)
[![Video Tutorial](https://img.shields.io/badge/video_tutorial-brightgreen.svg)](https://www.youtube.com/playlist?list=PLkx8oFug638oBYF5EOwsSS-gOVBXj1dkP)
[![Forum](https://img.shields.io/badge/forum-brightgreen.svg)](https://forum.unity.com/threads/mirror-networking-for-unity-aka-hlapi-community-edition.425437/)
[![Build](https://img.shields.io/appveyor/ci/vis2k73562/hlapi-community-edition/Mirror.svg)](https://ci.appveyor.com/project/vis2k73562/hlapi-community-edition/branch/mirror)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=vis2k_Mirror&metric=coverage)](https://sonarcloud.io/dashboard?id=vis2k_Mirror)
[![Discord](https://img.shields.io/discord/343440455738064897.svg)](https://discordapp.com/invite/N9QVxbM)
[![release](https://img.shields.io/github/release/vis2k/Mirror.svg)](https://github.com/vis2k/Mirror/releases/latest)

## Mission
Mirror is a **high level** Networking API for Unity, built on top of the **low level** [Telepathy](https://github.com/vis2k/Telepathy) library.

Mirror is built [and tested](https://www.youtube.com/watch?v=mDCNff1S9ZU) for **MMO Scale** Networking by the developers of [uMMORPG](https://assetstore.unity.com/packages/templates/systems/ummorpg-51212) and [Cubica](https://cubica.net).

Mirror is optimized for **ease of use** and **probability of success**. Projects that use Mirror are small, concise and maintainable. uMMORPG was possible with <6000 lines of code. We needed a networking library that allows us to [launch our games](https://mirror-networking.com/showcase/), period.

## Architecture
With Mirror, the **Server & Client are ONE** project _(hence the name)_. Instead of having one code base for the server and one for the client, we simply use the same code for both of them.
* **[Server]** / **[Client]** tags can be used for the server-only and client-only parts
* **[Command]** s are used for Client->Server communication
* **[ClientRpc]** / **[TargetRpc]** for Server->Client communication
* **[SyncVar]** s / SyncLists are used to automatically synchronize state

_Note: Mirror is based on Unity's abandoned UNET Networking system. We fixed it up and pushed it to MMO Scale._

## Low Level Transports
* (built in) [Telepathy](https://github.com/vis2k/Telepathy): TCP
* (built in) [UNET LLAPI](https://docs.unity3d.com/Manual/UNetUsingTransport.html): UDP
* (built in) [Ninja.Websockets](https://github.com/ninjasource/Ninja.WebSockets): Websockets
* [Apathy](https://mirror-networking.com/apathy/): Native TCP
* [FizzySteam](https://github.com/Raystorms/FizzySteamyMirror/): SteamNetwork
* [Ignorance](https://github.com/SoftwareGuy/Ignorance/): ENET UDP
* [LiteNetLib4](https://github.com/MirrorNetworking/LiteNetLibTransport/) LiteNetLib UDP

## Getting Started
Download [Mirror on the Asset Store](https://assetstore.unity.com/packages/tools/network/mirror-129321), open one of the examples & press Play!

Check out our [Documentation](https://mirror-networking.com/docs/) to learn how it all works.

If you are migrating from UNET, then please check out our [Migration Guide](https://mirror-networking.com/docs/General/Migration.html). Don't panic, it's very easy and won't take more than 5 minutes.

## Funding
Mirror is free & open source software funded by Donations. If you love it, please consider supporting [Mirror on GitHub](https://github.com/sponsors/vis2k). As reward, you'll receive our [Network Profiler](https://mirror-networking.com/docs/Guides/Profiler.html?q=Profiler), priority support access and more :)

## Benchmarks
* Telepathy [1000 connections](https://github.com/vis2k/Telepathy) test
* [uMMORPG 480 CCU worst case test](https://youtu.be/mDCNff1S9ZU) (everyone broadcasting to everyone else)

## Mirror Development
Mirror is used **in production** by games ranging from small indie projects to large scale MMORPGs that will run for a decade.

Imagine if your dream game requires networking bug fixes 10 years from now when most contributors moved on and you are left alone with the code base. It is of utmost importance that we follow the KISS principle in order for our future games to survive.

Mirror has plenty of features. What matters now is that we make them as simple, as stable and as performant as possible (in that order).

If you want to contribute, please keep that mind and understand that while **fixes** / **tests** / **improvements** are highly appreciated, new features have a low probability of being merged.
