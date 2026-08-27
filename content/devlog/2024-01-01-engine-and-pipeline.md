---
title: "Engine & Pipeline"
date: 2024-01-01
draft: false
summary: "Why PotHole Dodgers stays on Unreal Engine 5 — and what the terrain pipeline looks like."
---

Every few months I ask myself whether this project should move to a different engine. The answer keeps being no, and now I can say exactly why.

**The terrain is the game.** PotHole Dodgers is set in a ~400 km² slice of the East Rand / Gauteng. That's not a stylized map — it's real geography, built from SRTM/DEM elevation data. The pipeline: merged SRTM tiles → heightmap import → UE5 Landscape with World Partition, so the world streams in chunks as you drive. Roads are then laid along that heightfield, which is what keeps the highway feeling like a place instead of a track.

There is no Godot equivalent for that stack. That single fact settles most of the debate before it starts.

**The systems are C++, and they stay.** The gearbox, the weapons system, the three-currency economy — these are hand-built C++ systems in UE 5.8. They don't port to GDScript or C#; they'd be rewrites, not migrations.

**The Windows slices are specs, not code.** I still keep the old .exe vertical slices from the Windows era. They're 100% working behavioral references — how the J160 gearbox should feel, how vehicle lights should behave at night, what a specific tile of landscape looked like when it was right. They live on and guide the rebuild.

So: Unreal Engine 5.8, C++, real-geography terrain pipeline. Not because I'm attached to the engine, but because this particular game is exactly where that stack earns its keep.
