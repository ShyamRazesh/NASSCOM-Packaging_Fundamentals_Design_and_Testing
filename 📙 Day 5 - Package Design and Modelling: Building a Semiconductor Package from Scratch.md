
# <h5 id="header-5">📙 Day 5 - Package Design and Modelling: Building a Semiconductor Package from Scratch</h5>

# Creating the Die and Substrate in AEDT:

In this lab exercise, I focused on building the foundational layers of a semiconductor package by creating the die and substrate within ANSYS Electronics Desktop (AEDT).

- I began by launching the Q3D Modeller and setting up a new project. Using the modelling tools, I created two primary solids: the substrate and the die. The substrate serves as the base layer, providing mechanical support and electrical interconnection for the package. The die, representing the active silicon component, was modeled as a separate solid and positioned accurately on top of the substrate.

- To achieve this, I used the "Create Rectangle" and "Thicken Sheet" commands to define the precise dimensions and thickness for both the substrate and the die. The properties panel allowed me to specify a thickness of 0.5 mm for the die, ensuring realistic proportions in the cross-sectional model. I organised the model tree with clear naming conventions, grouping the substrate and die under their respective material categories (e.g., copper for the substrate, silicon for the die).

- Throughout the process, I utilised the 3D visualisation tools to inspect the model from different angles, confirming the correct alignment and stacking of the die on the substrate. This careful construction provides the essential foundation for subsequent steps in package modelling, such as adding die-attach materials, bond pads, and encapsulation layers.

- By completing this exercise, I gained hands-on experience in using AEDT’s geometric modelling features to accurately represent the core structural elements of a semiconductor package, which is critical for further simulation and analysis.
  
  <img width="319" height="191" alt="image" src="https://github.com/user-attachments/assets/28333e3d-2982-49cd-a9d7-70cc4e886df0" />

**Steps to Create a Die in ANSYS**

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
  
<img width="1919" height="856" alt="image" src="https://github.com/user-attachments/assets/99831d83-19a3-437e-9fcd-b8ac60000323" />

<img width="1919" height="835" alt="image" src="https://github.com/user-attachments/assets/e12b4bff-3fe9-4ca2-ac53-4625b70c29ac" />

**Step 4. Create the Substrate Geometry**

- Create another rectangle for the substrate (e.g., 5mm x 5mm)
- Position the substrate such that the die is at the center (e.g., -1, -1, -0.1)
- Modeler -> Surface -> Thicken Sheet and set the thickness as -0.5mm

<img width="1271" height="357" alt="image" src="https://github.com/user-attachments/assets/7be2e6c0-f3d7-42a8-94cd-9ae1a254e329" />

<img width="1919" height="670" alt="image" src="https://github.com/user-attachments/assets/ae672f92-6f43-4896-95d5-d53022cb2b3e" />

<img width="1428" height="878" alt="image" src="https://github.com/user-attachments/assets/334cc012-ee53-47d8-abf9-456cafba0de0" />

<img width="1891" height="671" alt="image" src="https://github.com/user-attachments/assets/11b1760b-efea-431f-9fba-20a860ddfcd8" />

- Changing the name from Rectangle1 to Die
- Changing the property from Copper to Silicon
<img width="1273" height="410" alt="image" src="https://github.com/user-attachments/assets/ea617dd8-346e-46d0-8836-57712ee4c5e0" />

# Adding Die Attach Material and Bond Pads:

In this lab exercise, I enhanced the semiconductor package model by adding the die attach material and bond pads using ANSYS Electronics Desktop (AEDT).

- I began by creating the die attach layer, which is essential for securing the silicon die to the substrate and ensuring efficient thermal and mechanical coupling. Using the modelling tools, I defined a thin rectangular solid to represent the die attach material, carefully positioning it between the die and the substrate. I assigned appropriate material properties (such as modified epoxy) to this layer to accurately reflect its real-world behaviour.

- Next, I focused on creating the bond pads for both the die and the substrate. The bond pads serve as the electrical interface points for wire bonding or flip-chip connections. I used the rectangle creation feature to define the geometry of the bond pads, specifying their size and location on both the die and substrate surfaces. For each bond pad, I assigned a conductive material, typically copper, to simulate its electrical characteristics.

- I utilised the properties dialogue to name and organise each bond pad (e.g., "DieBondPad" and "SubstrateBondPad") and to ensure correct orientation and grouping within the model hierarchy. This careful organisation is important for clarity and for subsequent simulation steps.

- Throughout the process, I made use of 3D visualisation tools to verify the correct placement and alignment of the die attach layer and all bond pads. This attention to detail ensures that the model accurately represents the physical structure of a real semiconductor package.

- By completing this exercise, I gained practical experience in modelling critical interconnect features and intermediate materials, which are fundamental for both electrical and thermal simulations in advanced semiconductor packaging.

**Steps to Create a Die Attach Material**

**Step 5: Create the DAM Geometry**

- Create another rectangle same size as die at origin (0,0,0) to represent die attach epoxy
- Set thickness: -0.1 mm
- Assign appropriate material such as modified_epoxy for thermal conductivity simulation

