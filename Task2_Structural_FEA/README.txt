TASK 2 — Structural Simulation package

Contents
- structural_fea_report.html: report with model definition, load cases, results, observations and figures. Open in a browser.
- fea_beam.js: runnable Node.js generator and 20-element beam FE calculation. From the task folder run: node outputs/fea_beam.js
- fea_results.csv: calculated numeric results.
- beam_geometry_loads.svg, deflection_chart.svg, stress_chart.svg: figures used by the report.
- cantilever_beam.CATScript: CATIA V5 macro to create the editable 300 x 30 x 6 mm beam solid and save CATPart.

CATIA V5 steps
1. Open CATIA V5. Tools > Macro > Macros > select cantilever_beam.CATScript > Run.
2. The macro creates the beam solid with its length along +Z and saves cantilever_beam.CATPart in this outputs folder.
3. If Generative Structural Analysis is licensed, create a 3D solid static analysis, assign steel (E=210 GPa, yield=250 MPa), clamp the z=0 end face, and create separate cases for 100 N and 200 N downward tip forces and 100 N/m downward full-span distributed load. Mesh and solve each case.
4. Capture CATIA screenshots of the model, boundary conditions, mesh, displacement and Von Mises stress result for each case. The included report's numerical results are an independent linear Euler-Bernoulli beam FE model, not CATIA solver output.

Key results (FE model):
Case A: 100 N tip — 7.9365 mm tip deflection; 166.6667 MPa bending stress; FoS 1.50.
Case B: 200 N tip — 15.8730 mm; 333.3333 MPa; FoS 0.75 (yield exceeded under assumed strength).
Case C: 100 N/m UDL — 0.8929 mm; 25.0000 MPa; FoS 10.00.

Units: N, mm, MPa. Linear-elastic static study; no shear deformation, stress concentrations, fatigue, buckling or self-weight. The report makes no claim that native CATIA analysis screenshots or solver results were generated.
