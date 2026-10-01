# 🌻 Garden Centre – Seed Shop (Java OOP)

A console-based shopping application for a garden centre that sells flower seeds.
Built individually for the **Programming – Object Oriented Approach** module (Year 1, CCT College Dublin), completed in May 2024.

## Overview
Users can browse available seeds, view detailed plant information, add items to a
shopping trolley with a chosen quantity, remove items, and proceed to checkout
with a running total. Stock levels update in real time as items are added.

## Features
- Interactive console menu with input validation and error messages
- Quantity selection with stock checking (can't buy more than is available)
- Live trolley view showing selected items and total spend
- "More Information" option showing each plant's scientific name, type, height,
  sowing and flowering seasons, and description
- Remove items from the trolley
- Checkout summary with the option to return to the shop

## OOP Concepts Demonstrated
- **Abstraction** – `Seeds` is an abstract parent class defining shared properties
  and an abstract `buy()` method
- **Inheritance** – `Sunflower`, `Poppy`, `Daisy`, `Lily` and `Lavander` extend `Seeds`
- **Polymorphism** – each subclass overrides `buy()`; items are stored and handled
  as a single `ArrayList<Seeds>`
- **Encapsulation** – private fields accessed through getters, with stock changed
  only via `reduceStock()`

## Project Structure
- `gardencentre/GardenCentre.java` – entry point (main method)
- `gardencentre/ShoppingTrolley.java` – menu, trolley and checkout logic
  (extended from starter code provided for the module)
- `seeds/Seeds.java` – abstract parent class
- `seeds/Sunflower.java`, `Poppy.java`, `Daisy.java`, `Lily.java`, `Lavander.java` – product classes

## Tech
Java · Apache Ant · NetBeans

## How to Run
You need Java 8 or later.

Run the packaged app:
```bash
java -jar GardenCentre_CA.jar
```

Or compile and run from source:
```bash
mkdir out
javac -d out gardencentre/*.java seeds/*.java
java -cp out gardencentre.GardenCentre
```

## Notes and known limitations
- This is a Year 1 project and is kept as it was submitted.
- The project was uploaded to GitHub in 2026. The commit that adds the source code is dated 21 May 2024, when the app was completed.
- The lavender class is spelled `Lavander` in the code.
- Stock and the trolley are kept in memory, so they reset each time the app starts.

## Credits
Plant information sourced from Seeds Ireland (seedsireland.ie).
