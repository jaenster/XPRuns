
# XPRuns
Here is a script that does a teamed xp run
Assuming you know what your doing this is quite easy to setup.

It runs a teamed XPRun.
Currently its allot faster as the default Baal and BaalHelper/Assistant script available.
The *diablo* script is in development, and not that good. I advice you to currently use this to do a teamed Mephisto/Nihlathak/Baal run.

This script uses the *Config.Leader* However, it can chance within the script. Make sure you set this up and not make it empty.
Leave it empty on the actual leader

Make sure your chars use fieldID





### Instructions:
Add something like this to your config files (your chars). Note its case sensitive. So if you are a *traspin*, make sure its a *Trapsin* ;) If your char tele's, make sure you type *Tele* and so on.
```

    Scripts.XPRun = true;
      // General Settings
		  Config.XPRun.Char.type = '';					    // The type. Can be Trapsin, Warcry, Javazon, Curse, Eledruid, Hammerdin, Blizzy, Lightsorc, Smiter
      Config.XPRun.baalFirst = false;           // Doing baal first? Most quick runs to do baal first. (saves about 20 seconds each run)
      Config.XPRun.weak = false;                // Dont worry, the script figures this out himself. However, if set on true its overruled

      // Baal settings
		  Config.XPRun.Baal.do = false; 						// Do a baalrun
		  Config.XPRun.Baal.type = '';					    // Helper or Tele to throne? (Multiple chars can tele) <-- best to have multiple

		  // Nihlathak settings
		  Config.XPRun.Nihlathak.do = false;				// Do Nihlathak as a team
		  Config.XPRun.Nihlathak.type = '';		    	// Helper or Tele? (Multiple chars can tele). Best practice is one

		  // Diablo settings
		  Config.XPRun.Diablo.do = false;					  // Do a diarun or not?
		  Config.XPRun.Diablo.type = '';		        // Helper or tele to chaos? If doing
		  Config.XPRun.Diablo.fast = false;					// Not supported yet, leave it on false.

		  // Mehpisto settings
		  Config.XPRun.Mephisto.do = false ;				// Do a mephisto run?
		  Config.XPRun.Mephisto.type = '';		      // Tele or help?
```

* This should go somewhere in *d2bs/kolbot/libs/common/Config.js*:

```
  XPRun: {
        Char: {
            weak: true,
            type: ''
        },
        Bo: {
            do: true,
            type: '',
            receivers: []
        },
		Baal:  {
        	do: true,
        	type: ''
		},
        Nihlathak: {
            do: true,
            type: ''
        },
		Diablo: {
        	do: true,
			type: '',
			fast: false
		},
		Mephisto: {
        	do: true,
        	type: ''
		},
		baalFirst: true
	}
```

* Oh, and save *XPRun.js* in *d2bs/kolbot/libs/bots/* of course.

### Other stuff
Make sure your kolbot\data\ files are cleaned up. Throw away the old .json files. The script sees who is ingame and what is there profile name. However, due to the limitation of javascript i can't see which profiles are running in the manager. To by pass this, please clear out the data folder so no old json files of other older profiles are still listed in here.


### Licence:
**Beerware licence**
