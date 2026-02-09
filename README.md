# X-Arm Robot Models and Configuration Repository

This repository provides **technical assets of the X-Arm robot** for simulation and motion planning

## Repository Overview

- **Single-arm / Dual-arm URDF models**
- **Single-arm / Dual-arm USDZ models** 
- **CuRobo motion planning configurations**



## Repository Structure

```text
xarm/
├── preview_image/   
│
├── xarm_curobo_config/           
│   ├── dual_arm/     
│   └── single_arm/
│       ├── collision_xarm.yml          
│       └── xarm.yml  
│
├── xarm_urdf/     
│   ├── dual_arm/
│   │   ├── xarm.srdf          
│   │   └── xarm.urdf                  
│   ├── meshes/                   
│   └── single_arm/
│       ├── xarm.srdf          
│       └── xarm.urdf          
│
├── xarm_single-arm.usdz                     
├── xarm_dual-arm.usdz            
│
├── LICENSE
└── README.md

```



## 1. URDF Models

 Path: `xarm_urdf/`
 URDF models describe the **topology and kinematics** of the robot and are used for:

* URDF → USD conversion

- Collision modeling and joint validation

 Typical URDF contents:

- Link and joint definitions
- Joint limits
- Visual and collision meshes



## 2. USDZ Models

-  `xarm_single-arm.usdz`: single-arm model
-  `xarm_dual-arm.usdz`: dual-arm model

 USDZ models are directly usable in **NVIDIA Isaac Sim** and typically include:

- Full articulation hierarchy
- Physical properties (mass, inertia)
- Collision shapes
- Materials and textures

 Typical use cases:

- Robot simulation


### Model Preview

The image below displays the 3D asset previews for both the single-arm model and the dual-arm model

<table style="width:100%;">
<tr>
<td style="width:50%; padding:8px;">
<div style="width:100%; height:320px; display:flex; align-items:center; justify-content:center;">
<img src="./preview_image/singal_arm.png" alt="Preview left" style="width:100%; height:100%; display:block; object-fit:contain;"/>
</div>
</td>
<td style="width:50%; padding:8px;">
<div style="width:100%; height:320px; display:flex; align-items:center; justify-content:center;">
<img src="./preview_image/dual_arm.png" alt="Preview right" style="width:100%; height:100%; display:block; object-fit:contain;"/>
</div>
</td>
</tr>
</table>



## 3. CuRobo Configuration

 Path: `xarm_curobo_config/`

 This directory contains **CuRobo** configurations defining the robot model for motion planning.

 Typically includes:

- Kinematic / dynamic parameters
- Joint constraints
- Collision spheres or simplified geometry
- Planner and optimizer parameters

 Supported scenarios:

- Single-arm or Dual-arm planning
- Batch trajectory generation and testing



## Version (Suggested)

- Isaac Sim: `>= 5.x`

>  Please update according to the validated environment
