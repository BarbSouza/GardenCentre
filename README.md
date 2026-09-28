# GardenCentre
Console-based Java shopping app for a garden centre seed shop. Demonstrates OOP principles (abstract classes, inheritance, encapsulation, method overriding) with stock tracking, trolley management and checkout. 1st-year CA, CCT College Dublin.

# 🌻 Garden Centre – Seed Shop (Java OOP)

A console-based shopping application for a garden centre that sells flower seeds.
Built as my Year 1 Object-Oriented Programming assessment at CCT College Dublin (2024).

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
- **Inheritance** – `Sunflower`, `Poppy`, `Daisy`, `Lily` and `Lavender` extend `Seeds`
- **Polymorphism** – each subclass overrides `buy()`; items are stored and handled
  as a single `ArrayList<Seeds>`
- **Encapsulation** – private fields accessed through getters, with stock changed
  only via `reduceStock()`

## Project Structure
- `gardencentre/GardenCentre.java` – entry point (main method)
- `gardencentre/ShoppingTrolley.java` – menu, trolley and checkout logic
  (extended from starter code provided for the module)
- `seeds/Seeds.java` – abstract parent class
- `seeds/Sunflower.java`, `Poppy.java`, `Daisy.java`, `Lily.java`, `Lavender.java` – product classes

## Tech
Java · Apache Ant · NetBeans

## How to Run
java -jar GardenCentre_CA.jar

## Credits
Plant information sourced from Seeds Ireland (seedsireland.ie).
