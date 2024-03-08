# NEBOViewer

This tool allows to view .ebo files and provides export/import ability.

## Usage

NEBOViewer is handy for editing .ebo files. Currently, it is possible to edit;

- Court models

- Arena models

- Frontend models

You can find basic information about the tool [here](https://wasserlasser.com/filebase/index.php?file/2003-neboviewer/#overview).

The tool allows to load .fsh files and view the model with textures. This is useful for courts and stadia. However, you can import only one part at a time. The tool allows export in .obj and .ply. I advise to export to .ply as vertex color data is also stored.

Then in Blender, edit the model. Make sure that the total number of vertexes, normals, texcolors, etc. must be respected and not exceeded when saving. For exporting, again select .PLY format.

The .ply format has two file formats, a binary format and a text format. NEBOViewer only uses only the text format. Therefore, in Blender when you export in .PLY format, make sure you check the 'ASCII' box.

Why export in .PLY format? Only because some geometries use vertex colors and the Wavefront .obj format doesn't support vertex colors. So you have to use the ASCII format of the stanford .PLY format.

## Known issues

It is not possible to edit face models, or expand the face number in models yet.

## FAQ

It will be filled as users come up with questions.