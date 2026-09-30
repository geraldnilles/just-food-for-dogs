# JustFoodForDogs Meal Calculator

A simple, single-page web app that makes it easy to calculate per-meal portions (in grams) for JustFoodForDogs Fresh Frozen daily diets **and A Pup Above Fresh, Gently Cooked recipes** — perfect for use with a digital food scale.

## What It Does

The [official JustFoodForDogs feeding guide](https://www.justfoodfordogs.com/on/demandware.static/-/Library-Sites-JustFoodForDogsSharedLibrary/default/v1f157f2dd490747058308657bb57b9d02dbaad53/pdf/2025-Feeding-Guidelines-Frozen.pdf) provides daily intake ranges in cups and ounces across weight classes, recipes, and activity levels. But those ranges can be tedious to interpret when you just want to know exactly how many grams to scoop for each meal.

This calculator does the math for you:

- **Pick your recipe** — seven JustFoodForDogs daily diets, four JustFoodForDogs Targeted Nutrition diets, or seven A Pup Above recipes
- **Set the activity level** (Low, Moderate, or High)
- **Dial in your dog's weight** via slider or text input
- **Get precise per-meal and daily amounts** in grams and ounces

The per-meal gram value is displayed prominently so you can zero your scale and scoop the exact right amount — no guessing or eyeballing required.

## How It Works

Each source guide defines anchor points at specific weight boundaries. The calculator uses **linear interpolation** between these anchors to compute a smooth, continuous daily intake estimate for any weight from 5 to 80 lbs. That daily total is then split into two equal meals.

- **JustFoodForDogs** anchors at **5, 10, 20, 40, 60, and 80 lbs**, with separate values per recipe and activity level (Low / Moderate / High).
- **A Pup Above** anchors at **5, 10, 15, 20, 30, 40, 50, 60, 70, and 80 lbs**. A Pup Above publishes a single chart that applies to all seven recipes (a patty is standardized at 1 lb), and it is **not** broken out by activity level — so the same amount applies at every activity level.

### Supported Recipes

**JustFoodForDogs — Daily Diets**

| Recipe                        |
|-------------------------------|
| Beef & Russet Potato          |
| Chicken & Rice                |
| Fish & Sweet Potato           |
| Lamb & Brown Rice             |
| Tofu & Quinoa                 |
| Turkey & Whole Wheat Macaroni |
| Venison & Squash              |

**JustFoodForDogs — Targeted Nutrition**

| Recipe                    |
|---------------------------|
| Healthy Weight            |
| Joint & Skin              |
| Sensitive Skin            |
| Balanced Remedy           |

**A Pup Above — Fresh, Gently Cooked**

| Recipe                          |
|---------------------------------|
| Chicka Chicka Bow Wow (Chicken) |
| Turkey Pawella (Turkey)         |
| Texas Beef Stew (Beef)          |
| Porky's Luau (Pork)             |
| Turducken (Poultry Blend)       |
| Fish Gone Wild (Fish)           |
| Puppy Recipe                    |

### Activity Levels

- Low
- Moderate
- High

Activity levels apply to the JustFoodForDogs charts. A Pup Above publishes a single chart for all recipes that does not vary by activity level, so the activity selector is disabled while an A Pup Above recipe is selected.

## Usage

Open `index.html` in any modern browser — no build step, no server, no dependencies (beyond Tailwind CSS loaded via CDN). It works offline once loaded.

For convenience, it's also hosted via GitHub Pages at:

**[geraldnilles.github.io/just-food-for-dogs](https://geraldnilles.github.io/just-food-for-dogs)**

## Source Data

The feeding values are derived from two sources:

- **2025 JustFoodForDogs Feeding Guidelines for Fresh Frozen Daily Diets** (Revision 25.4.1). A copy of the source PDF is included in this repository: [`2025-Feeding-Guidelines-Frozen.pdf`](./2025-Feeding-Guidelines-Frozen.pdf)
- **A Pup Above feeding guidelines** — "How Much Should My Dog Eat? Feeding Charts by Weight": <https://apupabove.com/blogs/all/how-much-food-should-my-dog-eat>

> **Disclaimer:** The charts are only a guide. Always adjust feeding recommendations based on careful monitoring of your dog's weight. This calculator is not affiliated with or endorsed by JustFoodForDogs or A Pup Above.

## License

MIT © 2026 Gerald Nilles — see [LICENSE](./LICENSE) for details.
