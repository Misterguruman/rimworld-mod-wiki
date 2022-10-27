<h1 align="center">Creating Backstories</h1>

[< back](../../README.md)


> this information is referenced starting in the '/Data/Core/Defs/Solid_Adult.xml' file

> supplemental information taken from the [wiki](https://rimworldwiki.com/wiki/Skills)

> as always the information found here is incomplete, and is added to as we learn, feel free to fork and contribute if you find something is missing

An example of a backstory object

```xml
  <BackstoryDef>
    <defName>CivilEngineer2</defName> <!-- Use defName to create a uid for your character, or overwrite -->
    <ignoreIllegalLabelCharacterConfigError>False</ignoreIllegalLabelCharacterConfigError> <!-- False -->
    <identifier>CivilEngineer2</identifier> <!-- A separate uid? Seems to always === defName -->
    <slot>Adulthood</slot> <!-- Choose age Childhood/Adulthood -->
    <title>civil engineer</title> <!-- The label used in game (pretty name) -->
    <titleShort>engineer</titleShort> <!-- Shortened version of the pretty name -->
    <baseDesc>[PAWN_nameDef] was a well-known civil engineer. [PAWN_possessive] job involved designing and maintaining rock fortification structures. [PAWN_pronoun] did enough statistical analysis to keep [PAWN_possessive] mind sharp.</baseDesc> <!-- See below -->
    <skillGains><!-- See below -->
      <li>
        <key>Construction</key>
        <value>7</value>
      </li>
      <li>
        <key>Intellectual</key>
        <value>3</value>
      </li>
      <li>
        <key>Mining</key>
        <value>2</value>
      </li>
      <li>
        <key>Social</key>
        <value>-3</value>
      </li>
    </skillGains>
    <workDisables>None</workDisables> 
    <requiredWorkTags>None</requiredWorkTags> <!-- Always None -->
    <spawnCategories> <!-- -->
      <li>Offworld</li>
      <li>Outlander</li>
      <li>Pirate</li>
    </spawnCategories>
    <bodyTypeGlobal>Male</bodyTypeGlobal> <!-- Global Gender Body Type -->
    <bodyTypeFemale>Male</bodyTypeFemale> <!-- Body Type if Female -->
    <bodyTypeMale>Male</bodyTypeMale> <!-- Body Type if Male -->
    <shuffleable>False</shuffleable> <!-- idk -->
  </BackstoryDef>
```

# ignoreIllegalLabelCharacterConfigError
This field appears to be False always, there are no instances of True in the Core file referenced above

# baseDesc
This field is a description field for the character, I'm gathering a list of as many options as I can find for environment variables you can use to spice up the text below

- [PAWN_possessive] - your character's pronoun (Possessive)
- [PAWN_pronoun]    - your character's pronoun (subjective)
- [PAWN_nameDef]    - your defName property 
- [PAWN_objective]  - your character's pronoun (Objective)

 A pronoun chart for choosing which pronous to use because I needed one below: 

| Subjective | Objective | Possessive |
|   ---      |   ---     |      ---   |
|I           |me         |my          |
|you         |you        |your        |
|he          |him        |his         |
|she         |	her      |	her       |
|it          |	it       |	its       |
|we          |	us       |	our       |
|they        |	them     |	their     |
|who         |	whom     |	whose     |
|whoever     |	whomever |	whose ever|

# skillGains
A collection of nested \<li> tags containing a \<key> and \<value> tag

According to the [wiki](https://rimworldwiki.com/wiki/Skills)

A list of possible (default) skills below:
- Shooting
- Melee
- Construction
- Mining
- Cooking
- Plants
- Animals
- Crafting
- Artistic
- Medical
- Social
- Intellectual

Max level is level 20

For creating new skills, see [Skills](../skills/skills.md)