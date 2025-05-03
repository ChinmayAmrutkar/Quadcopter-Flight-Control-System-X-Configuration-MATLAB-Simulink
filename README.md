# Quadcopter Flight Control System (X-Configuration) – MATLAB Simulink

This project implements a **complete Flight Control System (FCS)** for a quadrotor in **X-configuration**, built from scratch using **MATLAB Simulink**. It features a modular, layered control structure and simulates 6-DOF quadrotor dynamics using the **Aerospace Blockset's 6DOF (Euler Angles)** model.
![image](https://github.com/user-attachments/assets/76d7f9a9-c1f6-4b19-b931-65166b15a96e)

---

## 🚀 Project Highlights

- **Trajectory Generator**  
  Designed for **Figure 8 trajectory path tracking** using minimum jerk polynomial trajectories and discrete waypoints.
![Quiz_3_function](https://github.com/user-attachments/assets/80a734a5-9fd8-4c0b-8c5d-6f8626e162fb)

![image](https://github.com/user-attachments/assets/ab8a8367-6b78-40d4-b83f-68bf08a90f1f)


- **Position Controller (Outer Loop)**  
  Converts position error into desired angles (pitch/roll) and altitude control signals using PID controllers.
![image](https://github.com/user-attachments/assets/06df2d3e-57a2-4899-b316-124fa68146bf)

- **Attitude Controller (Inner Loop)**  
  Nested PID controllers stabilize roll, pitch, and yaw angles using feedback from simulated state outputs.
![image](https://github.com/user-attachments/assets/da1fa46a-29aa-41ec-8360-76b10cc0215b)

- **Motor Mixing & Allocation**  
  Implements **inverse motor mixing** to compute individual rotor thrusts from control inputs.
![image](https://github.com/user-attachments/assets/35e0e73d-cc10-43a7-bf20-63aef0cbaea9)

- **Feedforward Control**  
  Additional forward compensation to improve transient response and steady-state accuracy.
![image](https://github.com/user-attachments/assets/8636af59-e58d-4bfb-9ba8-b44cccc2166a)


- **6DOF Dynamics Simulation**  
  Utilizes MATLAB's built-in **6DOF (Euler Angles)** block to simulate realistic translational and rotational dynamics under control inputs.
![image](https://github.com/user-attachments/assets/8d1dc27d-6dd8-4b49-a4f1-ca1b232feba7)


- **3D Visualization**  
  Integrated 3D animation using Simulink's **3D Animation Toolbox** to visualize drone motion and evaluate trajectory tracking.
![image](https://github.com/user-attachments/assets/526470ce-592e-4c8f-9279-4f03fee1a93c)

---

## 📷 System Diagram

The complete flight control architecture is shown below, including:
- Trajectory generation
- Hierarchical control loops
- Motor mixing and thrust computation
- 6DOF quadrotor simulation with visualization

> 📌 *Note: Diagram built using MATLAB Simulink Aerospace Toolbox.*

![image](https://github.com/user-attachments/assets/5490d50b-7e8f-4080-afe0-5243c1b6c106)


---

## 🔧 Tools & Technologies

- **MATLAB Simulink (R2023a)**
- Aerospace Blockset
- Control System Toolbox
- Signal Processing Toolbox
- Simulink 3D Animation

---

### 📈 Results

#### ✅ Trajectory Tracking Performance

The figure below shows the actual vs desired positions in the X, Y, and Z directions during a circular trajectory tracking task. The Flight Control System successfully follows the path with minimal steady-state error and smooth transitions.

![Quiz_3_results](https://github.com/user-attachments/assets/e6238a1c-425e-4826-9acf-da53594294c2)

- **Yellow, Blue, Purple**: Actual X, Y, Z positions  
- **Green, Cyan, Orange**: Desired X, Y, Z references

The Flight Control System was simulated in 3D using Simulink’s animation environment. Below is a visual glimpse of the quadcopter following the trajectory in 3D space:

![Drone_8_Figure](https://github.com/user-attachments/assets/8c3d6f45-625c-4b18-817e-c15079cbe8af)


---

## 🎯 Outcomes

- Achieved **stable hover**, **circular 8 trajectory tracking**, and **attitude stabilization**.
- Modular design can be extended to **hardware-in-the-loop (HIL)** testing or PX4 integration.
- Demonstrated resilience to initial perturbations and minor disturbances in simulation.

---

## 🧠 Future Work

- Integrate with PX4 or ROS2 for real-world deployment
- Add wind disturbance and IMU noise models
- Extend to support **autonomous landing** and **obstacle avoidance**

---

## 📫 Contact

For questions, collaboration, or feedback, reach out to [Chinmay Amrutkar](mailto:chinmayamrutkar01@gmail.com) or connect on [LinkedIn](https://www.linkedin.com/in/chinmay-amrutkar-153375209).

