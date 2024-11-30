---
type: PC
tags: 
playerName: 
playerArt: 
details:
  background: 
  alignment: 
  languages:
    - 
    - 
    - 
  age: 0
  gender: 0
  height: 0
  weight: 0
  totalLevel: 0
  faith: ""
race:
  name: 
  subrace: 
  traits: 
class1:
  name: 0
  subclass: []
features: 
feats: 
prof: 1
combat:
  tempHP: 0
  initiative: 
  ac: 0
  conditions: []
  resistances: 
  hitDice: '[MB_EXPRESSION] "failed to evaluate expression" caused by error "Undefined symbol False"'
  inspiration: true
  speed: 30
  tHP: 0
  thp: 
  hitDiceAMOUNT: 0
  maxHP: 0
  currentHP: 0
  hitDiceUSE: 0
  exhaustion: 0
deathSaves:
  successOne: false
  successTwo: false
  successThree: false
  failOne: false
  failTwo: false
  failThree: false
abilityScores:
  str: 0
  dex: 0
  con: 0
  int: 0
  wis: 0
  cha: 0
  mod:
    str: -5
    dex: -5
    con: -5
    int: -5
    wis: -5
    cha: -5
savingThrows:
  str: false
  dex: false
  con: false
  int: false
  wis: false
  cha: false
skills:
  acrobatics: -5
  athletics: -5
  animalHandling: -5
  arcana: -5
  deception: -5
  history: -5
  insight: -5
  intimidation: -5
  investigation: -5
  medicine: -5
  nature: -5
  perception: -5
  performance: -5
  persuasion: -5
  religion: -5
  sleightOfHand: -5
  stealth: -5
  survival: -5
  persuassion: false
  prof:
    performance: false
    athletics: false
    religion: false
    arcana: false
    investigation: false
    perception: false
    insight: false
    deception: false
    acrobatics: false
    stealth: false
  expt:
    nature: false
    stealth: false
    athletics: false
    arcana: false
    medicine: false
    acrobatics: false
    animalHandling: false
    deception: false
    history: false
    insight: false
    perception: false
proficiencies:
  armor: []
  weapons: []
  tools: []
  languages: []
globalMod:
  savingThrow: 
  skillCheck: 
  ac: 0
  prof: 0
  speed: 0
passive:
  perception: 
  investigation: 
  insight: 
spells:
  slots1: 4
  slots2: 3
  slots3: 2
  slots4: 1
  slots5: 0
  slots6: 0
  slots7: 0
  slots8: 0
  slots9: 0
sca: 0
sca_temp: 0
values:
  copper: 5
  silver: 9
  electrum: 
  gold: 66
  platinum: 
experimentalElixir:
  healing: 1
  swiftness: 0
  resilience: 0
  boldness: 0
  flight: 0
  transformation: 0
expt: 2
defenses:
  resistances: []
  resistance: []
cssclasses:
  - hc
  - h-line
  - t-c
  - paper
  - wide
---
# `=this.file.name`
---

>[!cards|no-i no-t  5]
> > [!recite| no-i txt-c]  Speed­ `VIEW[{globalMod.speed}<0 ? "(-" : {globalMod.speed}>0 ? "(+" : ""]`­`VIEW[{globalMod.speed} == 0 ? "" : abs({globalMod.speed})]`­`VIEW[{globalMod.speed}==0 ? "" : ")"]`
> > ### `VIEW[({race.name} == 12 ? 35: {race.name} == 52 ? 35 :{race.name} == 34 ? 35 : 30) + {globalMod.speed}]` ft
> > `BUTTON[increment-speed, decrement-speed]`
> >
> 
> > [!recite| no-i txt-c] AC­ `VIEW[{globalMod.ac}<0 ? "(-" : {globalMod.ac}>0 ? "(+" : ""]`­`VIEW[{globalMod.ac} == 0 ? "" : abs({globalMod.ac})]`­`VIEW[{globalMod.ac}==0 ? "" : ")"]`
> > ### `VIEW[{abilityScores.mod.dex} + 10 + {globalMod.ac}]`
> > `BUTTON[increment-ac, decrement-ac]`
> 
> > [!recite| no-i txt-c] Level
> > ### `VIEW[{details.totalLevel}]`
> > `BUTTON[levelUpID]`
> 
> > [!recite| no-i txt-c] Inspiration
> >### `INPUT[toggle:combat.inspiration]`
> 
> >[!recite| no-i txt-c] Prof `VIEW[{globalMod.prof}<0 ? "(-" : {globalMod.prof}>0 ? "(+" : "­"]`­`VIEW[{globalMod.prof} == 0 ? "­" : abs({globalMod.prof})]`­`VIEW[{globalMod.prof}==0 ? "­" : ")"]`
> > ### `VIEW[{prof} > 0 ? "+" : {prof} < 0 ? "-": "" ]`­`VIEW[(ceil({details.totalLevel} / 4 + 1) + {globalMod.prof})][math:prof]`
>  >`BUTTON[increment-prof, decrement-prof]`

