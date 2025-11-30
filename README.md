The notifications and consequently the notification sound is broken. I tried adding some extra stage packages but they had no effect so I removed them.

The most notable part of the snap is:

```
    environment:
     BRIAR_DATA_DIR: $SNAP_USER_DATA/.briar
     _JAVA_OPTIONS: -Djava.util.prefs.userRoot=$SNAP_USER_DATA/.java/.userPrefs
```

Briar doesn't respect $HOME and uses its own variable. The _JAVA_OPTIONS is necessary for storing and reading user settings.

I'm using core2**2** because the latest .deb file was for Ubuntu 22.04 at the time of making and I didn't want to risk incompatibility. They still produce 20.04 debs so I think I'm good for a while.
