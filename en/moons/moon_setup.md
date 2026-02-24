# Creating your own moon.
## ExtendedLevel

In the same folder as `ExtendedMod`, create `ExtendedLevel` (`Right Click > LethalLevelLoader > Extended Content > ExtendedLevel`)

### General Settings
The `Selectable Level` field is responsible for the selectable level script, we'll deal with this later.

The `Route Price` field is responsible for the cost of flying to the planet (like on `Rend`, `Dine`, etc.).

`Is Route Hidden` determines whether your planet will be hidden from the terminal list.

`Is Route Locked` determines whether your planet will be open for visiting (?)*.
<img width="848" height="871" alt="image" src="https://github.com/user-attachments/assets/1f48880f-abc3-41b1-9818-f5aed314d8a8" />

# SelectableLevel
`SelectableLevel` is, in general, the selectable level itself.

You can find examples in the folder `Assets/LethalCompany/Game/ScriptableObjects/SelectableLevel/`.

For example, let's choose `AdamanceLevel`. Copy it and paste it into your mod's folder.

## Main settings.
<img width="832" height="400" alt="image" src="https://github.com/user-attachments/assets/d102820c-6049-47f6-86bb-cd6a39f31417" />

`Planet Prefab` - planet prefab, there are three types: desert, grassy, snowy.

<img width="237" height="93" alt="image" src="https://github.com/user-attachments/assets/a5367597-cbf9-470b-a759-cc8a9b4ccb67" />

`Scene Name` - a fairly self-descriptive field name. You must enter the EXACT name of the scene where your "moon" will be placed.

`Level ID` - doesn't matter for us. Set it to 0, then LLL will do all the work itself.

`Locked For Demo` - (?)*

`Spawn Enemies And Scrap` - determines whether items and scrap should spawn on this moon.

`Planet Name` - the name of your planet. For my `12-Aerona`, I use the name "`12 Aerona`", in the terminal it's displayed simply as `Aerona`.

`Level Description` - the description of the planet. Exactly what appears on the main ship monitor when you are in orbit of this planet.

`Video Reel` - the video clip that appears on the main ship monitor when you are in orbit of this planet.

`Risk Level` - the danger level of the planet. A, B, C, D, S, S+, S++, anything of your choice. In game, it is displayed as Hazard Level when you land on the planet.

`Time To Arrive` - the amount of time it will take for the ship to land. In the case of Adamance, it's 4 seconds. (?)*

`Day Speed Multiplier` - the speed multiplier at which the day passes on the planet. Standard is 1, but if you want to slow down or speed up time on the planet, you can play around with it.

## Weather settings.
<img width="839" height="528" alt="image" src="https://github.com/user-attachments/assets/ec6d8896-225b-44f1-b181-c21b4a24758b" />

**`Random Weathers`** - an array of elements that will be used when choosing the weather.

`Weather Type` - weather type, includes Rainy, Stormy, Foggy, Flooded, Eclipsed.

**Keep in mind that with the Flooded weather type, everything below the ship's level will be flooded.**

`Weather Variable 1/2` - (?)*

`Override Weather` - whether the weather should be fixed to the one selected in `Override Weather Type`.

`Current Weather` - Runtime variable that is responsible for the current weather on the planet. Don't touch.

## Level settings.
<img width="827" height="337" alt="image" src="https://github.com/user-attachments/assets/eb98a9e1-6a14-4d6e-8163-a76c1a7e88f0" />

`Factory Size Multiplier` - a value that affects the size of the facility itself. On `Titan`, this value is `2.2`, while on `Experimentation` it's 1. Choose one that's comfortable for you.

### Traps appearing inside the maze
`Spawnable Map Objects` - these are mines, turrets, and other traps that may await you inside. Here you can customize them, remove one, or edit them, but often this element is left untouched.

<img width="836" height="606" alt="image" src="https://github.com/user-attachments/assets/d0fdd505-218b-4f1f-b973-63975da31315" />

