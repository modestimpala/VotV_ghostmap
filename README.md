# Voices of the Void editor recreation for ghostreferencing

> Currently targets game version: `a09j_0001`

This is an automatically generated, 1:1 accurate recreation of Voices of the Void assets for version `a09j_0001`.

## What this includes
- Every single asset accurately recreated down to component/widget hierarchy, interfaces, function signatures, and more
- Accurate events/delegates for binding
- GUID-matched structs (no more crashes on complex/weird structs and enums)
- All materials and material instances recreated with accurate parameters
- Placeholder 4×4 pixel textures created
- Default values populated + cross references populated

## What this does **not** include
- Any actual game logic or binary assets (no meshes, sounds, real textures, animations, or internal code/BP logic)
- Accurate skeletons
- Widget images/fonts
- Accurate particles (assets are created but not populated)
- Maps
- Any recreation of C++ game code

## Warning

> [!WARNING]
> If you have an **existing** modding environment you are installing these new ghostmappings into, please read carefully.
> If you are installing fresh, these warnings don't apply.

There are a *large* number of assets included in this repo. Old ghostmappings are archived [here](https://github.com/modestimpala/VotV_ghostmapping/tree/archive).

This is **not** an easy drop-in replacement for old ghostmappings. Every single asset has been re-generated. GUIDs are different. Pin names are different.

### Known migration issues

- Pre-existing maps that contained old ghostrefs may crash the editor on open, or crash UAT when packaging
- Broken "Break struct" nodes across many blueprints
- Broken pin connections across many blueprints

### How to fix

1. Re-create any broken "Break struct" nodes
2. Re-link broken pin connections
3. Safely migrate maps (open with old ghostrefs → delete bad refs → save → migrate) or delete them entirely

After that, things should stay stable since GUIDs/pin names shouldn't change often. If you're still having issues, check packaging logs for specific blueprint error mentions and fix each blueprint individually.

## Installation

**Option A** : Download the ZIP from GitHub.

**Option B** : Clone with Git LFS:
```
git lfs install
git clone https://github.com/modestimpala/VotV_ghostmap.git
```

Then, with Unreal Editor **closed**, drag and drop the `Content` folder into your mod project's base directory (usually named `VotV`). Your project should already have a `Content` folder - the contents will merge, and the new assets will appear in your editor.

## Contributing

If you notice any weirdness, inconsistencies or issues with assets please open an issue on GitHub.

## Credits

- **NynrahGhost** - Hard work creating the original VotV_ghostmapping repo, making ghostmaps by hand.
- **MrDrNose** - Voices of the Void.