# SDGyroDSU-nixos

SDGyroDSU packaged for NixOS.
This package is based on 
https://github.com/Jovian-Experiments/Jovian-NixOS
https://github.com/kmicki/SteamDeckGyroDSU

## Installing the flake

```nix
# flake.nix
inputs = {
    sdgyrodsu.url = "github:GrigoryKuchinskij/sdgyrodsu-nixos";
};
```

```nix
# configuration.nix

programs.nix-ld.enable = true;

environment.systemPackages = with pkgs; [
    sdgyrodsu
];
```

## Running installed program

```bash
sdgyrodsu
```

## Running program from flake

```bash
nix shell github:GrigoryKuchinskij/sdgyrodsu-nixos#sdgyrodsu
sdgyrodsu
```
