
# <h5 id="header-5">📙 Day 5 - Package Design and Modelling: Building a Semiconductor Package from Scratch</h5>

**Creating the Die and Substrate in AEDT:**

In this lab exercise, I focused on building the foundational layers of a semiconductor package by creating the die and substrate within ANSYS Electronics Desktop (AEDT).

- I began by launching the Q3D Modeller and setting up a new project. Using the modelling tools, I created two primary solids: the substrate and the die. The substrate serves as the base layer, providing mechanical support and electrical interconnection for the package. The die, representing the active silicon component, was modeled as a separate solid and positioned accurately on top of the substrate.

- To achieve this, I used the "Create Rectangle" and "Thicken Sheet" commands to define the precise dimensions and thickness for both the substrate and the die. The properties panel allowed me to specify a thickness of 0.5 mm for the die, ensuring realistic proportions in the cross-sectional model. I organised the model tree with clear naming conventions, grouping the substrate and die under their respective material categories (e.g., copper for the substrate, silicon for the die).

- Throughout the process, I utilised the 3D visualisation tools to inspect the model from different angles, confirming the correct alignment and stacking of the die on the substrate. This careful construction provides the essential foundation for subsequent steps in package modelling, such as adding die-attach materials, bond pads, and encapsulation layers.

- By completing this exercise, I gained hands-on experience in using AEDT’s geometric modelling features to accurately represent the core structural elements of a semiconductor package, which is critical for further simulation and analysis.

**Creating the Die and Substrate in AEDT**
🛠️ Steps to Create a Die in ANSYS

Step 1. Launch ANSYS Electronics Desktop (AEDT)

- Choose a project type: Icepak, HFSS 3D Layout, or Q3D Extractor
- Create a new project and insert a new design (e.g., Icepak for thermal, HFSS for EM)
- Define the Working Units: Go to Modeller → Units
- Set units to mm (or μm) for package-scale modelling. Step 2. Create the Die Geometry
- Use Draw → Rectangle to create the die (chip)
- Set the dimensions as 3mm x 3mm and the positions (0,0,0) for center
- For thickness, apply 0.2mm (after thinning). Modeler -> Surface -> Thicken Sheet and set the thickness as 0.2mm
- Pro Tip: Name it clearly (e.g., Die) Step 3: Assign Material Properties
- Go to Modeler → Assign Material
- Choose Silicon from the material library (or create a custom material)
- Assign it to the die geometry


**Adding Die Attach Material and Bond Pads:**

In this lab exercise, I enhanced the semiconductor package model by adding the die attach material and bond pads using ANSYS Electronics Desktop (AEDT).

- I began by creating the die attach layer, which is essential for securing the silicon die to the substrate and ensuring efficient thermal and mechanical coupling. Using the modelling tools, I defined a thin rectangular solid to represent the die attach material, carefully positioning it between the die and the substrate. I assigned appropriate material properties (such as modified epoxy) to this layer to accurately reflect its real-world behaviour.

- Next, I focused on creating the bond pads for both the die and the substrate. The bond pads serve as the electrical interface points for wire bonding or flip-chip connections. I used the rectangle creation feature to define the geometry of the bond pads, specifying their size and location on both the die and substrate surfaces. For each bond pad, I assigned a conductive material, typically copper, to simulate its electrical characteristics.

- I utilised the properties dialogue to name and organise each bond pad (e.g., "DieBondPad" and "SubstrateBondPad") and to ensure correct orientation and grouping within the model hierarchy. This careful organisation is important for clarity and for subsequent simulation steps.

- Throughout the process, I made use of 3D visualisation tools to verify the correct placement and alignment of the die attach layer and all bond pads. This attention to detail ensures that the model accurately represents the physical structure of a real semiconductor package.

- By completing this exercise, I gained practical experience in modelling critical interconnect features and intermediate materials, which are fundamental for both electrical and thermal simulations in advanced semiconductor packaging.



**Wire Bond Creation and Material Assignment:**

In this lab exercise, I focused on creating wire bonds and assigning appropriate materials within ANSYS Electronics Desktop (AEDT) to further develop the semiconductor package model.

- I started by defining the bond wire geometry using the bond wire creation tool. This involved selecting the bond pads on the die and the corresponding pads on the substrate, then specifying parameters such as wire diameter, height, and the JEDEC 4-point profile to accurately model the physical shape and routing of each wire bond.

- After generating the wire bonds, I used the material assignment feature to specify the wire material. I selected "gold" from the material library, which is commonly used for wire bonding due to its excellent electrical conductivity and reliability. Assigning the correct material is essential for realistic electrical and thermal simulation.

- I carefully adjusted the wire bond properties and orientation to ensure correct alignment between the die bond pads and the substrate bond pads. This step is crucial for both the mechanical integrity and electrical performance of the package.

- Throughout the process, I used the 3D visualisation tools to inspect the wire bond placement and verify that the model accurately represents real-world semiconductor packaging practices.

- By completing this exercise, I gained hands-on experience in modelling wire bonds and assigning materials, which are critical steps for simulating the electrical connectivity and reliability of advanced semiconductor packages.




**Applying Mold Compound and Finalizing the Package Model:**

In this lab exercise, I completed the semiconductor package model by applying the mold compound and finalizing the entire structure within ANSYS Electronics Desktop (AEDT).

- I began by creating a new solid to represent the mold compound, which encapsulates and protects the die, wire bonds, and bond pads from environmental factors and mechanical stress. Using the modeling tools, I defined the geometry of the mold compound as a rectangular block that fully covers the internal components of the package.

- I assigned an appropriate material property (such as epoxy or a specific mold compound) to this layer to accurately simulate its protective and insulating characteristics. The properties panel allowed me to specify the material and adjust the dimensions as needed for complete coverage.

- Throughout the process, I used the 3D visualisation tools to inspect the model, ensuring that the mold compound encapsulated all critical elements without leaving any gaps. I also reviewed the model tree to confirm that all components were properly organised and named for clarity.

- By completing this exercise, I gained practical experience in the final steps of package modelling, understanding how the mold compound contributes to the mechanical integrity and environmental protection of semiconductor packages. This step is essential for preparing the model for subsequent reliability and thermal simulations.











