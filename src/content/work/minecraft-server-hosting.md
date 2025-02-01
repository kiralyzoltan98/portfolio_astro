---
title: Hosting a Minecraft Server
publishDate: 2024-04-11 00:00:00
img: /assets/minecraft.png
img_alt: An image of typical american houses.
description: |
    Every so often, my friends and I find ourselves drawn back to Minecraft, the timeless sandbox game that has given us countless hours of fun and creativity. To ensure a smooth and customizable experience, we need a reliable server. This year, I decided to embrace my inner DevOps enthusiast and host the server myself. Here’s the journey, the technical details, and some nostalgic reflections on how hosting a Minecraft server has evolved since my early days of gaming.
tags:
    - Minecraft
    - DevOps
    - Linux
    - Server
---

### The Hosting Evolution: From Aternos to DIY VPS
We’ve often relied on <a href="https://aternos.org/">Aternos.org</a>, a free Minecraft server hosting platform, for our gaming sessions. <a href="https://aternos.org/">Aternos</a> is fantastic for its accessibility—anyone can spin up a server without worrying about costs. However, it comes with limitations:

##### Automatic Shutdowns:
If no one is online, the server goes offline, and restarting it requires manual effort.
##### Limited Customization:
Customizations are restricted to what the <a href="https://aternos.org/">Aternos</a> console allows.
##### Performance Issues:
With multiple players exploring different parts of the map, lag becomes noticeable.

Seeking a smoother, more flexible experience, I explored paid hosting options but realized the cost of renting a dedicated Minecraft server could be better spent on a Virtual Private Server (VPS). A VPS offered the freedom to configure, optimize, and experiment with plugins—all while staying within budget.

### Reviving Old Skills:
Hosting Like It's 2010!
This brought back memories of my first Minecraft server, hosted on my sister’s laptop when I was 14. Back then, I downloaded the server .jar file, tweaked a few config files, and shared my public IP with friends. It worked flawlessly for months, connecting classmates for epic build sessions.

### Fast-forward to today:
hosting a Minecraft server is just as straightforward, but now I had the tools and knowledge to take it to the next level.

The VPS: A Modern Playground for Hosting
After some research, I found a great deal on <a href="https://vipy.hu/hu/services/cloud">vipy.hu</a>, a Hungarian VPS provider. For a steal of <b>3600Ft</b>, I got:

- 4-core AMD CPU
- 8 GB of RAM
- 80 GB SSD storage
- Dedicated IPv4 address

With these specs, I was ready to host a robust Minecraft server. I chose Ubuntu 24.04 as my operating system for its stability and familiarity, and the adventure began.

##### Setting Up the Server: The DevOps Approach
Here’s how I set up my self-hosted Minecraft server, step by step:

### Preparing the VPS
The first step in setting up the VPS was ensuring it was fully updated and secure. I made sure the system had the latest updates installed to improve stability and performance. To secure the server, I configured a firewall to allow only the necessary ports, such as the default Minecraft server port and the one needed for secure remote access. This ensured that the server would only accept connections required for hosting and management, keeping everything locked down against unauthorized access.

#### Downloading the Minecraft Server
To get the server up and running, I visited the official Minecraft website to download the latest server software. Once I had the necessary file, I organized it into a dedicated folder on the VPS to keep everything tidy. This made managing the server files and configurations much easier as I worked through the setup.

#### Configuring the Server
Running the server for the first time generates essential config files. After accepting the EULA, I configured server.properties for gameplay settings like:

Enabling custom resource packs.
Adjusting view distance for performance.
Allowing players to join with plugins enabled.

#### Installing Plugins
Using a Spigot build of the server, I added plugins to enhance gameplay and management. Plugins included:

EssentialsX for quality-of-life improvements.
Dynmap for real-time map visualization.
Custom plugins to fine-tune the experience.

#### Hosting a Resource Pack
To further personalize the server, I created a custom resource pack. I hosted the pack on my website, kiralyzoltan.com, enabling automatic downloads for players upon connection.

#### Automating Server Maintenance
To ensure uninterrupted gameplay, I implemented an automated process to monitor the server’s status. This involved setting up a scheduled task that would periodically check whether the Minecraft server was running. If it detected a crash or unexpected shutdown, it would automatically restart the server, minimizing downtime. This simple automation step added a layer of reliability, making sure my friends and I could always jump back into the game without worrying about technical hiccups.

#### Reflections on Hosting: Then vs. Now
Hosting a Minecraft server has come a long way since my teenage years. While the basics remain familiar—downloading .jar files, configuring ports, and sharing IP addresses—the tools available today make the process much more sophisticated. A VPS offers unmatched flexibility, and Linux's automation capabilities ensure smooth operations with minimal downtime.

### Why Self-Hosting Was Worth It
By hosting my own server, I achieved several benefits:

 - Cost-Effective Performance: Better specs than paid Minecraft hosting at a fraction of the cost.
 - Full Control: Unlimited customization, from plugins to resource packs.
 - Reliability: No more shutdowns due to inactivity, thanks to my cron job.
 - This project wasn’t just about playing Minecraft; it was a chance to flex my DevOps skills, from VPS configuration to process automation. It was nostalgic, educational, and, above all, incredibly satisfying.