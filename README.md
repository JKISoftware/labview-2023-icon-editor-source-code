# LabVIEW 2023 Q1 Icon Editor Source Code

![LabVIEW Version](https://img.shields.io/badge/LabVIEW-2023%20Q1-%23FFC50C.svg?})

This project contains the source code for NI LabVIEW 2023 Q1 Icon Editor, along with some improvements.

## Source Contents:

Key Folders:

- `src\resource\plugins` - This folder contains the Icon Editor GUI and its support VIs.
- `vi.lib\LabVIEW Icon API` - This folder contains a library of VIs for working with LabVIEW VI icons, which are available for use in your LabVIEW applications. They are called by the Icon Editor GUI.

Key Files:

- `resource\plugins\lv_icon.lvproj` this is a LabVIEW Project file with a build spec for building the PPL (which is the form of the Icon Editor that ships with LabVIEW).

## Running the Icon Editor from Source Code

We can configure LabVIEW use this source code version of the Icon Editor(instead of the built PPL (`.lvibp` file) version that ships with LabVIEW). Running from source is nice because we can quickly/easily edit and debug the code while using it in the LabVIEW editor.

## Installing the Source Code into LabVIEW manually

### 1. Backup LabVIEW's Installed Files

Backup the following file(s) and folder(s):

    - `<LabVIEW2023>\resource\plugins\lv_icon.lvlibp`
    > Note: `lv_icon.lvlibp` is the built Icon Editor LabVIEW plugin. By moving it out of the pluygins folder (or renaming it with a different extension like `.lvlibp_`), LabVIEW will not load it (which will allow us to use the source code version of the Icon Editor).
    - `<LabVIEW2023>\vi.lib\LabVIEW Icon API`
    > One way you can backup these files/folders is to create a zip of them, and then delete the unzipped files.

After you've backed up these items, you can proceed to installing the source code.

### 2. Copy Source Files into LabVIEW

Copy the contents of this repo's `src` folder into the `<LabVIEW2023>` installation folder.

Note: When running from source (after "installing" the source as described below), LabVIEW loads this Icon Editor LabVIEW plugin VI, here:

- `resource\plugins\lv_icon.vi`