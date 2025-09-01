# AP_Environmental_Science
Quick program to quiz myself on biomes


import random

# Dictionary of biomes
biomes = {
    "tundra": {
        "temp": "cold",
        "precipitation": "low",
        "latitude": "high",
        "biomass": "low",
        "soil": "permafrost",
        "decomposition": "very slow",
        "limiting nutrient": "nitrogen and phosphorous",
        "leaching": "minimal"
    },
    "taiga": {
        "temp": "cold",
        "precipitation": "moderate",
        "latitude": "high",
        "biomass": "high",
        "soil": "acidic",
        "decomposition": "slow",
        "limiting nutrient": "nitrogen",
        "leaching": "minimal"
    },
    "temperate rainforest": {
        "temp": "mild",
        "precipitation": "high",
        "latitude": "mid",
        "biomass": "very high",
        "soil": "nutrient rich",
        "decomposition": "moderate",
        "limiting nutrient": "nitrogen",
        "leaching": "high"
    },
    "temperate grassland": {
        "temp": "moderate",
        "precipitation": "moderate",
        "latitude": "mid",
        "biomass": "high",
        "soil": "fertile",
        "decomposition": "rapid",
        "limiting nutrient": "nitrogen",
        "leaching": "moderate"
    },
    "temperate seasonal forest": {
        "temp": "swings",
        "precipitation": "moderate",
        "latitude": "mid",
        "biomass": "high",
        "soil": "fertile",
        "decomposition": "moderate",
        "limiting nutrient": "nitrogen and phosphorous",
        "leaching": "moderate"
    },
    "tropical rainforest": {
        "temp": "hot",
        "precipitation": "high",
        "latitude": "low",
        "biomass": "high",
        "soil": "nutrient poor",
        "decomposition": "rapid",
        "limiting nutrient": "nitrogen and phosphorous",
        "leaching": "extreme"
    },
    "shrubland": {
        "temp": "hot",
        "precipitation": "low",
        "latitude": "mid",
        "biomass": "moderate",
        "soil": "nutrient poor",
        "decomposition": "slow",
        "limiting nutrient": "water",
        "leaching": "low"
    },
    "savanna": {
        "temp": "hot",
        "precipitation": "seasonal",
        "latitude": "low",
        "biomass": "mid-high",
        "soil": "fertile",
        "decomposition": "fast",
        "limiting nutrient": "nitrogen and water",
        "leaching": "moderate"
    },
    "desert": {
        "temp": "hot",
        "precipitation": "no",
        "latitude": "low",
        "biomass": "low",
        "soil": "nutrient poor",
        "decomposition": "very slow",
        "limiting nutrient": "water",
        "leaching": "minimal"
    }
}

# Quiz loop
while True:
    biome = random.choice(list(biomes.keys()))
    attribute = random.choice(list(biomes[biome].keys()))
    
    print(f"\n🌍 Biome: {biome}")
    guess = input(f"What is the '{attribute}' of this biome? ")
    
    correct = biomes[biome][attribute]
    print(f"Correct answer: {correct}")

    if guess == correct:
        print("✅ You got it right!")
    else:
        print("Try again!")
    
    again = input("\nDo you want another question? (y/n): ")
    if again.lower() != "y":
        print("Good job studying! 📚")
        break
