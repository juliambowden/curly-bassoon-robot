---

hero_image: /images/hero.jpg
<!-- hero_height: is-fullwidth -->
hero_darken: true

---

# Installing and Running

The most common way to run the Studio is from a PhysiCell root directory. Of course you can always download just the Studio and explore (File->Open) the example .xml configuration files (in its /config folder), however, without an executable model, you won't be able to run a simulation and plot results. Therefore, for this Guide, we assume you have installed
PhysiCell and have compiled a sample model (rf. the [latest workshop slides](https://github.com/physicell-training/ws2023/blob/main/agenda.md)). (In the terminal command lines shown below, PhysiCell has been installed into a directory `~/PhysiCell`, but yours may be something different depending how you installed it). To download the Studio and have it be installed in its own
directory inside the PhysiCell directory, click this link and download the `get_studio.py`:

* https://github.com/PhysiCell-Tools/PhysiCell-Studio/blob/main/get_studio.py 

![](./images/download_get_studio.png)

Then run the script:
```
~/PhysiCell$ python get_studio.py
```

It will download and install the latest version of the Studio into a directory called `studio` within your PhysiCell directory. The `get_studio.py` script will also print out sample commands for running the Studio, e.g.:

```
~/PhysiCell$ python studio/bin/studio.py    # by default, try to load config/PhysiCell_settings.xml and use "project" as executable
or,
~/PhysiCell$ python studio/bin/studio.py -c <config_file.xml> -e <executable_program>   # be explicit about the config file and executable
and,
~/PhysiCell$ python studio/bin/studio.py --help
```

Note:
* there are ways to create an alias and/or a symbolic link to make it easier to run the Studio
* you may need to prefix your executable name with `./`, depending on your PATH environment variable
* this guide will use a Unix-style command syntax; Windows syntax will differ slightly (e.g., you will need a ".exe" suffix on the executable program name)

It is important to understand that the XML configuration file you are editing in the Studio will be updated (overwritten) when you do `File->Save` or *when you Run a simulation*. Also, the rules you have in your Rules table will automatically be written to the folder/file you have specified in that tab. But the ICs requires that you explicitly `Save` to the .csv file from the ICs tab. The Studio does not do "instantaneous" updates to the XML, so if it encounters a fatal error and crashes, any changes you made will not be automatically saved. Neither does it track changes you made and warn you of unsaved changes when you quit the Studio. Therefore, if you are working on your own model, it is a good practice to `File->Save` (has keyboard shortcut) occasionally and adopt the habit of making backup copies of any files you consider critical.
