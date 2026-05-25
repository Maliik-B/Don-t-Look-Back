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

19 commits, ~316 LOC across `Assets/Scripts/`, October 2019.

- **Pause system** (`Scripts/UI/Pause.cs`) - escape-key pause with state preservation and resume hook
- **Scene loading and flow** (`Scripts/UI/SceneLoader.cs`) - menu → game → victory / death routing, with level-remembrance so the death screen returns the player to the correct level
- **Main menu polish** - layout centering, button states, visual pass to match the tone
- **Victory and death scenes** - built `victoryScene.unity` and `endingScene.unity` and the UI manager hooks that load them
- **Light flickering** (`Scripts/UI/LightFlicker.cs`) - ambient-unease pass on environmental lights
- **Integration touches** on `PlayerMovement.cs` and `RoomManager.cs` to expose the accessors and scene transitions my UI layer needed

## Repo Layout

```
Assets/
  Scripts/
    Camera/      - 3rd-person camera control
    EnemyAI/     - 5-state enemy pathfinding (~1K LOC)
    Objects/     - Door, Key, LadderProperties, StairProperties
    Player/      - PlayerMovement, Flashlight, Tutorial
    Room/        - RoomManager, RoomProperties, EntityRoomUpdater, WallProperties
    Sound/       - AudioManager singleton + Sound class
    UI/          - Pause, SceneLoader, MenuManager, SettingsMenu, VictoryManager,
                   LightFlicker, GameManager, UIManager, Singleton
  Scenes/        - MainMenu, Level1/2/3, victoryScene, endingScene
  Models, Prefabs, Sounds, Animation/, Victorian Interiors/, GHOUL/
```
