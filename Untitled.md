---
character_name: 
player_name: 
class: 
level: 
race: 
background: 
alignment: 
experience_points: 
---

# 📊 Core Stats

> [!info]- Ability Scores & Modifiers
> - Strength: `= this.strength` (Mod: `= floor((this.strength - 10) / 2)`)
> - Dexterity: `= this.dexterity` (Mod: `= floor((this.dexterity - 10) / 2)`)
> - Constitution: `= this.constitution` (Mod: `= floor((this.constitution - 10) / 2)`)
> - Intelligence: `= this.intelligence` (Mod: `= floor((this.intelligence - 10) / 2)`)
> - Wisdom: `= this.wisdom` (Mod: `= floor((this.wisdom - 10) / 2)`)
> - Charisma: `= this.charisma` (Mod: `= floor((this.charisma - 10) / 2)`)

strength::
dexterity::
constitution::
intelligence::
wisdom::
charisma::

# ❤️ Health & Defense

> [!info]- Combat Stats
> - Hit Points: `= this.current_hp`/`= this.max_hp`
> - Armor Class: `= this.armor_class`
> - Initiative: `= this.initiative`
> - Speed: `= this.speed`
> - Hit Dice: `= this.hit_dice`

current_hp::
max_hp::
armor_class::
initiative::
speed::
hit_dice::

# 🎯 Skills & Proficiencies

> [!info]- Saving Throws
> Mark proficient saves with (P)
> - Strength: `= floor((this.strength - 10) / 2) + (this.str_save_prof * this.proficiency_bonus)`
> - Dexterity: `= floor((this.dexterity - 10) / 2) + (this.dex_save_prof * this.proficiency_bonus)`
> - Constitution: `= floor((this.constitution - 10) / 2) + (this.con_save_prof * this.proficiency_bonus)`
> - Intelligence: `= floor((this.intelligence - 10) / 2) + (this.int_save_prof * this.proficiency_bonus)`
> - Wisdom: `= floor((this.wisdom - 10) / 2) + (this.wis_save_prof * this.proficiency_bonus)`
> - Charisma: `= floor((this.charisma - 10) / 2) + (this.cha_save_prof * this.proficiency_bonus)`

proficiency_bonus::
str_save_prof:: 0
dex_save_prof:: 0
con_save_prof:: 0
int_save_prof:: 0
wis_save_prof:: 0
cha_save_prof:: 0

> [!info]- Skills
> Mark proficient skills with (P)
> ### Strength
> - Athletics: `= floor((this.strength - 10) / 2) + (this.athletics_prof * this.proficiency_bonus)`
> 
> ### Dexterity
> - Acrobatics: `= floor((this.dexterity - 10) / 2) + (this.acrobatics_prof * this.proficiency_bonus)`
> - Sleight of Hand: `= floor((this.dexterity - 10) / 2) + (this.sleight_of_hand_prof * this.proficiency_bonus)`
> - Stealth: `= floor((this.dexterity - 10) / 2) + (this.stealth_prof * this.proficiency_bonus)`
> 
> ### Intelligence
> - Arcana: `= floor((this.intelligence - 10) / 2) + (this.arcana_prof * this.proficiency_bonus)`
> - History: `= floor((this.intelligence - 10) / 2) + (this.history_prof * this.proficiency_bonus)`
> - Investigation: `= floor((this.intelligence - 10) / 2) + (this.investigation_prof * this.proficiency_bonus)`
> - Nature: `= floor((this.intelligence - 10) / 2) + (this.nature_prof * this.proficiency_bonus)`
> - Religion: `= floor((this.intelligence - 10) / 2) + (this.religion_prof * this.proficiency_bonus)`
> 
> ### Wisdom
> - Animal Handling: `= floor((this.wisdom - 10) / 2) + (this.animal_handling_prof * this.proficiency_bonus)`
> - Insight: `= floor((this.wisdom - 10) / 2) + (this.insight_prof * this.proficiency_bonus)`
> - Medicine: `= floor((this.wisdom - 10) / 2) + (this.medicine_prof * this.proficiency_bonus)`
> - Perception: `= floor((this.wisdom - 10) / 2) + (this.perception_prof * this.proficiency_bonus)`
> - Survival: `= floor((this.wisdom - 10) / 2) + (this.survival_prof * this.proficiency_bonus)`
> 
> ### Charisma
> - Deception: `= floor((this.charisma - 10) / 2) + (this.deception_prof * this.proficiency_bonus)`
> - Intimidation: `= floor((this.charisma - 10) / 2) + (this.intimidation_prof * this.proficiency_bonus)`
> - Performance: `= floor((this.charisma - 10) / 2) + (this.performance_prof * this.proficiency_bonus)`
> - Persuasion: `= floor((this.charisma - 10) / 2) + (this.persuasion_prof * this.proficiency_bonus)`

# ⚔️ Attacks & Spellcasting

> [!info]- Weapons & Attacks
> | Name | Attack Bonus | Damage | Type |
> |------|--------------|--------|------|
> |      |              |        |      |
> |      |              |        |      |
> |      |              |        |      |

> [!info]- Spellcasting
> - Spellcasting Ability:
> - Spell Save DC: `= 8 + this.proficiency_bonus + floor((this.spellcasting_ability - 10) / 2)`
> - Spell Attack Bonus: `= this.proficiency_bonus + floor((this.spellcasting_ability - 10) / 2)`

spellcasting_ability::

# 🎒 Equipment & Currency

> [!info]- Currency
> - Platinum (PP): 
> - Gold (GP): 
> - Electrum (EP): 
> - Silver (SP): 
> - Copper (CP): 

> [!info]- Inventory
> | Item | Quantity | Weight |
> |------|----------|--------|
> |      |          |        |
> |      |          |        |
> |      |          |        |

# 📜 Features & Traits

> [!info]- Character Features
> #### Racial Features
> 
> 
> #### Class Features
> 
> 
> #### Background Features
> 
> 
> #### Feats
> 

# 📖 Character Details

> [!info]- Personality
> #### Personality Traits
> 
> #### Ideals
> 
> #### Bonds
> 
> #### Flaws
> 

> [!info]- Background
> #### Appearance
> 
> #### Backstory
> 

# 📝 Notes

> [!info]- Campaign Notes
>