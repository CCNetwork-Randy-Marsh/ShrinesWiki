## How to run Shrines data generator

### Use the pre-generated Data for each release:

- Open GitHub [here](https://github.com/Silverminer007/Shrines/releases)
- Select a release for 1.18.2 or above
- Download "Shrines-Default-Config-{version}.zip"

### Generate the files yourself:

For more information about the data-generator see [here](https://minecraft.fandom.com/wiki/Tutorials/Running_the_data_generator)

1. Clone Shrines locally: Run `git clone https://github.com/Silverminer007/Shrines.git` (This step might take a while)
2. Run `cd Shrines`
3. Run the generator
   1. If you want to create worldgen files:
      1. run `./gradlew runWorldGenData` or `gradlew runWorldGenData` on Windows systems (This step might take a while)
      2. run `cd src/generated/reports/reports/worldgen/shrines/worldgen`
   2. If you want to generate tags:
      1. run `./gradlew runGenerateData` or `gradlew runGenerateData` on Windows systems (This step might take a while)
      2. run `cd src/generated/resources/data/shrines/tags/worldgen`