# Refinery VTT

Refinery is a self-hostable virtual table top system. It is only just beginning,
so don't count on it for your latest (or maybe your next couple) campaigns.

## Goals

The goals of this project include:

### Characters

- [ ] Generate character sheets
- [ ] Keep track of character sheets
- [ ] Avatar creation base on preset characters

### Rules

- [ ] Allow GMs pick from preset rules
- [ ] Allow GMs make their own rules
- [ ] Allow GMs modify rules

### Automation

- [ ] Allow GMs to create automations that make story immersion easier
- [ ] **Dream**: Allow GMs to trigger physical media (such as lights, fog, sounds,
      etc.) using in-built scripting

### Communication

- [ ] Chat platform that supports both in and out of character chats
- [ ] **Dream**: Voice chat with voice processing for in-character

### Map Visualization

- [ ] Show where players are on the map in a pleasing way
- [ ] Support various emotes for each player
- [ ] Per-player/per-group visibility limitations option

### Self-hosting

- [ ] The whole system should be easily self-hostable (ideally just a single binary)
- [ ] The system should be easy to migrate between host computers (i.e. data easily separable)

### System Requirements

- [ ] The final server should be easy to run on a computer with minimal resources
- [ ] The final client should be easy to run within a browser on a modest computer

## Design

This whole project will use the latest version of the Bevy engine (0.15 at the
time of writing). As such, if you are using the supporting "common" types,
you will implicitly pull in bevy as well. This is done mostly to satisfy the
Rust orphan rule.

Rulesets will be implemented in a set of supported scripting languages/VMs
(Lua, Rhai, WASM). Configurations will include a way to override portions of
default rulesets by implementing handlers for certain events.
