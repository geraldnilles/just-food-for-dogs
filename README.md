# JustFoodForDogs Meal Calculator

A simple, single-page web app that makes it easy to calculate per-meal portions (in grams) for JustFoodForDogs Fresh Frozen daily diets — perfect for use with a digital food scale.

## What It Does

The [official JustFoodForDogs feeding guide](https://www.justfoodfordogs.com/on/demandware.static/-/Library-Sites-JustFoodForDogsSharedLibrary/default/v1f157f2dd490747058308657bb57b9d02dbaad53/pdf/2025-Feeding-Guidelines-Frozen.pdf) provides daily intake ranges in cups and ounces across weight classes, recipes, and activity levels. But those ranges can be tedious to interpret when you just want to know exactly how many grams to scoop for each meal.

This calculator does the math for you:

- **Pick your recipe** (Beef, Chicken, Fish, Lamb, Tofu, Turkey, or Venison)
- **Set the activity level** (Low, Moderate, or High)
- **Dial in your dog's weight** via slider or text input
- **Get precise per-meal and daily amounts** in grams and ounces

The per-meal gram value is displayed prominently so you can zero your scale and scoop the exact right amount — no guessing or eyeballing required.

## How It Works

The feeding guide defines anchor points at specific weight boundaries (5, 11, 21, 41, and 61 lbs). The calculator uses **linear interpolation** between these anchors to compute a smooth, continuous daily intake estimate for any weight from 5 to 80 lbs. That daily total is then split into two equal meals.

### Supported Recipes

| Recipe                        |
|-------------------------------|
| Beef & Russet Potato          |
| Chicken & Rice                |
| Fish & Sweet Potato           |
| Lamb & Brown Rice             |
| Tofu & Quinoa                 |
| Turkey & Whole Wheat Macaroni |
| Venison & Squash              |

### Activity Levels

- Low
- Moderate
- High

## Usage

Open `index.html` in any modern browser — no build step, no server, no dependencies (beyond Tailwind CSS loaded via CDN). It works offline once loaded.

For convenience, it's also hosted via GitHub Pages at:

**[nilles.github.io/just-food-for-dogs](https://nilles.github.io/just-food-for-dogs)**

## Source Data

The feeding values are derived from the **2025 JustFoodForDogs Feeding Guidelines for Fresh Frozen Daily Diets** (Revision 25.4.1). A copy of the source PDF is included in this repository:

- [`2025-Feeding-Guidelines-Frozen.pdf`](./2025-Feeding-Guidelines-Frozen.pdf)

> **Disclaimer:** The charts are only a guide. Always adjust feeding recommendations based on careful monitoring of your dog's weight. This calculator is not affiliated with or endorsed by JustFoodForDogs.

## License

MIT © 2026 Gerald Nilles — see [LICENSE](./LICENSE) for details.
