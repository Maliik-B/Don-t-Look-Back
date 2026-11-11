# Don't Look Back

### Team On The Spot

![image](https://ianmatic.com/images/lookBack.png)

A horror game developed in Unity with C#. Originally a team school project at RIT (October 2019, Team On The Spot).

- **Play it on itch.io:** https://ianmatic.itch.io/dont-look-back
- **Gameplay video:** https://www.youtube.com/watch?v=W-NjUMILNjw

Ian continued expanding the game after the semester ended and shipped the itch.io build above.

## Team

| Role | Dev |
|---|---|
| Lead programmer / Enemy AI / Room system | Ian Matic ([ianmatic](https://github.com/ianmatic)) |
| UI, scene flow, pause, polish | Maliik Bryan ([Maliik-B](https://github.com/Maliik-B)) |
| Gameplay / systems | James Schrupp |
| Gameplay / systems | TJ Driscoll |
| Gameplay / systems | Anthony Ferraioli |

## My Contributions

October 2019, mostly under `Assets/Scripts/UI/`.

- **Pause system** (`Scripts/UI/Pause.cs`) - escape-key pause with state preservation and resume hook
- **Scene loading and flow** (`Scripts/UI/SceneLoader.cs`) - menu → game → victory / death routing, with level-remembrance so the death screen returns the player to the correct level
- **Main menu polish** - layout centering, button states, visual pass to match the tone
- **Victory and death scenes** - built `victoryScene.unity` and `endingScene.unity` and the UI manager hooks that load them
- **Light flickering** (`Scripts/UI/LightFlicker.cs`) - the flicker on the scene lights
- **Integration touches** on `PlayerMovement.cs` and `RoomManager.cs` to expose the accessors and scene transitions my UI layer needed

In July 2020 Ian re-imported the project as a new root commit ([`38c2f20`](https://github.com/Maliik-B/Don-t-Look-Back/commit/38c2f20a5f5b9c909e18c40ce8b160c4d565d400)) and merged it with the original history, so GitHub's blame view shows his name on these scripts too. My originals are in [`9ad2e9b`](https://github.com/Maliik-B/Don-t-Look-Back/commit/9ad2e9b1a60f75216c690d46e6a20e1ca0c63cba) (`SceneLoader.cs`), [`7085517`](https://github.com/Maliik-B/Don-t-Look-Back/commit/7085517707de9247775e0f2fd030eedfa9b8a6a7) (`LightFlicker.cs`) and [`4091495`](https://github.com/Maliik-B/Don-t-Look-Back/commit/4091495a31d51972c4300e24188324f69e688b70) (`Pause.cs`), from October 2019.

## Repo Layout

```
Assets/
  Scripts/
    Camera/      - 3rd-person camera control
    EnemyAI/     - 5-state enemy pathfinding
    Objects/     - Door, Key, LadderProperties, StairProperties
    Player/      - PlayerMovement, Flashlight, Tutorial
    Room/        - RoomManager, RoomProperties, EntityRoomUpdater, WallProperties
    Sound/       - AudioManager singleton + Sound class
    UI/          - Pause, SceneLoader, MenuManager, SettingsMenu, VictoryManager,
                   LightFlicker, GameManager, UIManager, Singleton
  Scenes/        - MainMenu, Level1/2/3, victoryScene, endingScene
  Models, Prefabs, Sounds, Animation/, Victorian Interiors/, GHOUL/
```
