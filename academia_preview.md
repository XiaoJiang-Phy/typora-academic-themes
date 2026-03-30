# Theme Preview

## 1. Typography

This is English body text, set in the primary font designed for long-form reading with excellent legibility. This is Chinese body text, designed to provide both an academic feel and modern aesthetics.

Body text supports *italic*, **bold**, ***bold italic***, and `inline code` formatting natively. The typography is optimized for both screen viewing and PDF exports.

## 2. Mathematics

### Inline Math

The Schrödinger equation $i\hbar \frac{\partial}{\partial t} |\Psi\rangle = \hat{H} |\Psi\rangle$ governs the time evolution of quantum states. 

### Display Math

The Berry curvature in momentum space is given by:

$$
\Omega_{n}(\mathbf{k}) = -2 \sum_{m \neq n} \frac{\mathrm{Im} \langle n\mathbf{k} | \nabla_{\mathbf{k}} H | m\mathbf{k} \rangle \times \langle m\mathbf{k} | \nabla_{\mathbf{k}} H | n\mathbf{k} \rangle}{(E_m - E_n)^2}
$$

The anomalous Hall conductivity is defined as:

$$
\sigma_{xy} = -\frac{e^2}{\hbar} \sum_n \int_{\mathrm{BZ}} \frac{d^2 k}{(2\pi)^2} \, f_n(\mathbf{k}) \, \Omega_n(\mathbf{k})
$$

## 3. Code Blocks

### Python

```python
import numpy as np
from scipy.linalg import eigh

def berry_curvature(H_func, kx, ky, dk=1e-5):
    """Compute Berry curvature at (kx, ky) for the lowest band."""
    # Finite-difference derivatives compute partial variations
    psi_x = eigh(H_func(kx + dk, ky))[1][:, 0]
    psi_y = eigh(H_func(kx, ky + dk))[1][:, 0]
    psi_0 = eigh(H_func(kx, ky))[1][:, 0]

    # U(1) link variables representation
    Ux = np.dot(psi_0.conj(), psi_x)
    Uy = np.dot(psi_0.conj(), psi_y)

    return -2.0 * np.imag(np.log(Ux * Uy / (np.abs(Ux) * np.abs(Uy))))
```

### C++

```cpp
#include <Eigen/Dense>
using Eigen::Matrix2cd;

Matrix2cd haldane_hamiltonian(double kx, double ky, double t1, double t2, double phi) {
    Matrix2cd H = Matrix2cd::Zero();
    // Nearest-neighbor hopping construction
    std::complex<double> f_k = t1 * (1.0 + std::exp({0, kx}) + std::exp({0, ky}));
    H(0, 1) = f_k;
    H(1, 0) = std::conj(f_k);
    return H;
}
```

## 4. Blockquotes

> "The career of a young theoretical physicist consists of treating the harmonic oscillator in ever-increasing levels of abstraction."
>
> — Sidney Coleman

## 5. Tables

| Model       | Gap (eV) | Chern Number | $\sigma_{xy}$ ($e^2/h$) |
| ----------- | -------: | -----------: | -----------------------: |
| Haldane     |     0.52 |            1 |                     1.00 |
| Kane-Mele   |     0.03 |            0 |                     0.00 |
| BHZ         |     0.01 |           -1 |                    -1.00 |
| Altermagnet |     0.00 |            0 |                     0.15 |

## 6. Task Lists & Checklists

### Unordered Lists

- Tight-binding Hamiltonian
- Bloch theorem and band structure
- Berry phase and geometric quantities
  - Berry connection $\mathcal{A}_n(\mathbf{k})$
  - Berry curvature $\Omega_n(\mathbf{k})$
  - Chern number $C_n$

### Ordered Lists

1. Define the lattice model geometry.
2. Construct the Bloch Hamiltonian $H(\mathbf{k})$.
3. Diagonalize the system to obtain the eigenstates.
4. Integrate invariant properties over the Brillouin Zone.

### Task List

- [x] Create Academia Light theme
- [x] Create Clarity elevated card theme
- [ ] Add Dark Mode variations
- [ ] Setup repository automation

## 7. Footnotes

The integer quantum Hall effect[^1] was experimentally discovered in 1980, leading to a Nobel Prize for von Klitzing shortly after.

[^1]: K. von Klitzing, G. Dorda, and M. Pepper, *Phys. Rev. Lett.* **45**, 494 (1980).

---

*End of preview document*