> [!columns| no-i no-t 3  ] 
> > [!infobox| wfull left clean  no-t]  
> >![[Pasted image 20240229200427.png | cover  ]]
> >
> > >[!table|clean wfull n-th no-t]
> > >
| Details        |                                   |
| -------------- | -------------------- |
| **Gender**     | `INPUT[inlineSelect(option(1, Male), option(2, Male)):details.gender]`       |
| **Race**       | `INPUT[inlineSelect(option(1, Dragonborn), option(2, Dwarf), option(3, Elf), option(4, Gnome), option(5, Half-Elf), option(6, Halfling), option(7, Half-Orc), option(8, Human), option(9, Tiefling), option(10, Aarakocra), option(11, Aasimar), option(12, Air Genasi), option(13, Bugbear), option(14, Centaur), option(15, Changeling), option(16, Deep Gnome), option(17, Duegar), option(18, Earth Gensai), option(19, Eladrin), option(20, Fairy), option(21, Firbolg), option(22, Fire Gensai), option(23, Githyanki), option(24, Githzerai), option(25, Goblin), option(26, Goliath), option(27, Harengon), option(28, Hobgoblin), option(29, Kenku), option(30, Kobold), option(31, Lizardfolk), option(32, Minotaur), option(33, Orc), option(34, Satyr), option(35, Sea Elf), option(36, Shadar-kai), option(37, Shifter), option(38, Tabaxi), option(39, Tortle), option(40, Triton), option(41, Water Genasi), option(42, Yuan-ti), option(43, Kender), option(44, Astral Elf), option(45, Autognome), option(46, Giff), option(47, Hadozee), option(48, Plasmoid), option(49, Thri-kreen), option(50, Owlin), option(51, Lineages), option(52, Leonin), option(53, Kalashtar), option(54, Warforged), option(55, Verdan), option(56, Loxodon), option(57, Simic Hybrid), option(58, Vedalken), option(59, Feral Tiefling), option(60, Locathah), option(61, Grung), option(62, Cervan), option(63, Corvum), option(64, Gallus), option(65, Hedge), option(66, Jerbeen), option(67, Luma), option(68, Mapach), option(69, Raptor), option(70, Strig), option(71, Vulpin)):race.name]`    |
| **Class**      | `INPUT[inlineSelect(option(1, Artificer), option(2, Barbarian), option(3, Bard), option(4, Blood Hunter), option(5, Cleric), option(6, Druid), option(7, Fighter), option(8, Monk), option(9, Paladin), option(10, Ranger), option(11, Rogue), option(12, Sorcerer), option(13, Warlock), option(14, Wizard)):class1.name]`     |
| **Subclass**   | `INPUT[inlineListSuggester(option(--- Artificer ---), option('Alchemist'), option('Armorer'), option('Artillerist'), option('Battle Smith'), option(--- Barbarian ---), option('Path of the Ancestral Guardian'), option('Path of the Battlerager'), option('Path of the Beast'), option('Path of the Berserker'), option('Path of the Giant'), option('Path of the Storm Herald'), option('Path of the Totem Warrior'), option('Path of the Wild Magic'), option('Path of the Zealot'), option(--- Bard ---), option('College of Creation'), option('College of Eloquence'), option('College of Glamour'), option('College of Lore'), option('College of Spirits'), option('College of Swords'), option('College of Valor'), option('College of Whispers'), option(--- Cleric ---), option('Ambition Domain)'), option('Arcana Domain'), option('Blood Domain'), option('Community Domain'), option('Death Domain'), option('Forge Domain'), option('Grave Domain'), option('Knowledge Domain'), option('Life Domain'), option('Light Domain'), option('Moon Domain'), option('Nature Domain'), option('Night Domain'), option('Order Domain'), option('Peace Domain'), option('Solidarity Domain'), option('Strength Domain'), option('Tempest Domain'), option('Trickery Domain'), option('Twilight Domain'), option('War Domain'), option('Zeal Domain'), option(--- Druid ---), option('Circle of Dreams'), option('Circle of Spores'), option('Circle of Stars'), option('Circle of the Land)'), option('Circle of the Moon'), option('Circle of the Shepherd'), option('Circle of Wildfire'), option(--- Fighter ---), option('Arcane Archer'), option('Banneret'), option('Battle Master'), option('Cavalier'), option('Champion'), option('Echo Knight'), option('Eldritch Knight'), option('Psi Warrior'), option('Rune Knight'), option('Samurai'), option(--- Monk ---), option('Way of Mercy'), option('Way of Shadow'), option('Way of the Ascendant Dragon'), option('Way of the Astral Self'), option('Way of the Drunken Master'), option('Way of the Four Elements'), option('Way of the Kensei'), option('Way of the Long Death'), option('Way of the Open Hand'), option('Way of the Sun Soul'), option(--- Paladin ---), option('Oath of Conquest'), option('Oath of Glory'), option('Oath of Redemption'), option('Oath of the Ancients'), option('Oath of the Crown'), option('Oath of Devotion'), option('Oath of the Watchers'), option('Oath of Vengeance'),  option('Oath of the Open Sea'), option('Oathbreaker'), option(--- Ranger ---), option('Beast Master'), option('Drakewarden'), option('Fey Wanderer'), option('Gloom Stalker'), option('Horizon Walker'), option('Monster Slayer'), option('Swarmkeeper'), option(--- Rogue ---), option('Arcane Trickster'), option('Assassin'), option('Inquisitive'), option('Mastermind'), option('Phantom'), option('Scout'), option('Soulknife'), option('Swashbuckler'), option('Thief'), option(--- Sorcerer ---),  option('Aberrant Mind)'), option('Clockwork Soul'), option('The Divine Soul'), option('The Draconic Bloodline'),option('Lunar Sorcery'), option('Runechild)'), option('Shadow Magic'), option('Storm Sorcery'), option('Wild Magic'), option(--- Warlock ---), option('The Archfey'), option('The Celestial'), option('The Fathomless'), option('The Fiend'), option('The Genie'), option('The Great Old One'), option('The Hexblade'), option('The Undead'), option('School of Conjuration'), option('School of Divination'), option('School of Enchantment'), option('School of Evocation'), option('School of Graviturgy'), option('School of Illusion'), option('School of Necromancy'), option('School of Transmutation'), option('School of War Magic')):class1.subclass]` |
| **Background** | `INPUT[inlineSelect(option(Acolyte), option(Acolyte - BG), option(Anthropologist), option(Anthropologist), option(Archaeologist), option(Astral Driter), option(Athlete), option(Azorius Functionary), option(Boros Legionnair), option(Celebrity Adventurers Scion), option(Charlatan), option(Charlatan - BG), option(City Watch / Investigator), option(Clan Crafter), option(Sloistered Scholar), option(Courtier), option(Criminal - BG),  option(Criminal / Spy), option(Dimir Operative), option(Entertainer), option(Entertainter - BG), option(Faceless), option(Faction Agent), option(Failed Merchant), option(Far Traveler), option(Feylost), option(Fisher), option(Folk Hero), option(Folk Hero - BG), option(Gambler), option(Gate Warden), option(Giant Foundling), option(Gladiator), option(Golgari Agent), option(Gruul Anarch), option(Guild Artsan - BG), option( Guild Artisan / Guild Merchant), option(Haunted One), option(Hermit), option(Hermit - BG), option(House Agent - Cannith), option(House Agent - Deneith), option(House Agent - Ghallanda), option(House Agent - Jorasco), option(House Agent - Kundarak), option(House Agent - Lyrandar), option(House Agent - Medani), option(House Agent - Orien), option(House Agent - Phiarlan), option(House Agent - Sivis), option(House Agent - Tharashk), option(House Agent - Thuranni), option(House Agent - Vadalis), option(Inheritor), option(Investigator), option(Izzet Engineer), option(Knight), option(Kight of Solamnia), option(Knight of the Order), option(Lorehold Student), option(Mage of High Sorcery), option(Marine), option(Mercenary Veteran), option(Nobel), option(Nobel - BG), option(Orzhov Representative), option(Outlander), option(Outlander - BG), option(Pirate), option(Plaintiff), option(Planar Philosopher), option(Prismari Student), option(Quandrix Student), option(Rewarded), option(Rival Intern), option(Ruined), option(Rune Carver), option(Sage), option(Sage - BG), option(Sailor), option(Sailor - BG), option(Selesnya Initiate), option(Shipwright), option(Silverquill Student), option(Simic Scientist), option(Smuggler), option(Soldier), option(Soldier - BG), option(Urban Bounty Hunter), option(Urchin), option(Urchin - BG), option(Uthgardt Tribe Member), option(Waterdhavian Nobel), option(Wildspacer), option(Witchlight Hand), option(Witherbloom Student)):details.background]`       |
| **Alignment**  | `INPUT[inlineSelect(option(Lawful Good), option(Lawful Neutral), option(Lawful Evil), option(Neutral Good), option(True Neutral), option(Neutral Evil), option(Chaotic Good), option(Chaotic Neutral), option(Chaotic Evil) ):details.alignment]`        |
| **Age**        | `INPUT[number(class(very-short)):details.age]`          |
| **Height**     | **`INPUT[number(class(very-short)):details.height]` m \| `VIEW[floor({details.height}*3.281)]`' `VIEW[round(12*({details.height}*3.281-floor({details.height}*3.281)),0)]`''**     |
| **Weight**     | **`INPUT[number(class(very-short)):details.weight]` kg \| `VIEW[round(2.205*{details.weight},0)]` lbs**         |
| **Faith**      | `INPUT[text(class(long)):details.faith]`   |
> > 
> > 
>> ---
> > 
> > 
| Temp. HP| Current HP | Max HP | Hit Dice |
| ------ | ------- | -------- | --- |
| `INPUT[number(class(very-short)):combat.tempHP]` | `INPUT[number(class(very-short)):combat.currentHP]` | `INPUT[number(class(very-short)):combat.maxHP]`  | **`VIEW[{details.totalLevel} - {combat.hitDiceUSE}][math():combat.hitDiceAMOUNT]`­`VIEW[{class1.name} == 0 ? False : ({class1.name} == 1 ? "d8" : ({class1.name} == 2 ? "d12" : ({class1.name} == 3 ? "d8": ({class1.name} == 4 ? "d10": ({class1.name} == 5 ? "d8": ({class1.name} == 6 ? "d8": ({class1.name} == 7 ? "d10": ({class1.name} == 8 ? "d8": ({class1.name} == 9 ? "d10": ({class1.name} == 10 ? "d10": ({class1.name} == 11 ? "d8": ({class1.name} == 12 ? "d6": ({class1.name} == 13 ? "d8": ({class1.name} == 14 ? "d6": "None"))))))))))))))][math():combat.hitDice]`** `BUTTON[useHDid]` |
> >  
> > 
> > Conditions| Exhaustion |
| ------ | ------- | 
| `INPUT[inlineListSuggester(option(Blinded), option(Charmed), option(Deafened), option(Frightedned), option(Grappeled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious)):combat.conditions]`       |`INPUT[inlineSelect(option(0), option(1), option(2), option(3), option(4), option(5), option(6)):combat.exhaustion]`         |
> > 
> > `BUTTON[longRest_id]`
> > 
> > <br> 
> > 
> >| Success                                                                                                                                   | Fails                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| <input type="checkbox" unchecked id="f1e788"> <input type="checkbox" unchecked id="2693f1"> <input type="checkbox" unchecked id="ba2be0"> | <input type="checkbox" unchecked id="2202df"> <input type="checkbox" unchecked id="91c144"> <input type="checkbox" unchecked id="f15531"> |
> >
> > 
> 
> > [!div|clean no-i no-t] 
> > > [!columns | s-mg  no-i no-t 3]
> > > > [!metadata|  bg-c-red no-i txt-c ] `INPUT[toggle:savingThrows.str]`STR 
> > > > ### `VIEW[{abilityScores.mod.str} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.str}-10)/2),0)][math():abilityScores.mod.str]`
> > > > `INPUT[number(class(tiny)):abilityScores.str]`
> > > 
> > > >[!metadata|no-i bg-c-blue txt-c] `INPUT[toggle:savingThrows.dex]`DEX 
> > > >### `VIEW[{abilityScores.mod.dex} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.dex}-10)/2),0)][math():abilityScores.mod.dex]`
> > > > `INPUT[number(class(tiny)):abilityScores.dex]`
> > > 
> > > > [!metadata|no-i bg-c-green txt-c] `INPUT[toggle:savingThrows.con]`CON 
> > > > ### `VIEW[{abilityScores.mod.con} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.con}-10)/2),0)][math():abilityScores.mod.con]`
> > > > `INPUT[number(class(tiny)):abilityScores.con]`
> > > 
> > > > [!metadata|no-i bg-c-purple txt-c] `INPUT[toggle:savingThrows.int]`INT 
> > > > ### `VIEW[{abilityScores.mod.con} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.con}-10)/2),0)][math():abilityScores.mod.int]`
> > > > `INPUT[number(class(tiny)):abilityScores.int]`
> > > 
> > > > [!metadata|no-i bg-c-orange txt-c] `INPUT[toggle:savingThrows.wis]`WIS 
> > > > ### `VIEW[{abilityScores.mod.wis} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.wis}-10)/2),0)][math():abilityScores.mod.wis]`
> > > > `INPUT[number(class(tiny)):abilityScores.wis]`
> > > 
> > > > [!metadata|no-i bg-c-pink txt-c] `INPUT[toggle:savingThrows.cha]`CHA
> > > > ### `VIEW[{abilityScores.mod.cha} > 0 ? "+" : "" ]`­`VIEW[round(floor(({abilityScores.cha}-10)/2),0)][math():abilityScores.mod.cha]`
> > > > `INPUT[number(class(tiny)):abilityScores.cha]`
> > 
> > <br>
> >
> > >[!infobox| wfull th]
| Expt                                       | Prof                                       | Skill           | #                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `INPUT[toggle:skills.expt.acrobatics]`     | `INPUT[toggle:skills.prof.acrobatics]`     | Acrobatics      | **`VIEW[{skills.acrobatics} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.dex}+{prof}*{skills.prof.acrobatics}+{expt}*{skills.expt.acrobatics}][math():skills.acrobatics]`**                |
| `INPUT[toggle:skills.expt.animalHandling]` | `INPUT[toggle:skills.prof.animalHandling]` | Animal Handling | **`VIEW[{skills.animalHandling} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.wis}+{prof}*{skills.prof.animalHandling}+ {expt} * {skills.expt.animalHandling}][math():skills.animalHandling]`** |
| `INPUT[toggle:skills.expt.arcana]`         | `INPUT[toggle:skills.prof.arcana]`         | Arcana          | **`VIEW[{skills.arcana} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.int}+{prof}*{skills.prof.arcana}+ {expt} * {skills.expt.arcana}][math():skills.arcana]`**                         |
| `INPUT[toggle:skills.expt.athletics]`      | `INPUT[toggle:skills.prof.athletics]`      | Athletics       | **`VIEW[{skills.athletics} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.str}+{prof}*{skills.prof.athletics}+ {expt} * {skills.expt.athletics}][math():skills.athletics]`**                |
| `INPUT[toggle:skills.expt.deception]`      | `INPUT[toggle:skills.prof.deception]`      | Deception       | **`VIEW[{skills.deception} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.cha}+{prof}*{skills.prof.deception}+ {expt} * {skills.expt.deception}][math():skills.deception]`**                |
| `INPUT[toggle:skills.expt.history]`        | `INPUT[toggle:skills.prof.history]`        | History         | **`VIEW[{skills.history} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.int}+{prof}*{skills.prof.history}+ {expt} * {skills.expt.history}][math():skills.history]`**                      |
| `INPUT[toggle:skills.expt.insight]`        | `INPUT[toggle:skills.prof.insight]`        | Insight         | **`VIEW[{skills.insight} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.wis}+{prof}*{skills.prof.insight}+ {expt} * {skills.expt.insight}][math():skills.insight]`**                      |
| `INPUT[toggle:skills.expt.intimidation]`   | `INPUT[toggle:skills.prof.intimidation]`   | Intimidation    | **`VIEW[{skills.intimidation} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.cha}+{prof}*{skills.prof.intimidation}+ {expt} * {skills.expt.intimidation}][math():skills.intimidation]`**       |
| `INPUT[toggle:skills.expt.investigation]`  | `INPUT[toggle:skills.prof.investigation]`  | Investigation   | **`VIEW[{skills.investigation} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.int}+{prof}*{skills.prof.investigation}+ {expt} * {skills.expt.investigation}][math():skills.investigation]`**    |
| `INPUT[toggle:skills.expt.medicine]`       | `INPUT[toggle:skills.prof.medicine]`       | Medicine        | **`VIEW[{skills.medicine} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.wis}+{prof}*{skills.prof.medicine}+ {expt} * {skills.expt.medicine}][math():skills.medicine]`**                   |
| `INPUT[toggle:skills.expt.nature]`         | `INPUT[toggle:skills.prof.nature]`         | Nature          | **`VIEW[{skills.nature} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.int}+{prof}*{skills.prof.nature}+ {expt} * {skills.expt.nature}][math():skills.nature]`**                         |
| `INPUT[toggle:skills.expt.perception]`     | `INPUT[toggle:skills.prof.perception]`     | Perception      | **`VIEW[{skills.perception} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.wis}+{prof}*{skills.prof.perception}+ {expt} * {skills.expt.perception}][math():skills.perception]`**             |
| `INPUT[toggle:skills.expt.performance]`    | `INPUT[toggle:skills.prof.performance]`    | Performance     | **`VIEW[{skills.performance} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.cha}+{prof}*{skills.prof.performance}+ {expt} * {skills.expt.performance}][math():skills.performance]`**          |
| `INPUT[toggle:skills.expt.persuasion]`     | `INPUT[toggle:skills.prof.persuasion]`     | Persuasion      | **`VIEW[{skills.persuasion} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.cha}+{prof}*{skills.prof.persuasion}+ {expt} * {skills.expt.persuasion}][math():skills.persuasion]`**             |
| `INPUT[toggle:skills.expt.religion]`       | `INPUT[toggle:skills.prof.religion]`       | Religion        | **`VIEW[{skills.religion} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.int}+{prof}*{skills.prof.religion}+ {expt} * {skills.expt.religion}][math():skills.religion]`**                   |
| `INPUT[toggle:skills.expt.sleightOfHand]`  | `INPUT[toggle:skills.prof.sleightOfHand]`  | Sleight of Hand | **`VIEW[{skills.sleightOfHand} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.dex}+{prof}*{skills.prof.sleightOfHand}+ {expt} * {skills.expt.sleightOfHand}][math():skills.sleightOfHand]`**    |
| `INPUT[toggle:skills.expt.stealth]`        | `INPUT[toggle:skills.prof.stealth]`        | Stealth         | **`VIEW[{skills.stealth} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.dex}+{prof}*{skills.prof.stealth}+ {expt} * {skills.expt.stealth}][math():skills.stealth]`**                      |
| `INPUT[toggle:skills.expt.survival]`       | `INPUT[toggle:skills.prof.survival]`       | Survival        | **`VIEW[{skills.survival} > 0 ? "+" : "" ]`­`VIEW[{abilityScores.mod.wis}+{prof}*{skills.prof.survival}+ {expt} * {skills.expt.survival}][math():skills.survival]`**                   |
> > 
> > <br>
> > 
> > >[!cards | no-i no-t 3]
> > > >[!recite| no-i] Passive Perception
> > > >### `VIEW[{skills.perception} + 10]`
> > >
> > > >[!recite| no-i] Passive Insight
> > > >### `VIEW[{skills.insight} + 10]`
> > >
> > > >[!recite| no-i] Passive Investigation
> > > >### `VIEW[{skills.investigation} + 10]`
> > >
> 
> > [!infobox| wfull clean]
> > > [!recite|] Class Abilities
> > > ``` dataview
LIST
FROM "1. Character Info/Class Abilities"
WHERE file.name != "Artificer Table"
> > >```
> > 
> > > [!recite] Subclass Abilities
> > > ```dataview
 LIST
 FROM "1. Character Info/Subclass Abilities"
 > > >```
 > > ---
