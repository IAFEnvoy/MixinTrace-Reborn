# MixinTrace Reborn

This is a fork and continuation version of MixinTrace
([CurseForge](https://www.curseforge.com/minecraft/mc-mods/mixintrace) | [Modrinth](https://modrinth.com/mod/mixintrace)),
a mod that can print all mixins applied to a class in the stacktrace when a crash happens. It is very useful for mod
developers to find out which mods are applying mixins to the class in the stacktrace, and it can also be used by players
to report mod conflicts.

This fork add support for 26.1+ which no longer use obfuscated names, and also add support for Forge and Neoforge.

**Note: Mod logically support all versions of Minecraft, if you find any incompatibility issues please report.**

## Example output

### 1.21.11- on Forge / Fabric

```
Mixins in Stacktrace: 
    net.minecraft.class_465:
        com.example.examplemod.mixin.ExampleMixin (examplemod.mixins.json)
Notice: Minecraft running in obfuscate mode. You may need to use some tools to find out the exact class name.
```

### 26.1+ / NeoForge

```
Mixins in Stacktrace: 
    net.minecraft.client.gui.screens.inventory.AbstractContainerScreen:
        com.example.examplemod.mixin.ExampleMixin (examplemod.mixins.json)
```