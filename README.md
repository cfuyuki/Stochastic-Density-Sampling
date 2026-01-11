# SDS: Stochastic Density Sampling
### Implementing Probabilistic Sampling for Architectural Density Design

![unnamed (5)](https://github.com/user-attachments/assets/3c8ca360-2b3d-4024-b2e9-d1ce6f876c94){width=200 height=100}
## 1. Introduction: Sequence or Existence?
**"Do we shake the order, or do we question the existence?"**

**SDS (Stochastic Density Sampling)** is a methodology that implements the core principles of **Stochastic Sampling**—the mathematical backbone of modern Generative AI—into the realm of architectural density design.

While traditional approaches focus on "adding" points to a grid (Count/Cell), SDS proposes a paradigm shift toward **Field-based logic**: generating a population first, then sampling "Existence" based on spatial potential. This allows for a more fluid and integrated approach to designing density gradients.

## 2. Core Logic: The Existence Filter
SDS translates a continuous potential field into a discrete manifestation through a simple yet powerful comparison:

$$R < P$$

* **$P$ (Probability):** The existence probability defined by the designer (Scalar Field).
* **$R$ (Random):** A value drawn from a uniform distribution $[0, 1]$, representing stochastic fluctuation.

By applying this logic, the design focus shifts from commanding specific point counts to designing the **"Tendency"** of a space. Each point effectively functions as an autonomous agent determining its own state based on the local field value, resulting in a "bleeding" gradient that maintains its quality regardless of scale or resolution.

## 3. Methodology: Deterministic vs. Stochastic
This repository provides a comparison between two distinct culling approaches:

| Method | Logic | Characteristics | Output Quality |
| :--- | :--- | :--- | :--- |
| **Subset Culling** | Deterministic | Sorting by distance; extracts top N points. | Sharp, geometric boundaries. |
| **Stochastic Sampling (SDS)** | Probabilistic | $R < P$ comparison per point. | Smooth, atmospheric "Nijimi" effect. |

Unlike deterministic methods, SDS ensures consistent gradient quality regardless of the population size, as the sampling logic is tied directly to the spatial coordinates $(x, y, z)$ rather than list indices.

## 4. Getting Started
### Prerequisites
* Rhino 7 / 8
* Grasshopper

### Usage
1. Download the `.gh` file from this repository.
2. Assign an **Attractor Curve** to define the field.
3. Utilize the **Graph Mapper** to distort the probability density $f(P)$ and manifest your specific density gradient.

---

## 5. Author
**Chie Fuyuki (千枝 冬木)**
* PhD Candidate, Tsinghua University
* Specializing in Computational Design and Generative AI in Architecture.
* [Medium Article](https://medium.com/your-link) | [Portfolio](https://your-portfolio.com)

---

## License
This project is licensed under the MIT License.
