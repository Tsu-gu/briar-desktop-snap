The notifications and consequently the notification sound is broken.

The most notable part of the snap is:

```
    environment:
     BRIAR_DATA_DIR: $SNAP_USER_DATA/.briar
     _JAVA_OPTIONS: -Djava.util.prefs.userRoot=$SNAP_USER_DATA/.java/.userPrefs
```

Briar doesn't respect $HOME and uses its own variable. The _JAVA_OPTIONS is necessary for storing and reading user settings.