<img width="1918" height="652" alt="image" src="https://github.com/user-attachments/assets/9e44ccef-197b-4c34-b115-d28601d5d760" />

<img width="1266" height="711" alt="image" src="https://github.com/user-attachments/assets/d1799f25-45ef-4b70-974a-a376baa27679" />

<img width="1263" height="707" alt="image" src="https://github.com/user-attachments/assets/ebd5201f-3e6a-4056-ad05-58e9c9e0f046" />

**Steps to Create Bond Pads**
**Step 6: Define Die Pads**

- Create a thin rectangle to represent the die pad of dimensions 0.2mm x 0.2mm
- Set thickness: 0.005 mm
- Similarly create pads on the substrate

<img width="1266" height="463" alt="image" src="https://github.com/user-attachments/assets/09e5fa27-38b3-488d-abf2-93c3d8d11415" />

**Step 7: Create bond pads on both die and substrate**

- Create the pads across the periphery of the die and substrate as shown in the below figure
- These will serve as connection points
- Assign material (typically metal types like copper, gold or aluminum)

<img width="1265" height="527" alt="image" src="https://github.com/user-attachments/assets/da12139c-f45d-45a8-9edc-fabefef27a94" />

# Wire Bond Creation and Material Assignment:

In this lab exercise, I focused on creating wire bonds and assigning appropriate materials within ANSYS Electronics Desktop (AEDT) to further develop the semiconductor package model.

- I started by defining the bond wire geometry using the bond wire creation tool. This involved selecting the bond pads on the die and the corresponding pads on the substrate, then specifying parameters such as wire diameter, height, and the JEDEC 4-point profile to accurately model the physical shape and routing of each wire bond.

- After generating the wire bonds, I used the material assignment feature to specify the wire material. I selected "gold" from the material library, which is commonly used for wire bonding due to its excellent electrical conductivity and reliability. Assigning the correct material is essential for realistic electrical and thermal simulation.

- I carefully adjusted the wire bond properties and orientation to ensure correct alignment between the die bond pads and the substrate bond pads. This step is crucial for both the mechanical integrity and electrical performance of the package.

- Throughout the process, I used the 3D visualisation tools to inspect the wire bond placement and verify that the model accurately represents real-world semiconductor packaging practices.

- By completing this exercise, I gained hands-on experience in modelling wire bonds and assigning materials, which are critical steps for simulating the electrical connectivity and reliability of advanced semiconductor packages.

**Steps to Create Bond Wires**
**Step 8: Connect pads using wires**

- Draw -> Bondwire
- Connect the die pads to substrate pads using gold wire
  
<img width="1258" height="483" alt="image" src="https://github.com/user-attachments/assets/1782ec70-9ff8-4c4d-9472-326edeb03aeb" />

<img width="1262" height="520" alt="image" src="https://github.com/user-attachments/assets/74f9c3f3-5930-4d43-83a0-6cd7c7c4d3bf" />

<img width="1257" height="462" alt="image" src="https://github.com/user-attachments/assets/35228065-93e0-42c1-9889-55cc8790793f" />

# Applying Mold Compound and Finalizing the Package Model:

In this lab exercise, I completed the semiconductor package model by applying the mold compound and finalizing the entire structure within ANSYS Electronics Desktop (AEDT).

- I began by creating a new solid to represent the mold compound, which encapsulates and protects the die, wire bonds, and bond pads from environmental factors and mechanical stress. Using the modeling tools, I defined the geometry of the mold compound as a rectangular block that fully covers the internal components of the package.

- I assigned an appropriate material property (such as epoxy or a specific mold compound) to this layer to accurately simulate its protective and insulating characteristics. The properties panel allowed me to specify the material and adjust the dimensions as needed for complete coverage.

- Throughout the process, I used the 3D visualisation tools to inspect the model, ensuring that the mold compound encapsulated all critical elements without leaving any gaps. I also reviewed the model tree to confirm that all components were properly organised and named for clarity.

- By completing this exercise, I gained practical experience in the final steps of package modelling, understanding how the mold compound contributes to the mechanical integrity and environmental protection of semiconductor packages. This step is essential for preparing the model for subsequent reliability and thermal simulations.


**Steps to Create Mold Compound**
**Step 9: Build mold around the die**

- Add a rectangular mold compound to encapsulate the die and wire bonds
- Set thickness: 1.2 mm
- Assign mold material (e.g., epoxy molding compound)

<img width="1259" height="504" alt="image" src="https://github.com/user-attachments/assets/278b94db-13e0-41f0-ac4d-35ddbe24c44d" />

<img width="1118" height="527" alt="image" src="https://github.com/user-attachments/assets/a65401bf-f62c-4da9-853c-0c7fd8e762cc" />

<img width="709" height="475" alt="image" src="https://github.com/user-attachments/assets/2519d67f-ccb7-463c-9977-6955938c8f6d" />

<img width="1242" height="505" alt="image" src="https://github.com/user-attachments/assets/0febd5bc-f1db-4ed1-80c0-ee0ab1e42a9f" />




