# Hypersonic Glide Vehicle Interceptor GNC via HJI Differential Games

![C++17](https://img.shields.io/badge/Language-C%2B%2B17-blue)
![Defense Aerospace](https://img.shields.io/badge/Domain-Hypersonic%20GNC%20%26%20Aerospace-red)
![Developer](https://img.shields.io/badge/Developer-Ayoub%20Lahmar-brightgreen)

An advanced 3D guidance engine executing saddle-point optimal control strategies derived from **Hamilton-Jacobi-Isaacs (HJI) Zero-Sum Differential Games** to intercept atmospheric Hypersonic Glide Vehicles (HGVs).

Implemented by **Ayoub Lahmar** ([@Redayoub-lang](https://github.com/Redayoub-lang)).

## 📐 Mathematical Formulation

The minimax value function \(V(\mathbf{x}, t)\) governed by the Hamilton-Jacobi-Isaacs PDE satisfies:

$$
-\frac{\partial V}{\partial t} = \max_{\mathbf{v} \in \mathcal{V}} \min_{\mathbf{u} \in \mathcal{U}} \left[ \nabla V^T f(\mathbf{x}, \mathbf{u}, \mathbf{v}) \right]
$$

Optimal pursuer control \(\mathbf{u}^*\) minimizes the objective value function under maximum maneuvering constraints:

$$
\mathbf{u}^* = -a_{\max} \frac{\nabla_{\mathbf{v}_{\text{rel}}} V}{\|\nabla_{\mathbf{v}_{\text{rel}}} V\|}
$$

## 💻 Build & Compile

```bash
g++ -std=c++17 -O3 main.cpp -o HypersonicGNC
./HypersonicGNC
