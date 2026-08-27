---
title: "Vertical Slice: The Gauteng World"
date: 2026-08-15
draft: false
summary: "Heightmap terrain import complete — 8192×8192 merged SRTM tiles. Where the slice stands."
---

The vertical slice is moving, and the foundation under it is done.

## Terrain import complete

The merged SRTM heightmap for the East Rand region is in — **8192×8192**, built from merged SRTM elevation tiles covering the ~400 km² play area. It's imported as a UE5 Landscape with World Partition, so the world streams in regions as you drive rather than loading as one block. The road network now follows the actual heightfield, which is the difference between "a map of Gauteng" and "Gauteng."

## What's next in the slice

- **Road network** — laying the highway corridors along the terrain, with the event zones branching off them
- **Vehicle physics** — the J160 gearbox behavior is specced from the old Windows slices; that's the reference the new C++ system has to match
- **Event boards** — the sprint / circuit / survival / raid loop, wired end-to-end so placement actually pays out SCRAP and FLUID

## A note on the rebuild

This slice isn't starting from zero. The old Windows .exe slices still exist as behavioral specs — night sky, vehicle lights, gearbox feel, a specific tile of landscape that was right. Every system I build gets compared against them. If it doesn't match the spec, it's not done.

That's the standard for the rest of development: the old game is the boss, and the new one has to pass its tests.
