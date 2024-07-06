---
layout: default
title: Complex Numbers
parent: Fundamentals
nav_order: 2
---

# Complex Numbers

$$z=\mathcal{Re}\{z\}+j\mathcal{Im}\{z\}$$

---

#### Euler's Formula

$$\mathrm{e}^{j\theta}=\cos\theta+j\sin\theta$$

---

#### Modulus / Magnitudes

$$r=|z|=\sqrt{|\mathcal{Re}\{z\}|^2+|\mathcal{Im}\{z\}|^2}$$

##### Properties

$$|r\mathrm{e}^{j\theta}|=|r||\cos\theta+j\sin\theta|=\sqrt{|r|^2}\sqrt{|\cos\theta|^2+|\sin\theta|^2}=r$$

$$|\mathrm{e}^{j\theta}|=|\cos\theta+j\sin\theta|=\sqrt{|\cos\theta|^2+|\sin\theta|^2}=1$$

---

#### Argument / Phase

$$\theta=\arg (r\mathrm{e}^{j\theta})$$

##### Properties

$$\arg (ab)=\arg a+\arg b$$

$$z_1z_2=r_1\mathrm{e}^{j\theta_1}r_2\mathrm{e}^{j\theta_2}=r_1r_2r\mathrm{e}^{j(\theta_1+\theta_2)}$$

$$z_1+z_2=r_1\mathrm{e}^{j\theta_1}+r_2\mathrm{e}^{j\theta_2}$$

---

#### Complex conjugate

$$z^*=\mathcal{Re}\{z\}-j\mathcal{Im}\{z\}$$

##### Properties

$$(\mathrm{e}^{j\theta})^*=\mathrm{e}^{-j\theta}$$

$$\mathcal{Re}\{z\}=\frac{z+z^*}{2} \ \ \ \mathcal{Im}\{z\}=\frac{z-z^*}{2j}$$

$$\cos\theta=\frac{\mathrm{e}^{j\theta}+\mathrm{e}^{-j\theta}}{2} \ \ \ \sin\theta=\frac{\mathrm{e}^{j\theta}-\mathrm{e}^{-j\theta}}{2j}$$