## P6

### Fundamentals: ions in a electric field (3/5)

#### 泊松方程（Poisson equation）
- 泊松方程的表达式是：
     \[
     \Delta \phi_{EI} = -\frac{\rho_{EI}}{\epsilon_0 \epsilon_r}
     \]
- 其中，\(\Delta \phi_{EI}\) 是电势的拉普拉斯算子，\(\rho_{EI}\) 是电荷密度，\(\epsilon_0\) 是真空中的电容率，\(\epsilon_r\) 是相对电容率。
- 泊松方程是数学和物理学中非常重要的一个偏微分方程，它描述了标量场（如电势、重力势）在空间中的分布情况。在电磁学中，泊松方程用于描述电势在空间的分布，其一般形式为：

    \[
    \Delta \phi = -\frac{\rho}{\epsilon}
    \]

    其中，\(\Delta\) 是拉普拉斯算子，表示为：

    \[
    \Delta = \nabla \cdot \nabla = \frac{\partial^2}{\partial x^2} + \frac  {\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2}
    \]

    \(\phi\) 是标量场（在电磁学中是电势），\(\rho\) 是电荷密度，\(\epsilon\) 是电   容率（在真空中为 \(\epsilon_0\)，在介质中为 \(\epsilon_0 \epsilon_r\)，其中 \(\epsilon_r\) 是相对电容率）。

    在幻灯片中，泊松方程具体表示为：

    \[
    \Delta \phi_{EI} = -\frac{\rho_{EI}}{\epsilon_0 \epsilon_r}
    \]

    1. **拉普拉斯算子 \(\Delta \phi_{EI}\)**：
       - 这是一个二阶偏微分算子，表示电势 \(\phi_{EI}\) 的空间变化率。具体形式为：
         \[
         \Delta \phi_{EI} = \frac{\partial^2 \phi_{EI}}{\partial x^2} + \frac   {\partial^2 \phi_{EI}}{\partial y^2} + \frac{\partial^2 \phi_{EI}} {\partial z^2}
         \]
       - 它衡量了电势在各个方向上的变化率的总和。

    2. **电荷密度 \(\rho_{EI}\)**：
       - 这是空间中的电荷分布情况，表示每单位体积中的电荷量。单位是库仑每立方米（C/ m³）。

    3. **电容率 \(\epsilon_0 \epsilon_r\)**：
       - \(\epsilon_0\) 是真空中的电容率，约为 \(8.854 \times 10^{-12} \, \text {F/m}\)（法拉每米）。
       - \(\epsilon_r\) 是介质的相对电容率，它表示介质对电场的响应程度。

    泊松方程的物理意义是描述电势如何在空间中因电荷分布而变化。根据电荷密度的分布，电势的二阶导数（拉普拉斯算子）与电荷密度成比例。

    例如，在静电学中，如果我们知道一个区域内的电荷分布 \(\rho_{EI}\)，我们可以通过  解泊松方程来确定该区域内的电势分布 \(\phi_{EI}\)。然后，通过电势的梯度，我们可以进一步求得电场 \(\vec{E}\)：

    \[
    \vec{E} = -\nabla \phi_{EI}
    \]

    总结起来，泊松方程是连接电荷分布与电势分布的重要方程，通过它可以从已知的电荷分布    推导出空间中的电势分布和电场分布。

#### 静电学中的电场
   - 在静电学中，电场可以通过电势 \(\phi_{EI}\) 来描述：
     \[
     \vec{E} = -\nabla \phi_{EI}
     \]
   - 这意味着电场是电势的梯度的负值。

#### 第一部分
   - 电场的散度为负的电势的拉普拉斯算子：
     \[
     \nabla \cdot \vec{E} = -\nabla^2 \phi_{EI} = -\Delta \phi_{EI}
     \]

---

## P7

### Fundamentals: ions in a electric field (4/5)

