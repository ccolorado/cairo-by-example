---
title: "events"
date: 2023-06-22T15:39:00-06:00
draft: false
---

Events are a useful mechanism to logging activity in  smart contracts
    - Require the `#[event]` attribute.
    - Designed to be consumed by off chain clients
    - Only emit events, but not read them.

```cairo
# Declaring an event
#[event]
fn MyEvent(value: u8) {};

# Emmiting an event
#[extenral]
fn emitMyEvent(value: u8 ) {
  MyEvent(value);
}
```