# Unity 3D Interaction Prototype

A Unity prototype for character movement and event-driven interactions. The example scene brings together a controllable character, a health bar, collectible resources, and ground buttons that trigger sequences of events.

## Features in the source

- Rigidbody-based movement with keyboard axes and a mobile joystick fallback.
- Character rotation and Animator parameters for movement, hit reactions, and death.
- A health bar that follows the character.
- Trigger-based damage when the character encounters an object marked with `EnemyDamage`.
- Collectibles that animate toward the player and return to their spawn position.
- Ground buttons with a fill indicator and configurable delayed UnityEvents.
- A helper component for triggering character animations.

## Technology

- Unity **2022.3.30f1**
- Universal Render Pipeline **14.0.11**
- C#, uGUI, and TextMeshPro
- Mobile joystick utilities included under `Assets/Plugins`

## Open the project

1. Clone this repository.
2. In Unity Hub, add the repository's root folder as an existing project.
3. Open it with Unity 2022.3.30f1 and let Unity import the assets and resolve packages.
4. Open [Test_Example.unity](Assets/Game/Scenes/Test_Example.unity).
5. Enter Play mode to explore the example scene.

The player script reads the `Horizontal` and `Vertical` input axes when the mobile joystick is idle. Ground-button behavior is configured through Inspector events.

## Source guide

| File | Purpose |
| --- | --- |
| [Player.cs](Assets/Game/Scripts/Player.cs) | Movement, health, damage, and trigger interactions |
| [Collectable.cs](Assets/Game/Scripts/Collectable.cs) | Collection animation and respawning |
| [GroundButton.cs](Assets/Game/Scripts/GroundButton.cs) | Fill indicator and delayed event sequences |
| [PlayerAnimationTrigger.cs](Assets/Game/Scripts/PlayerAnimationTrigger.cs) | Animator trigger helper |
| [EnemyDamage.cs](Assets/Game/Scripts/EnemyDamage.cs) | Marker component recognized by the player's damage logic |

## Scope

This repository is a gameplay interaction prototype. Collection effects and button actions depend on the events configured in the scene and Inspector; the scripts do not define a complete progression or inventory system.
