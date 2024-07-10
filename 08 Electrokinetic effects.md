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

## P18

### 介电双层：电动电位（Dielectric double layer: Zeta potential）

剪切面外的分子能够由于粘性力跟随主体流动

#### 电动电位由剪切面的电势定义
  - 电动电位（Zeta potential）是指在剪切面上的电势差。定义如下：
    \[
    \zeta = \phi(x_{\text{shear}}) - \phi(x \to \infty)
    \]
  - 其中，\(\zeta\) 是电动电位，\(\phi(x_{\text{shear}})\) 是剪切面上的电势，\(\phi(x \to \infty)\) 是远离表面时的电势（趋近于零）。

#### 剪切距离 \(x_{\text{shear}}\) 通常由德拜长度给出
  - 剪切距离 \(x_{\text{shear}}\) 通常用德拜长度 \(l_D\) 表示，德拜长度的公式如下：
    \[
    l_D = \sqrt{\frac{\epsilon_0 \epsilon_r k T}{e^2 \sum_i c_i z_i^{*2}}}
    \]
  - 其中，\(\epsilon_0\) 是真空中的电容率，\(\epsilon_r\) 是相对电容率，\(k\) 是玻尔兹曼常数，\(T\) 是温度，\(e\) 是电子电荷，\(c_i\) 是离子浓度，\(z_i^*\) 是离子的有效电荷数。

#### 图示解释
右侧的图片展示了电动电位的图示：

- 上方灰色区域表示带正电荷的电极表面（+）。
- 绿色圆圈表示带负电荷的离子（-），粉红色圆圈表示带正电荷的离子（+）。
- 剪切面（shear plane）用一条黑色实线表示，表示在该面内外的流体行为不同。
- 电势 \(\phi\) 随着距离 \(x\) 的变化曲线显示在左侧，电势在剪切面位置急剧下降，定义了电动电位 \(\zeta\)。
- 德拜长度 \(l_D\) 表示电势显著衰减的距离范围。

#### 总结

电动电位 \(\zeta\) 是描述剪切面处电势差的重要参数，它影响流体中离子的运动和分布。剪切距离 \(x_{\text{shear}}\) 通常由德拜长度来表征，而德拜长度是由溶液的电解质浓度和温度等因素决定的。这个模型对于理解电流体力学和电泳等现象非常重要。

---

## P47

### Simplified Navier-Stokes Equation for Microfluidic Flow

在微流体流动中，简化的Navier-Stokes方程如下所示：

\[ \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_z}{\partial r} \right) \right) = \frac{\Delta P}{L} + \epsilon_0 \epsilon_r \nabla^2 \phi_{El} \frac{\Delta V}{L} \]

这表示在微流体环境中，由于惯性项可以忽略，方程变得线性。因此，速度的叠加原理（superposition principle）在这种情况下是适用的。

#### 边界条件
- 在管道中心处，速度梯度为零，即：\[ \left. \frac{\partial v_z}{\partial r} \right|_{r=0} = 0 \]
- 在管道壁面处，速度为零，即：\[ v_z |_{r=R} = 0 \]

#### 简化后的方程
由于没有惯性项，Navier-Stokes方程变得线性，可以进行速度叠加。总速度 \( v_z(r) \) 可以表示为压力驱动速度和电渗驱动速度的叠加：

\[ v_z(r) = v_{z,P}(r) + v_{z,EO}(r) \]

#### Hagen-Poiseuille流动
由于压力梯度引起的速度分布为：

\[ v_{z,P}(r) = \frac{1}{4\eta} (R^2 - r^2) \frac{\Delta P}{L} \]

#### 电渗流动
由于电渗效应引起的速度分布为：

\[ v_{z,EO}(r) = \left( 1 - \frac{I_0(r/l_D)}{I_0(R/l_D)} \right) \frac{\epsilon_0 \epsilon_r \zeta}{\eta} \frac{\Delta V}{L} \]

