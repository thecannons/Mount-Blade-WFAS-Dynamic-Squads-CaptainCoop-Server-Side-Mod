NOTE: The main files I've edited where the core of the mod works is module_scripts.py, module_mission_templates.py, module_scene_props.py. For custom maps its: module_scenes.py


Instructions:
To host a dedicated server visit: https://forums.taleworlds.com/index.php?threads/hosting-a-dedicated-server-guide.113653/

WFAS dedicaated server files found here: https://www.taleworlds.com/en/Games/FireAndSword

Direct link to dedicated files: http://download.taleworlds.com/mb_wfas_dedicated_1143.zip

The dedicated server files are setup like your client game installation, the difference is you're configuring them. The config files you need for Captain coop can be found here: https://github.com/Daimyo21/Mount-Blade-WFAS-Dynamic-Squads-CaptainCoop-Server-Side-Mod/tree/master/Server%20Related%20Files%20and%20Maps

Sample_Captain_Coop.txt is the config file, replace your existing one in the dedicated server directory.

Sample_Captain_Coop_start.bat is a startup file, place this in the main directory.
  
You can remove these flags if you want, they set the CPU to use etc as well as priority for program. /affinity 20 /abovenormal 


WFAS Custom Maps.zip can be extracted into your C:\Mount&Blade With Fire and Sword Dedicated\Modules\Ogniem i Mieczem\SceneObj directory. Make sure you backup existing sceneobjs. To use these custom maps, add them to rotation via Sample_Captain_Coop.txt (should be there by default)

Finally, to build my custom module system to your dedicated server files, you need to download Python. I use Python 2.7.6 https://www.python.org/downloads/release/python-276/

Install it and in windows, Edit Path variable "Path" and add C:\Python27;  Follow instructions here if you're not sure: https://forums.taleworlds.com/index.php?threads/guide-editing-and-building-the-module-system.264025/

These instructions are all you need to mod. The bread and butter is the last part but here is for my server:

Set up your module directory and build to it:
In the module system directory, open module_info.py and change the export dir variable to be the path of your module directory, using forward slashes (/) to separate directories rather than back slashes (\). For example, you might set it to this:
export_dir = "C:/Mount&Blade With Fire and Sword Dedicated/Modules/Ogniem i Mieczem/"
Double click build_module.bat in the module system directory.


So quick recap:
Download official WFAS dedicated server files and extract somewhere
Download and install Python, I use 2.7.6, setup windows path variable
Download my custom module here, extract in a separate directory, configure the module_info.py to your dedicated server files "Ogniem i Mieczem" directory. Run build_module.bat
Download WFAS Custom Maps.zip and extract into C:\Mount&Blade With Fire and Sword Dedicated\Modules\Ogniem i Mieczem\SceneObj
Place sample Sample_Captain_Coop.txt and Sample_Captain_Coop_start.bat in main dedicated server files directory. Configure Sample_Captain_Coop.txt and run the Sample_Captain_Coop_start.bat


