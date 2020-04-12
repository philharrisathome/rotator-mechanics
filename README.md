# rotator-mechanics

This is my branch of https://gitlab.com/librespacefoundation/satnogs/satnogs-rotator/-/tree/v3.1-pre-release, heavily modified for different drive motor strategy.

Full credit goes to the team at SatNOGS - if I can get this build working I'll look at merging it in.

---

# SatNOGS Rotator

Hardware for SatNOGS Rotator. This repository includes all needed source files for 3D printed (and other) parts of SatNOGS Rotator.

## Documentation

More information can be found in our [wiki](https://wiki.satnogs.org/SatNOGS_Rotator_v3).

## Repository policy - Naming Convention

According to F3 - [Form, Fit and function](https://en.wikipedia.org/wiki/Form,_fit_and_function) and
[Part number, wiki page](https://en.wikipedia.org/wiki/Part_number) some rules build about the naming
convention and versioning:
* C, custom parts, placed in rotator_parts file
* H, hardware parts, placed in shared file
* A, assemblies, placed in assemblies file
* All used part numbers are placed in part-number-list spreadsheet.
* Start the number from 1000, e.g. C1000-1.
* Dash -1 (odd), are parts from same family for example M5 screws with same DIN and different lengths.
* Dash -2 (even), are parts from same family but all features are mirrored.
* Small changes in the part (fit - aspect), not affect the part number but affected the variant (-n).
* Big changes in the part or assembly (form and function aspect), affect the part number, make a new one
and replace or remove the old one.
* When a part is ready, in the commit message only this part and the message contains the revision of the part and a
release note about the changes. If needed update the drawing inside the freecad.
Then commit all sub-assemblies and the main assembly which affected by the part or parts.
* In order to add a new part take a new part number according to the part number list (spreadsheet).
* When a part or assembly isn't ready for release, in commit message add WIP, work in progress, write the
changes must be done, refers to the issue.
* When all parts and assemblies are ready and working properly, a release is done with tagging the last commit
and a file with all fabrication files like *.stl, *.step, *.pdf (for drawings), *.dxf (for 2D parts) are generated
which each file is naming with pn_revN.*
* Master branch is most times under active development, so expect things to break.
* Assembly is broken down to specific groups, sub-assemlies. The first priority of assembly levels is to help the designer in
design process and not in the real assembly. The second priority is to make assemblies that helps in assembly process.
We never work on very large assemblies, due to limitation in CAD program.
* Try to use a coordinate system that is fit in the main assembly.
* Drawing revision does not exist, only part or assembly revision is modified. When a small change is done in drawing for example in text the revision isn't change because the part or assembly isn't change.

## Contribute

The main repository lives on [Gitlab](https://gitlab.com/librespacefoundation/satnogs/satnogs-rotator) and all Merge Request should happen there.

## License

[![Libre Space Foundation](https://img.shields.io/badge/%C2%A9%202014--2018-Libre%20Space%20Foundation-6672D8.svg)](https://librespacefoundation.org/)
Licensed under the [CERN OHLv1.2](LICENSE).
