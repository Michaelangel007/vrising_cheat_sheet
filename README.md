# V-Rising Cheat Sheet For Teleport

## Admin Mode

1. Options > General > Console Enabled `[x]`
2. Press `~`
3. `AdminAuth`

## Waygates

In v1.1 there are 22 waygates:

```
    TeleportToChunkWaypoint 16,19  Cursed Forest (E)
    TeleportToChunkWaypoint 13,19  Cursed Forest (W)
    TeleportToChunkWaypoint 10,20  Gloomrot North (NE)
    TeleportToChunkWaypoint  8,18  Gloomrot North (SW)
    TeleportToChunkWaypoint 10,18  Gloomrot South
    TeleportToChunkWaypoint 15,13  Hallowed Mountains
    TeleportToChunkWaypoint 12,15  Dunley Farmlands (NE)
    TeleportToChunkWaypoint  9,16  Dunley Farmlands (NW)
    TeleportToChunkWaypoint 13,13  Dunley Farmlands (SE) 
    TeleportToChunkWaypoint  9,13  Dunley Farmlands (SW)
    TeleportToChunkWaypoint 11,11  Farbane Woods (C)
    TeleportToChunkWaypoint 14,11  Farbane Woods (NE)
    TeleportToChunkWaypoint  6,12  Farbane Woods (NW)
    TeleportToChunkWaypoint 14, 8  Farbane Woods (SE)
    TeleportToChunkWaypoint  8, 8  Farbane Woods (SW)
    TeleportToChunkWaypoint  9,10  Farbane Woods (W 
    TeleportToChunkWaypoint  6,20  Oakveil Woodlands (NE)
    TeleportToChunkWaypoint  4,18  Oakveil Woodlands (SW)
    TeleportToChunkWaypoint 15,17  Ruins of Mortium (NW)
    TeleportToChunkWaypoint 17,16  Ruins of Mortium (E)
    TeleportToChunkWaypoint 15,15  Ruins of Mortium (SW)
    TeleportToChunkWaypoint  6,16  Silverlight Hills
```
## Cave Teleport Coordinates

See [v1.1 Map with Caves and Waypoints](https://old.reddit.com/r/vrising/comments/1kc6v3r/updated_v11_map_with_caves_and_waypoints/)

* [Caves](https://i.redd.it/trdsj6h8s5ye1.png)

In v1.1 there are 10 caves:

```
                               From         To                                      Nearest Chunk
    Teleport Self TilePosition 2206, 3254   Farbane (SW) to Cursed Forest           TeleportToChunk 6,10
    Teleport Self TilePosition 5033, 6416   Cursed Forest to Farbane (SW)           TeleportToChunk 15,19
    
    Teleport Self TilePosition 3225, 3424   Farbane to Gloomroot                    TeleportToChunk 9,10
    Teleport Self TilePosition 3497, 6396   Gloomrot to Farbane                     TeleportToChunk 10,19
    
    Teleport Self TilePosition 3875, 3234   Farbane to Dunley                       TeleportToChunk 12,10
    Teleport Self TilePosition 3424, 4774   Dunley to Farbane                       TeleportToChunk 10,14
    
    Teleport Self TilePosition 4334, 3796   Farbane to Oakveil Woodlands            TeleportToChunk ?,?
    Teleport Self TilePosition 1729, 6472   Oakveil Woodlands to Farbane Woods      TeleportToChunk ?,?
    
    Teleport Self TilePosition 2386, 4814   Silverlight Hills TO Farbane Woods (SE) TeleportToChunk ?,?
    Teleport Self TilePosition 4983, 3476   Farbane (SE) to Silverlight Hills       TeleportToChunk ?,?
```

## Camps

```
Teleport Self TilePosition 1400, 6225  Stavros the Caber @ Carvers Logging Camp
```

## Fishing

```
Teleport Self TilePosition 1441, 4623 Brighthaven Docks
```

## Mines

```
TeleportToChunk 11,14  Haunted Iron Mine
TeleportToChunk 10,19  Transcedium Mine
```


## Secret Locations

```
TeleportToChunk  7, 2  Dev Island #1
```

## Starting Cave / Tutorial

```
Teleport Self TilePosition 1183, 61     Tutorial cave / coffin
Teleport Self TilePosition 1180, 90     Top of stairs down in tutorial cave
Teleport Self TilePosition 4668, 2358   Exit starter/tutorial cave

TeleportToChunk 11,2                  Unused Dev/Test Tutorial Cemetary 
Teleport Self TilePosition 3680, 880  Unused Dev/Test Tutorial Cemetary 
```

## Tiles-to-Chunks

To convert chunks to tile position use this formula:

* Tile = Chunk*320 + 160

```
       N                 N
       ^                 ^
       |                 |
     11, 14 ---> E   3680, 4640 --> E
    Chunks           Tiles

TeleportToChunk 4, 18 ~= Teleport Self TilePosition 1440, 5920
TeleportToChunk 4, 14 == Teleport Self TilePosition 1440, 4640
TeleportToChunk 11,14 == Teleport Self TilePosition 3680, 4640

TeleportToChunk         7,14 == Teleport Self TilePosition 2400, 4640 (Emberleaf Grove)
TeleportToChunk         6,13 == Teleport Self TilePosition 2080, 4320
TeleportToChunk         6,12 == Teleport Self TilePosition 2080, 4000
n/a                          == Teleport Self TilePosition 2198, 3984 == TeleportToChunkWaypoint 6,12

Teleport Self TilePosition 16000, 9000  out-of-bounds --> default farbane SE
```

## Map Boundary

Main map boundary (note, it makes a polygon (!) not a square):

```
    Teleport Self TilePosition  961, 7039 -- Top Left
    Teleport Self TilePosition 4799, 7039 -- Top Right
    Teleport Self TilePosition  961,    ? --  Bottom Left
    Teleport Self TilePosition 4799,    ? -- Bottom Right
    Teleport Self TilePosition 3680, 2240 -- Bottom middle of map
    Teleport Self TilePosition 6300, 5200 -- Far Right, Dracula's Castle
```

# "Safe" City Locations

```
Teleport Self TilePosition 1400, 4600   SW corner of Brighthaven Docks
```

# References / Links

* https://old.reddit.com/r/vrising/comments/1kc6v3r/updated_v11_map_with_caves_and_waypoints/
* https://old.reddit.com/r/vrising/comments/14r2j1j/map_waygates_coords_for_admin_commands/
* https://i.redd.it/trdsj6h8s5ye1.png
* https://preview.redd.it/1yx0pbck092d1.png?width=3465&format=png&auto=webp&s=18b623ae8776133d9ce28dcc921514c7a8dd8a4a