#### 泊松方程（Poisson equation）
   - 泊松方程的表达式是：
     \[
     \Delta \phi_{EI} = -\frac{\rho_{EI}}{\epsilon_0 \epsilon_r}
     \]
   - 其中，\(\Delta \phi_{EI}\) 是电势的拉普拉斯算子，\(\rho_{EI}\) 是电荷密度，\(\epsilon_0\) 是真空中的电容率，\(\epsilon_r\) 是相对电容率。

#### 高斯定律（Gauss' law）
   - 高斯定律的表达式是：
     \[
     \nabla \cdot \vec{D} = \rho_{EI}
     \]
   - 其中，\(\vec{D}\) 是电位移场，\(\rho_{EI}\) 是电荷密度。

#### 电位移场（Electric displacement field）
   - 电位移场 \(\vec{D}\) 的定义为：
     \[
     \vec{D} = \epsilon_0 \vec{E} + \vec{P}
     \]
   - 其中，\(\epsilon_0\) 是真空中的电容率，\(\vec{E}\) 是电场强度，\(\vec{P}\) 是极化强度。

#### 液体和各向同性固体（For liquids and isotropic solids）
   - 在液体和各向同性固体中，电场 \(\vec{E}\) 与极化强度 \(\vec{P}\) 成正比：
     \[
     \vec{D} = \epsilon_0 \vec{E} + \epsilon_0 \chi_e \vec{E} = \epsilon_0 \epsilon_r \vec{E}
     \]
   - 其中，\(\chi_e\) 是电极化率，\(\epsilon_r\) 是相对电容率。

#### 第二部分（Part 2）
   - 从高斯定律推导出泊松方程的另一种形式：
     \[
     \nabla \cdot \vec{E} = \frac{\rho_{EI}}{\epsilon_0 \epsilon_r}
     \]

右侧的图片继续显示在电场中的离子分布。红色大圆表示带负电荷的离子（δ-），蓝色小圆表示带正电荷的离子（δ+）。黑色边界上标有正负号，表示电场的方向。这个图例展示了电场中正负离子的相互作用和分布情况。

总结：
- 泊松方程描述了电势和电荷密度之间的关系。
- 高斯定律提供了电场和电荷分布的关系。
- 电位移场考虑了介质的极化效应。
- 在液体和各向同性固体中，电位移场可以用相对电容率来表示。

--- 

## P13

### Dielectric double layer: Helmholtz model

#### 原理：刚性离子层（Principle: rigid ion layer）
亥姆霍兹模型假设在电极表面和溶液中的离子之间存在一个刚性离子层。

#### 推导（Derivation）
1. **泊松方程**（Poisson equation）
   - 亥姆霍兹模型中的泊松方程为：
     \[
     \frac{d^2 \phi}{dx^2} = -\frac{\rho_{EI}}{\epsilon_0 \epsilon_r} = 0
     \]
   - 这表明电荷密度 \(\rho_{EI}\) 为零，即在刚性离子层内没有净电荷。

2. **解（Solution）**
   - 泊松方程的解为：
     \[
     \phi = -\frac{\phi_0}{r} x + \phi_0
     \]
   - 其中，\(\phi_0\) 是电势的初始值，\(r\) 是特征长度，\(x\) 是距离。

#### 限制（Limitations）
亥姆霍兹模型有以下限制：
   - 只适用于高电解质浓度的情况（High electrolyte concentration only）。
   - 只适用于低温环境（温度接近0 K）（Low temperatures \( T \approx 0 \, \text{K} \)）。

#### 图示解释
右侧的图片展示了介电双层结构：
   - 上方的灰色区域表示电极表面，带有正电荷（+）。
   - 绿色的圆圈表示带负电荷的离子（-），粉红色的圆圈表示带正电荷的离子（+）。
   - 这些离子在电极表面形成一个刚性离子层，靠近电极表面带负电荷的离子，而远离电极表面的区域带正电荷的离子。

总结：
亥姆霍兹模型通过假设刚性离子层来描述电极表面附近的电势分布，但仅适用于高电解质浓度和低温环境。泊松方程在该模型中的解反映了电势在刚性离子层内的线性变化。

---

