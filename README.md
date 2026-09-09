# Guillermo Chagas Sartori

Backend developer — Python, asyncio, distributed systems, low-latency networking.
Based in Rondonópolis, Brazil. Working remotely.

## What I've built

**[dMix128](https://violetaudio.com/dmix128/)** — a 128-channel digital audio mixer,
released commercially in 2026 under the Violet Audio brand. I spent two and a half years
on its software, across three areas:

- **Control layer (Python).** The service sitting between the GUI and the FPGA: it takes
  parameters as JSON, applies the domain logic — EQ filter coefficients, dynamics
  processors, channel routing, processing-chain order, fader and switch behaviour — and
  writes to hardware registers over UDP in custom binary formats. Moving that work into
  software kept the FPGA free for audio.

- **Network subsystem (Python, fully async).** Device discovery over mDNS/Avahi and
  SAP/IGMP, stream allocation, connection health, shared state between remote units,
  state that survives a reboot, and what happens when a unit leaves the network or
  changes address. Three of us built it under a tight deadline; I worked across the
  whole codebase.

- **macOS audio driver (Objective-C/C++).** Written from scratch, in user space, with no
  reference implementation to work from. AES67, 128 channels in and out with effects,
  3 ms round-trip, zero packet loss, on both Intel and Apple Silicon. It ships with the
  product.

## How I work

The team was spread across five time zones — Brazil, Malta, Belarus, China and Australia
— and English was the working language for all of it: code, documentation, issues and
day-to-day communication. Almost every decision was made in writing.

I was handed a register map and a GUI that kept changing, and worked out what the commands
were supposed to do. I reported and fixed bugs outside my own area. When I left, I wrote up
the hardware work I hadn't finished so someone else could pick it up.

## Tech

**In production:** Python (asyncio, concurrency, pub/sub) · C · C++ · Objective-C ·
UDP and sockets · mDNS/Bonjour/Avahi · IGMP · AES67 · Docker · CI/CD (Bitbucket Pipelines) ·
Linux · Git · automated testing

**Learning right now:** SQL and PostgreSQL · Django

## Currently

Open to remote backend roles — full-time employment in Brazil, or contract work
internationally. My professional code lives in private repositories, which is why this
profile is new.

[LinkedIn](COLE-A-URL-AQUI) · guillermochagassartori@gmail.com
