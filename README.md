This is a repository for the polyhedron explorer in [icosahedron](https://github.com/hexahedron1/icosahedron/)  
Current checklist:  
- [x] Platonic solids
    - [ ] Platonic-archimedian connections
    - [ ] Platonic-catalan connections
    - [ ] Platonic-johnson connections
    - [ ] Platonic-star polyhedron connections
- [ ] Archimedian solids
    - [ ] Archimedian-catalan connections
    - [ ] Archimedian-johnson connections
    - [ ] Archimedian-star polyhedron connections
- [ ] Catalan solids
- [ ] Johnson solids
- [ ] Kepler-Poinsot polyhedra
- [ ] Uniform star polyhedra
- [ ] Polygons?
- [ ] Tilings?
# Groups
Each group consists of a folder with a `.group.json` file that describes it and other json files for each polyhedron  
The basic structure for the group file is:
```json
{
    "name": "Name of the group",
    "description": "Description of the group",
    "thumbnail": "Link to the thumbnail that will be shown in the embed",
    "sections": {
        "Name": "Value",
        "This can": "have anything as the keys and values will be dynamically converted to embed fields in discord"
    },
    "trivia": [
        "A random string gets chosen from here each time an embed is generated and put in the footer"
    ]
}
```
# Polyhedron files
Each polyhedron must be defined in a group folder in a json file  
The file structure is:
```json
{
    "name": "Name of the polyhedron",
    "description": "Description of the polyhedron",
    "sections": {
        "Same as .group.json": "but the most common sections are these (an icosahedron as an example):",
        "Edges": "30",
        "Vertices": "12",
        "Schläfli symbol": "{3, 5}",
        "Properties": "Convex\nComposite\nIsogonal\nIsohedral\nIsotoxal\nDeltahedron",
        "Dual": "Regular dodecahedron",
        "Faces": "20 Equilateral triangle",
        "Dihedral angle": "~138.190°",
        "Symmetry group": "Icosahedral"
    },
    "image": "Image of the polyhedron",
    "vfig": null,
    "trivia": [
        "Same as .group.json"
    ],
    "link": "Link to more info (usually the polyhedron's wikipedia page)",
    "otherNames": [
        "Other names the polyhedron is know as",
        "These will be used for autocomplete and search as well as the name key"
    ],
    "operations": {
        "Operations that can be applied to the polyhedron": "They are presented in a dropdown below the embed. Works similar to the sections key, but the value must be the resulting polyhedron's name (NOT path, the name value)"
    }
}
```