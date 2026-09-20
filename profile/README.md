# bedrock-v

bedrock-v is an open-source organization building server software and
reusable libraries for Minecraft: Bedrock Edition in the V programming language.

The projects range from protocol and networking libraries to server software. Most of the ecosystem is still under active
development, so contributions, testing and protocol research are welcome.

<p align="center">
    <a href="https://discord.gg/cM9BQsAk9D">
        <img src="https://discord.com/api/guilds/1520807994999439550/widget.png?style=banner2" alt="bedrock-v Discord"/>
    </a>
</p>

---

## Projects

### Vedrock

Minecraft: Bedrock Edition server software written in V.

Vedrock is the main server project in the organization. It brings together
the protocol, networking, world and gameplay libraries developed across
bedrock-v.

### Protocol

**protocol** — Minecraft: Bedrock Edition protocol implementation for V.

Packet definitions, encoding and decoding and the protocol types used by
Vedrock and other Bedrock projects.

### Networking

**nethernet** — NetherNet transport for modern Minecraft: Bedrock Edition.

**webrtc-v** — WebRTC implementation used by NetherNet.

**raknet** — RakNet transport for Minecraft: Bedrock Edition.

### Data & world formats

**nbt** — Named Binary Tag encoding and decoding for V.

Other supporting libraries are developed as the ecosystem grows.

---

## Development

bedrock-v is still evolving. APIs may change while the projects mature and
Minecraft itself continues to change.

We try to keep projects small and reusable rather than putting the entire
Bedrock stack inside the server. Libraries should be useful independently
where that makes sense.

If you want to contribute, bug reports, testing, documentation, protocol
research and pull requests are all useful.

See the [contribution guidelines](https://github.com/bedrock-v/.github/blob/master/profile/CONTRIBUTING.md) before starting larger changes.

---

## Community

Development and project discussion happens on GitHub and Discord.

If you're working with Minecraft Bedrock in V, experimenting with the
protocol, or just interested in the projects, you're welcome to join.