> > 
> >   Proficiencies |     |
| ---| --- |
| **Languages** | `INPUT[inlineListSuggester(option(Abyssal), option(Aarakocra), option(Alzhedo), option(Bedine), option(Celestial), option(Chessentan), option(Chondathan), option(Common), option(Damaran), option(Dambrathan), option(Deep Speech), option(Draconic), option(Druidic), option(Dwarvish), option(Elvish), option(Giant), option(Gith), option(Gnomish), option(Goblin), option(Guran), option(Halruaan), option(Infernal), option(Illuskan), option(Kraul), option(Loxodon), option(Merfolk), option(Minotaur), option(Mulhorandi), option(Orc), option(Primordial), option(Quori), option(Riedran), option(Roushoum), option(Shaaran), option(Shou), option(Sphinx), option(Sylvan), option(Terran), option(Thieves Cant), option(Tuigan), option(Turmic), option(Uluik), option(Undercommon), option(Untheric), option(Vedalken), option(Waelan)):proficiencies.languages]` |
| **Armor**     | `INPUT[inlineListSuggester(option(Light Armor), option(Medium Armor), option(Heavy Armor), option(Shield)):proficiencies.armor]`|
| **Weapons**   | `INPUT[inlineListSuggester( option(Simple Mele Weapons), option(Simple Range Weapons), option(Martial Mele Weapons), option(Martial Ranged Weapons)):proficiencies.weapons]`|
| **Tools**     | `INPUT[inlineListSuggester(option(Alchemist Supplies), option(Brewer Supplies), option(Calligrapher Supplies), option(Carpenter Tools), option(Cartographer Tools), option(Cobbler Tools), option(Cook Utensils), option(Dice Set), option(Glassblower Tools), option(Jewler Tools), option(Leatherworker Tools), option(Mason Tools), option(Painter Supplies), option(Playing Card Set), option(Potter Tools), option(Smith Tools), option(Tinker Tools), option(Weaver Tools), option(Woodcarver Tools)):proficiencies.tools]`|
|Mounts |`INPUT[inlineListSuggester(option(Camel), option(Mule), option(Elephant), option(Horse-draft), option(Horse-riding), option(Mastiff), option(Pony), option(Warhorse)):proficiencies.mounts]`  |
> > 
> > <br>
> >
> > | Defenses      |      |
| ------------- | -------- |
| **Resistance**    | `INPUT[inlineListSuggester(option('Acid'), option('Bludgeoning'), option('Bludgeoning (nonmagical)'), option('Cold'), option('Damage Traps'), option('Spell Damage'), option('Breath (acid)'), option('Breath (cold)'), option('Breath (fire)'), option('Breath (lightning)'), option('Breath (poison)'), option('Fire'), option('Force'), option('Lightning'), option('Necrotic'), option('Piercing'), option('Piercing (nonmagical)'), option('Poison'), option('Psychic'), option('Radiant'), option('Ranged Attacks'), option('Slashing'), option('Slashing (nonmagical)'), option(Thunder)):defenses.resistance]` |
| **Immunity**      | `INPUT[inlineListSuggester(option('--Damage--'), option('Acid'), option('Bludgeoning'), option('Bludgeoning (nonmagical)'), option('Bludgeoning (Falling)'), option('Cold'), option('Fire'), option('Force'), option('Lightning'), option('Necrotic'), option('Piercing'), option('Poison'), option('Psychic'), option('Radiant'), option('Slashing'), option('Thunder'), option('--Conditions--'), option('Blinded'), option(Charmed), option(Deafend), option(Exhaustion), option(Frightened), option(Grappled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious)):defenses.immunity]` 
| **Vulnerability** | `INPUT[inlineListSuggester(option(Acid), option(Bludgeoning), option(Cold), option(Fire), option(Force), option(Lightning), option(Necrotic), option(Piercing), option(Poison), option(Psychic), option(Radiant), option(Slashing), option(Thunder))]` |


