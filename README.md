# mc2mt
Convert maps from Minecraft to Minetest

## Dependencies
Quarry library is used to decode nbt format \
`pip install quarry` \
https://github.com/barneygale/quarry

## Usage
usage: mc2mt.py [-h] [--json JSON] input output

positional arguments:
  input                 Minecraft input world folder
  output                Output folder for the generated Minetest world

optional arguments:
  -h, --help            show this help message and exit
  --json JSON, -j JSON  Path to a folder containing dictionary lookup for block ids

Json lookup table is generated by running Minecraft server. \
You may create one like so: `java -cp minecraft_server.jar net.minecraft.data.Main --reports`. \
Files are generated under"./generated/reports". \
More details at https://quarry.readthedocs.io/en/latest/data_types/registry.html

## Unknown Block
All unknown block will be replaced with air.
The block conversion is made by [block_conversion.py](block_conversion.py) 
Have a look at it and if you want to improve it, please send me a pull request

