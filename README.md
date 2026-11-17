# Artificial Intelligence Power Line Maintenance System

This repository contains project documentation and robotics simulation assets for a power-line maintenance system concept. Its executable example is a miniature-robot navigation workflow in V-REP/CoppeliaSim; the repository does not include a trained power-line inspection model or a deployable inspection pipeline.

## Repository contents

- `Robotics_Artificial Intelligence Power Line MaintenanceSystem.pdf` and `annotated-R3%20Robotics_Artificial%20Intelligence%20Power%20Line%20Maintenance%20System.docx.pdf` — project report documents.
- `PF_VFH+ Runtime_Execution.xlsx` — runtime execution data.
- `Scene Files/` — CoppeliaSim/V-REP scenes, including project scenes and path-planning examples.
- `Path tracking/path_tracking_vrep-master/` — an example Jupyter notebook, simulation scene, map image, and legacy V-REP remote API files. The notebook processes a top-view image, finds a route with A*, smooths the route, and uses a differential-drive/PID controller to guide the simulated robot.
- `Path tracking/Backup/` and `Project/` — archived or duplicate project assets.

## Running the path-tracking example

The notebook uses the legacy V-REP remote API and expects a compatible simulator scene and API server. It connects to `127.0.0.1:19999` and refers to scene objects by name, so use the supplied scene and check that its object names and remote API configuration match the notebook.

1. Install a compatible V-REP/CoppeliaSim version with the legacy remote API enabled.
2. Install Python, Jupyter Notebook, NumPy, OpenCV, and Matplotlib.
3. Open `Path tracking/path_tracking_vrep-master/Astar.ttt` in the simulator and start the remote API server on port `19999`.
4. Start Jupyter in `Path tracking/path_tracking_vrep-master/`, open `path_tracking.ipynb`, and run the cells in order.

The notebook controls a simulator, not physical equipment. The archived remote API libraries and binaries may require adjustments for your operating system, Python version, or simulator release.

## Notes

Scene files use the `.ttt` format. PDF and spreadsheet files are project artifacts and are not required to run the path-tracking notebook.
