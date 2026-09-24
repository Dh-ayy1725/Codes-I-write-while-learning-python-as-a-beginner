# Codes-I-write-while-learning-python-as-a-beginner

#Top 3 DPS
Skirk = {
"name" : "Skirk",
"level" : 90,
"hp" : 19780,
"attack" : 2340,
"defence" : 700,
"class" : "cryo",
"crit_rate" : 4,
"crit_dmg" : 70
}

Mavuika = {
"name" : "Mavuika",
"level" : 90,
"hp" : 20567,
"attack" : 2150,
"defence" : 890,
"class" : "pyro",
"crit_rate" : 3,
"crit_dmg" : 80
}

Lan_yan = {
"name" : "Lan yan",
"level" : 100,
"hp" : 18560,
"attack" : 3250,
"defence" : 930,
"class" : "anemo",
"crit_rate" : 2,
"crit_dmg" : 90
}

def character_info(character):
	for key, values in character.items():
		print(key, ":", values)
		
				
character_info(Skirk)

def skirk_fight(character):
	if character["attack"] > Skirk["attack"]:
		print(character["name"], "is stronger")
		
	
	attack_value_skirk = 3
	skill_dmg_character = character["attack"] * character["crit_rate"] / character["crit_dmg"] * 100
	skill_dmg_skirk = Skirk["attack"] * Skirk["crit_rate"] / Skirk["crit_dmg"] * 100
	attack_value_character = int(input("How many slashes do the character make?"))
	if attack_value_character >= attack_value_skirk:
		print(skill_dmg_character)
		print(skill_dmg_skirk)
		
	else:
		print(character["name"],"is weaker than skirk, Skirk won")
		
	if skill_dmg_character > skill_dmg_skirk:
			print(character["name"],"is stronger than skirk",character,"wins")
	else:
		print(character["name"],"wins")
		
		
skirk_fight(Lan_yan)
		

