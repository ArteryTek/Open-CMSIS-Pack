# Open-CMSIS-Pack
## How to use
You can use the vidx2pidx utility to create your own index.pidx file. Once created, you can use it with cpackget to install the packs listed in the PIDX file. 

The vidx2pdix and cpackget utilities are included in the cmsis-toolbox package and can be found in the installation directory of Keil or other supported IDEs.

Follow these steps to run the conversion and installatin:
Download ArteryTek.vidx to your PC local disk.

Run
```bash
vidx2pidx ArteryTek.vidx
```
to create the index.pidx.

Run
```bash
cpackget init -R packroot index.pidx
```
to create a new pack root directory with only the packs from the index.pidx.

Run
```bash
cpackget list -p -R packroot
```
to show all packs and check if the process was successful.

Install listed packs
Run
```bash
cpackget add <packID> -R packroot
```
to check if all packs can be downloaded and installed.
