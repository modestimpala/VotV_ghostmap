# Voices of the Void editor recreation for ghostreferencing 

Currently targets game version: `a09j_0001`

This is an automatically generated, 1:1 accurate recreation of Voices of the Void assets for version a09j_0001.

## What this includes
    - Every single asset accurately recreated down to component/widget hierarchy, interfaces, function signatures, and more
    - Accurate events/delegates for binding
    - GUID-matched structs (no more crashes on complex/weird structs and enums)
    - All materials and material instances recreated with accurate parameters
    - Placeholder 4×4 pixel textures created
    - Default values populated + cross references populated

## What this does NOT include
    - Any sort of actual game logic or binary assets (NO meshes, sounds, real textures, or animations - NO internal code or BP logic recreation)
    - Accurate skeletons
    - Widget images/fonts
    - Accurate particles (asset is created, but not populated with any info)
    - Maps
    - Any recreation of C++ game code

## Warning

**If you have an existing modding environment you are installing these new ghostmappings into, please read. If you are installing fresh, these warnings don't apply.**

**There are also a *large* amount of assets included in this repo now.**

Old ghostmappings are archived [here](https://github.com/modestimpala/VotV_ghostmapping/tree/archive).

This is **NOT** an easy drop-in replacement for old ghostmappings. Every single asset has been re-generated. GUIDs are different. Pin names are different.

Known issues when migrating to these ghostrefs:

    - Pre-existing maps that contained old ghostrefs crashed the editor when opened, or crashed UAT when attempting to package
    - Broken "Break struct" nodes across many blueprints
    - Broken pin connections across many blueprints

You will have to re-create "Break struct" nodes, re-link broken existing pin connections, and safely migrate any maps (open with old ghostrefs, delete bad refs, save map, migrate) or delete maps entirely. After that, things should stay stable since GUIDs/Pin names shouldn't change often.

If you're still having issues, check packaging logs for specific blueprint error mentions and fix each blueprint.

## To use

Make sure Unreal Editor is closed. Drag and drop the Content folder into your mod project base directory (usually named VotV). Your project should already have a Content folder; the contents will merge, and the new assets will appear in your editor.

## Contributing

If you notice any weirdness, inconsistencies or issues with assets please open an issue on GitHub.

## Credits

NynrahGhost for his hard work creating the original VotV_ghostmapping repo, making ghostmaps by hand.

MrDrNose for VotV.