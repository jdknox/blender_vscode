# Changelog

## Unreleased

## [0.0.17] - 2022-06-08

### Added
- New `blender.addonFolders` option. Allows to specify absolute or root workspace relative 
directories where to search for addons. If not specified all workspace folders are searched.

### Fixed
- Update `get-pip.py`.
- Use `ensurepip` if available.

## [0.0.16] - 2021-06-15

### Fixed
- Fix after api breakage.

## [0.0.15] - 2021-05-10

### Fixed
- Use `debugpy` instead of deprecated `ptvsd`.

## [0.0.14] - 2021-02-27

### Fixed
- Update `auto_load.py` again.

## [0.0.13] - 2021-02-21

### Fixed
- Update `auto_load.py` to its latest version to support Blender 2.93.

## [0.0.12] - 2019-04-24

### Added
- New `blender.addon.moduleName` setting. It controls the name if the generated symlink into the addon directory. By default, the original addon folder name is used.

### Fixed
- Fix detection for possibly bad addon folder names.
- Addon templates did not contain `version` field in `bl_info`.

## [0.0.11] - 2019-03-06

### Added
- New `Blender: Open Scripts Folder` command.
- New `CTX` variable that is passed into scripts to make overwriting the context easier. It can be used when calling operators (e.g. `bpy.ops.object.join(CTX)`). This will hopefully be replaced as soon as I find a more automatic reliable solution.

### Fixed
- Scripts were debugged in new readonly documents on some platforms.
- Addon package was put in `sys.path` in subprocesses for installation.
- Warn user when new addon folder name is not a valid Python module name.
- Path to Blender executable can contain spaces.

## [0.0.10] - 2018-12-02

### Added
- Support for multiple addon templates.
- Addon template with automatic class registration.
- Initial `Blender: New Operator` command.

### Fixed
- Handle path to `.app` file on MacOS correctly ([#5](https://github.com/JacquesLucke/blender_vscode/issues/5)).
- Better error handling when there is no internet connection.
