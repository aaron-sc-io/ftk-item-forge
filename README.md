# FTK Item Forge

Built copy of the FTK Item Forge, the custom item editor for the For The King Combined Pack.
Open it at https://aaron-sc-io.github.io/ftk-item-forge/.

## Adding your item set to the game

You need the **For The King Combined Pack** installed through Gale (or another BepInEx setup). The pack
includes the CustomItemSets plugin that loads your sets.

1. **Build your set.** Open the [Item Forge](https://aaron-sc-io.github.io/ftk-item-forge/) and design your items.
   Drafts are saved in your browser, so you can come back later.
2. **Fix any red errors.** The download button stays disabled until every red validation error is resolved.
   Yellow warnings are fine.
3. **Download the set.** Click **Download .ftkset.json**. You get a file named `<set id>.ftkset.json`.
   Don't rename it.
4. **Launch the game once with the pack.** On first launch the plugin creates the folder
   `BepInEx\config\CustomItemSets\` inside your Gale profile. Close the game afterwards.
5. **Open your profile folder.** In Gale, select your For The King profile and open its folder
   (the profile folder option in Gale's menu), then go to `BepInEx\config\CustomItemSets\`.
6. **Copy the file in.** Put your `.ftkset.json` file in that folder. A set with the same id as one that
   ships with the pack replaces the bundled one.
7. **Start the game.** The set loads at startup. To confirm, check the BepInEx log for
   `Registered N custom item(s)` with no `failed to register` lines.
8. **Turn sets on or off (optional).** Every installed set gets an on/off entry under `[Sets]` in
   `BepInEx\config\CustomItemSets.cfg`, also shown in the in-game mod options. All sets start on.
   Only the host's choice counts in multiplayer.

### Playing online

- **Every player needs the exact same set files.** Item numbers depend on which sets are installed, so
  mismatched files cause desyncs. If yours differ from the host's, a warning banner appears for 20 seconds.
- **Don't add or remove sets mid-campaign.** It can renumber items in existing saves.

### Editing a set later

Use **Import** in the editor's sidebar to load a `.ftkset.json` file, make changes, download it again, and
replace the old file in `CustomItemSets\` (every player in your party needs the new copy too).

---

These files are generated. Edit the source and run `webapp/deploy-pages.ps1` instead.
