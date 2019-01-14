# LPAC Sandbox Launcher


## Screenshot:
![](https://raw.githubusercontent.com/WildByDesign/Privexec/master/LPAC%20Launcher.png)


## Details:

## Important Capabilities for LPAC (minimum)

- lpacCom
- lpacAppExperience
- registryRead


## Event Viewer

Applications and Services Logs > Microsoft > Windows > Security-LessPrivilegedAppContainer > Operational

* some activity, but not much detail yet. Likely more detail in future Windows releases


## LPAC File System Access

LPAC is essentially Default Deny AppContainer.  You need to give it permissions via capabilities and more.

Some example "icacls" commands:

```
icacls D:\* /grant *S-1-15-2-2:(OI)(CI)(RX) /T
```

S-1-15-2-2 = ALL RESTRICTED APPLICATION PACKAGES = LPAC

(RX) gives Read & Execute access.
(M) gives Modify access.
(F) gives Full access.


(more details to update later)


## LICENSE

This project use MIT License, and JSON use [https://github.com/nlohmann/json](https://github.com/nlohmann/json) , some API use NSudo, but rewrite it.
