To install directly from this, first build the package:
```
nix-build -E 'with import <nixpkgs> { overlays = [ (import ./redot-overlay.nix) ]; }; pkgs.redot' --keep-failed
```
This builds from source, then you have to add it to your nix-env:
```
nix-env -i ./result
```
alternatively you can import the redot-overlay.nix to your configuration.nix file 
