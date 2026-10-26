# comma_chestnut_mount_and_protector

## STEP models

| File | Description |
| --- | --- |
| `meshfinal.stp` | Original reference enclosure. |
| `meshfinal_33cm_trim.stp` | Earlier 330 mm internal-length enclosure with restored opening trim. |
| `meshfinal_40cm_bump_moved.stp` | Earlier 400 mm internal-length enclosure. |
| `tank_and_meshnut.stp` | Source containing the honeycomb and open-frame assemblies. |
| `honeycomb_original.stp` | Honeycomb assembly separated from the source, without dimensional changes. |
| `open_frame_original.stp` | Open-frame assembly separated from the source, without dimensional changes. |
| `honeycomb_33cm.stp` | Honeycomb enclosure extended to 330 mm internal length; added cells retain the original size. |
| `open_frame_33cm.stp` | Open-frame enclosure extended to 330 mm internal length, including its opening edges. |

The two new 330 mm variants retain their respective source designs rather than
substituting the earlier `meshfinal` geometry. Their motherboard parts, internal
brackets, and associated mounting locations are unchanged. Rear end-frame screws
and their matching cover holes move together to the new rear end. The honeycomb
variant is extended by approximately 106 mm, and the open-frame variant by
approximately 101 mm, because their original cavity lengths differ.

Both exports are re-imported and checked for valid solids, preserved parts,
mounting-hole locations, and a collision-free 330 x 126 x 50 mm rectangular card
envelope. The open-frame assembly retains the small, detached reference disk
present in the source; it is not an added enclosure feature.

These checks verify geometric space only, not PCIe connector alignment, cable
routing, cooling, or manufacturing tolerances. A 330 mm card uses the nominal
length without assembly clearance. The previously discussed 304 x 126 x 50 mm
ASUS card has 26 mm of nominal length allowance.

## Refined STEP variants

The following separately saved files merge redundant same-surface boundaries
introduced by extension. They do not fuse removable covers, brackets, or other
independent parts together:

- `honeycomb_33cm_merged.stp`
- `open_frame_33cm_merged.stp`
- `meshfinal_33cm_trim_merged.stp`
- `meshfinal_40cm_bump_moved_merged.stp`

The source versions remain unchanged. Each refined export is re-imported and
checked for valid solids, unchanged part counts and bounding dimensions, and
volume agreement. Geometric healing uses at most 0.001 mm tolerance. Genuine
part interfaces and edges between different surfaces remain visible.