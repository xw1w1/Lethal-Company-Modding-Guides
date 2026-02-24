# Creating the Mod

**If you haven't completed the [project setup](https://github.com/xw1w1/Lethal-Company-Modding-Guides/blob/main/en/moons/project_setup.md) stage yet, I recommend doing it right now.**

For brevity, I'll use the abbreviation LLL when talking about Lethal Level Loader.

If you've already imported all the necessary dependencies into the project, you can start creating the mod itself.

Since `LethalLevelLoader` is used for the planet, we'll first make the LLL mod itself.

In the `Assets/LethalCompany/Mods` folder, create your own folder next to `plugins`.

<img width="415" height="232" alt="image" src="https://github.com/user-attachments/assets/65bc403b-3011-4c71-8e08-b89a6f2070ea" />

Inside this folder, create an `ExtendedMod`. (`Right Click > LethalLevelLoader > ExtendedMod`)

The following `ScriptableObject` should appear in your folder:
<img width="854" height="367" alt="image" src="https://github.com/user-attachments/assets/faca4f33-86de-4df5-855e-248278e95bf8" />

The `Mod Name` field, as you might guess, is responsible for the name of your mod.
The `Author Name` field is the author's name. In my case, it's `Turbotaliz`. Keep in mind that it's better to use the same author name for all your projects :')

The fields with **Extended** content are what we want to add to our mod in the future.

It comes in different types: from custom items and moons to custom vehicles and footprint types on the ground.

### Project Structure
I'll add this note just for general understanding.

In the future, we'll split the project into bundles: one for the scene, and only the scene (Scene Asset), and a second for all the necessary mod files (ExtendedMod, ExtendedLevel, SelectableLevel, etc.).

The project structure may vary, but I follow this scheme:

```
LethalCompany/
\Game
\Mods
-\plugins [Files for BepInEx]
-\TurbotalizsMoons [Root folder where I store my projects]
--\12Aerona [The Aerona mod itself, one of my planets]
---|Include [Music and some meshes that I use in the scene]
---ExtendedLevel, ExtendedMod, etc. [The scene can actually be placed here too]
--\SharedPrefabs [Prefabs I made in advance. Shelves, hangars, ready-made trees, and other decor that I took from other maps. They are not part of the mod itself, only its scene, and can be used in other mods, which is why they're Shared.]
--\BlankReferences [We'll get to this later in the optimizations section]
--\Scenes [Folder for scene assets, but this is optional]
```

This is how I do it, but you can organize the project in a way that's convenient for you personally. I'm just showing how I have my resources distributed.

Starting from here, you can proceed to the next step: https://github.com/xw1w1/Lethal-Company-Modding-Guides/blob/main/en/moons/moon_setup.md