### Decorations outside
`Spawnable Outside Objects` - these are additional decorative elements that appear outside and are distributed across the map.

They include leafless trees, a pile of rocks, a giant pumpkin, etc.

<img width="839" height="291" alt="image" src="https://github.com/user-attachments/assets/b9f21071-206c-4907-94e0-70f9c61aaa94" />

## Scrap settings.

### Scrap appearing inside the facility
`Spawnable Scrap` - this is a list of items that can appear inside the facility and that players can collect.

`Rarity` determines how often an item can be encountered on your map.

<img width="849" height="218" alt="image" src="https://github.com/user-attachments/assets/38f2e746-39c0-48d4-a2be-226965e3a7b3" />

### Scrap value settings
`Min Scrap` - the minimum number of items that can appear inside the facility.

`Max Scrap` - the maximum number of items that can appear inside the facility.

`Min Scrap Value` - the minimum total value of all items inside the facility.

`Max Scrap Value` - the maximum total value of all items inside the facility.

<img width="837" height="87" alt="image" src="https://github.com/user-attachments/assets/0b3dc798-dfa7-4b9c-8873-23f3de65fb98" />

**Don't try to overly increase or decrease min/max scrap value, try to make it somewhat stable. If your planet is not a lategame option, don't make max scrap value exceed 1000 or more, although, this depends on the overall difficulty of your planet and your intentions.**

## Hostile creature settings. (?)*
`Max Enemy Power Count` - the maximum number of creatures that can exist simultaneously inside the facility.

`Max Outside Enemy Power Count` - the maximum number of hostile creatures that can exist simultaneously outside.

`Max Daytime Enemy Power Count` - the maximum number of other creatures that can exist simultaneously outside.

<img width="828" height="90" alt="image" src="https://github.com/user-attachments/assets/e7dd1be3-fe46-401a-a0d4-65d153e4544a" />

**`Enemies`** - a list of creatures that will appear inside the facility.

`Rarity` - the chance of a specific creature appearing during a spawn cycle.

<img width="839" height="446" alt="image" src="https://github.com/user-attachments/assets/fc11729c-1645-4304-8ebb-d46e944993f1" />

Here you can select creatures from a wide list provided by the game.

<img width="1205" height="227" alt="image" src="https://github.com/user-attachments/assets/456cb9f4-1709-479f-bf4d-2424f9be89f5" />

**Keep in mind that some of the creatures in this list may appear outside, and their presence inside the facility may look very strange and wrong, although the game allows it.**

**`Outside Enemies`** - a list of creatures that will appear outside, such as forest giants, robots, etc.

<img width="833" height="220" alt="image" src="https://github.com/user-attachments/assets/dcb40ea9-74dc-4c43-a25e-81391fbbb3ba" />

**For some entities that should be inside, placing them outside can cause serious lag, but I support experiments and good options could include `SandSpider` or `MaskedPlayerEnemy`.**

## Other creature settings.

You primarily see them when you first arrive on the planet. In the case of `Vow` and `March`, these are harmless swarms of flies, often.

<img width="834" height="356" alt="image" src="https://github.com/user-attachments/assets/63989c58-e5ec-45b7-b6c5-7a6b6d47ca91" />

### Miscellaneous
`Enemy Spawn Chance Throughout Day`, etc. - graphs responsible for the spawn chance of certain entities throughout the day.

`Spawn Probability Range` - (?)*

`Daytime Enemies Probability Range` - (?)*

<img width="826" height="126" alt="image" src="https://github.com/user-attachments/assets/d1225d27-58a2-4abb-b630-4216f65c848f" />

## Other level settings.
`Level Includes Snow Footprints` - whether snow footprints should be left on this planet. For full functionality, you'll need to work with the `Terrain` and take something from other original moons.

`Level Icon String` - (?)*

<img width="834" height="48" alt="image" src="https://github.com/user-attachments/assets/eadd3dd9-b289-4243-85cf-4b29188009ea" />

_(?) - I'm not entirely sure about the correctness of the phrasing_