其中：
- \( I_0 \) 是第一类零阶贝塞尔函数
- \( l_D \) 是德拜长度
- \(\epsilon_0\) 是真空介电常数
- \(\epsilon_r\) 是相对介电常数
- \(\zeta\) 是zeta电位

#### 结论
在微流体环境中，由于惯性力较小可以忽略，Navier-Stokes方程变得线性，这使得流体速度的不同分量（如压力驱动和电渗驱动）可以简单叠加。这种线性特性使得分析微流体系统中的流动行为更加简便。

### 关于线性性的讨论

#### 完整的Navier-Stokes方程
在不可压缩流体的情况下，NSE的完整形式为：

\[ \rho \left( \frac{\partial \mathbf{v}}{\partial t} + \mathbf{v} \cdot \nabla \mathbf{v} \right) = -\nabla p + \eta \nabla^2 \mathbf{v} + \mathbf{f} \]

其中：
- \(\rho\) 是流体的密度
- \(\mathbf{v}\) 是速度场
- \(p\) 是压力场
- \(\eta\) 是粘性系数
- \(\mathbf{f}\) 是外力（如电场力）

#### 惯性项的影响
在上述方程中，惯性项（即 \(\rho (\partial \mathbf{v}/\partial t + \mathbf{v} \cdot \nabla \mathbf{v})\)）是非线性的。具体而言：
- \(\partial \mathbf{v}/\partial t\) 是速度的时间导数，表示流体的加速度。
- \(\mathbf{v} \cdot \nabla \mathbf{v}\) 是速度的对流项，表示由于速度梯度引起的非线性变化。

非线性项的存在使得方程整体呈现非线性性质，这种情况下，两个速度场的叠加不再满足原方程，因为非线性项会产生交叉项。

#### 简化的Navier-Stokes方程
在低雷诺数条件下（即流体的惯性力远小于粘性力），惯性项可以忽略，简化后的NSE为：

\[ 0 = -\nabla p + \eta \nabla^2 \mathbf{v} + \mathbf{f} \]

或者在某些情况下，惯性项仅表现为常数项，不影响线性叠加性：

\[ \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_z}{\partial r} \right) \right) = \frac{\Delta P}{L} + \epsilon_0 \epsilon_r \nabla^2 \phi_{El} \frac{\Delta V}{L} \]

#### 线性可叠加性
在线性方程中，叠加原理（Superposition Principle）成立。这意味着如果\(\mathbf{v}_1\) 和 \(\mathbf{v}_2\) 是方程的解，则它们的线性组合 \(\mathbf{v} = a \mathbf{v}_1 + b \mathbf{v}_2\) 也是方程的解。具体而言，简化后的方程为：

\[ \eta \nabla^2 \mathbf{v} = -\nabla p + \mathbf{f} \]

在这种线性方程中，如果有两个解\(\mathbf{v}_1\) 和 \(\mathbf{v}_2\)，则：

\[ \eta \nabla^2 \mathbf{v}_1 = -\nabla p + \mathbf{f}_1 \]
\[ \eta \nabla^2 \mathbf{v}_2 = -\nabla p + \mathbf{f}_2 \]

那么其线性组合：

\[ \mathbf{v} = a \mathbf{v}_1 + b \mathbf{v}_2 \]

也是方程的解，因为：

\[ \eta \nabla^2 \mathbf{v} = \eta \nabla^2 (a \mathbf{v}_1 + b \mathbf{v}_2) = a (\eta \nabla^2 \mathbf{v}_1) + b (\eta \nabla^2 \mathbf{v}_2) = a (-\nabla p + \mathbf{f}_1) + b (-\nabla p + \mathbf{f}_2) \]

这仍然满足原方程。因此，在忽略惯性项的情况下，NSE是线性的，可以对不同驱动力（如压力驱动和电渗驱动）的速度场进行叠加。

#### 结论
当惯性项不存在时，Navier-Stokes方程简化为线性方程，因此满足叠加原理。这使得我们可以将由于不同驱动力（如压力差和电场）引起的速度场简单地叠加在一起，得到总的速度场。