# Spellcasting `INPUT[inlineSelect(option(0, -), option(1, INT), option(2, WIS), option(3, CHA)):sca_temp]` 
> [!infobox| wfull clean]
> | Spell Ability Mod. | Spell Save DC     |  Spell Atk. Mod.   | Spells Known | 
| --- | --- | --- | --- |
|   **`VIEW[{sca} > 0 ? "+" : "" ]`­`VIEW[{sca_temp} == 0 ? "None" : round(floor(({sca}-10)/2),0)]`**  | **`VIEW[{sca_temp} == 0 ? "None" : 8+{prof}+round(floor(({sca}-10)/2),0)]`**   | **`VIEW[{sca} > 0 ? "+" : "" ]`­`VIEW[{sca_temp} == 0 ? "None" : {prof}+round(floor(({sca}-10)/2),0)]`**  | **`VIEW[{sca_temp} == 0 ? "None" : round(floor(({sca}-10)/2 + ({details.totalLevel}/2)),0)]`**

<!-- Spell Casting Math-->
`VIEW[{sca_temp} == 0 ? 0 : ({sca_temp} == 1 ? {abilityScores.int} : ({sca_temp} == 2 ? {abilityScores.wis} : {abilityScores.cha}))][math(hidden):sca]`


---



> [!columns| no-i no-t  2]+
>
>> [!recite| no-i]+ [[Cantrips]]
>> ---
>> ```dataview
TABLE  WITHOUT ID choice(spell.prepared, "✅ ", "❌ ") AS "", file.link AS "Spell",  spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type"
FROM "Resources/Spells/Cantrips"
WHERE spell.known=true
>>```
>
>> [!recite|bg-c-gray no-i]+ [[Level 1 | 1st Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots1]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 1"
WHERE spell.known=true
>>```
>
>> [!recite|bg-c-red no-i]+ [[Level 2 | 2nd Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots2]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 2"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-orange no-i]+ [[Level 3 | 3rd Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 3"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-yellow no-i]+ [[Level 4 | 4th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 4"
WHERE spell.known = true
>>``` 
>
>> [!recite|bg-c-green no-i]+ [[Level 5 | 5th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 5"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-blue no-i]+ [[Level 6  | 6th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 6"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-purple no-i]+ [[Level 7 | 7th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 7"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-pink no-i]+ [[Level 8 | 8th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 8"
WHERE spell.known = true
>>```
>
>> [!recite|bg-c-black no-i]+ [[Level 9 | 9th Level]]
>>  `INPUT[slider(minValue(0), maxValue(1), addLabels):spells.slots3]`
>> ```dataview
TABLE  WITHOUT ID file.link AS "Spell" , choice(spell.prepared, "✔️ ", "❌ ") AS "", spell.school AS "School", spell.castingTime AS "Casting Time", spell.range AS "Range", spell.duration AS "Duration", spell.effect.amount AS "Amount", spell.effect.type AS "Type" 
FROM "Resources/Spells/Level 9"
WHERE spell.known = true
>>```

<!--Expertise Math-->
`VIEW[{prof}*2][math(hidden):expt]`

<!-- Level Up -->
```meta-bind-button
label: Level Up!
icon: ""
hidden: true
class: ""
tooltip: LEVEL UP!!!!!!
id: levelUpID
style: primary
actions:
  - type: updateMetadata
    bindTarget: details.totalLevel
    evaluate: true
    value: x + 1

```

<!-- Use Hit Dice -->
```meta-bind-button
label: Use
icon: ""
hidden: true
class: ""
tooltip: "Expend one hit dice."
id: useHDid
style: primary
actions:
  - type: updateMetadata
    bindTarget: combat.hitDiceUSE
    evaluate: true
    value: x + 1

```

<!-- Long Rest -->
```meta-bind-button
label: Long Rest!
icon: ""
hidden: true
class: ""
tooltip: Take a long rest to reset your hit dice and spell slots
id: longRest_id
style: primary
actions:
  - type: updateMetadata
    bindTarget: combat.hitDiceUSE
    evaluate: false
    value: "0"
  - type: updateMetadata
    bindTarget: combat.exhaustion
    evaluate: false
    value: "0"
  - type: updateMetadata
    bindTarget: spells.slots1
    evaluate: false
    value: "4"
  - type: updateMetadata
    bindTarget: spells.slots2
    evaluate: false
    value: "3"
  - type: updateMetadata
    bindTarget: spells.slots3
    evaluate: false
    value: "2"

```


<!-- Increase Proficiency Bonus -->
```meta-bind-button
label: "↑"
hidden: true
id: "increment-prof"
class: my-mb-button-down
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.prof
    evaluate: true
    value: x + 1
```

<!-- Decrease Proficiency Bonus -->
```meta-bind-button
label: "↓"
hidden: true
id: "decrement-prof"
class: my-mb-button-down
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.prof
    evaluate: true
    value: x - 1
```

<!-- Increase Speed -->
```meta-bind-button
label: "↑"
hidden: true
id: "increment-speed"
class: my-mb-button-down
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.speed
    evaluate: true
    value: x + 5
```

<!-- Decrease Speed Bonus -->
```meta-bind-button
label: "↓"
hidden: true
id: "decrement-speed"
class: my-mb-button-down
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.speed
    evaluate: true
    value: x - 5
```

<!-- Increase AC -->
```meta-bind-button
label: "↑"
hidden: true
id: "increment-ac"
class: my-mb-button-up
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.ac
    evaluate: true
    value: x + 1
```

<!-- Decrease AC -->
```meta-bind-button
label: "↓"
hidden: true
id: "decrement-ac"
class: my-mb-button-down
style: plain
actions:
  - type: updateMetadata
    bindTarget: globalMod.ac
    evaluate: true
    value: x - 1
```


