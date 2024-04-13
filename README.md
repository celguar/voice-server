# What is it

<img align="right" width="150"  src="https://github-production-user-asset-6210df.s3.amazonaws.com/576838/320511282-f4670bb1-8b0e-492c-a86b-ca67c7aa14fb.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240408%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240408T140843Z&X-Amz-Expires=300&X-Amz-Signature=d30addcc279f44594b1f06fc837e599d863d314f951ed62140769602a352f7e1&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=0">


- Is a separate app that handles UDP voice packets from the game (basically just sends them unchanged to other active members of the voice channel)
- Is the one made by **Ascent Team** (specifically, by _Burlex_) back in 2007-08, just with couple opcodes added and CmakeLists.txt https://github.com/SkyFire/ascent_classic/tree/master/src/ascent-voicechat
- Can be on a separate host, but requires a TCP connection to world server and a UDP connection for users to connect. Ports are configurable
- Builds on Windows and Linux, but I think it doesn't support -c parameter for config file so probably uses current directory when you start it

# How to use:

### World server should handle opcodes, request & manage voice channels while being connected to Voice Chat server, so core change is needed
- CMaNGOS PR: https://github.com/cmangos/mangos-tbc/pull/668

## How Voice Chat works in WoW?
- https://github.com/celguar/voicechat-server/wiki/What-is-Voice-Chat
