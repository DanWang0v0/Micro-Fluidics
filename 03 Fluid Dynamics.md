## P2

# 学习目标（Learning Goals）

- **命名流体动力学的控制方程**（governing equations of fluid dynamics）并解释不同术语的物理意义。
- 对给定的流体问题，能够对**纳维-斯托克斯方程**（Navier-Stokes equations）进行合理的简化。
- 能够**解析地解决**（analytically solve）简化后的纳维-斯托克斯方程，并应用于某些示例。
- 能够描述**微流体流动**（microfluidic flows）的特征。

---

## P3

### 流体动力学的控制方程（The Governing Equations for Fluid Dynamics）

#### 基本守恒方程（Basic Conservation Equations）
- **纳维-斯托克斯方程**（Navier-Stokes equations）
  - **质量守恒**（Mass conservation）：也称为**连续性方程**（Continuity equation）。
  - **动量守恒**（Momentum conservation）。
- **能量守恒**（Energy conservation）：如果考虑热效应。

#### 纳维-斯托克斯方程（NSE）
纳维-斯托克斯方程是一组**偏微分方程**（partial differential equations，PDE），它们将流体的**密度场**（density field） \( \rho(\vec{x}, t) \) 与**速度场**（velocity field） \( \vec{v}(\vec{x}, t) \) 和相应的**压力分布**（pressure distribution） \( p(\vec{x}, t) \) 相关联。

#### 重要说明
纳维-斯托克斯方程在没有简化假设的情况下**无法解析求解**（cannot be solved analytically）。

---

## P10

### 质量守恒（连续性方程）（Conservation of Mass - Continuity Equation）

#### 微小控制体积内的质量流动（Mass Flow Through an Infinitesimal Small Control Volume）

#### 质量变化
控制体积内的质量变化等于通过控制体积表面的质量流动差异。

#### 数学表达式
对于一个微小的控制体积 \( dx \times dy \times dz \)，质量 \( m \) 的变化可以表示为：
\[ \frac{\partial}{\partial t} (m) = \frac{\partial}{\partial t} (\rho \, dx \, dy \, dz) \]

#### 进一步推导
考虑到密度 \(\rho\) 和体积 \( dx \, dy \, dz \) 的变化，我们可以进一步推导出连续性方程的具体形式。

#### 图示说明
右侧的图示展示了一个微小的控制体积 \( dx \times dy \times dz \)，其中 \( x \)、\( y \) 和 \( z \) 是坐标轴。

---

## P13

### 方程形式
质量守恒方程的不同形式如下：

#### 1. 基本形式
\[ \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \vec{v}) = 0 \]

#### 2. 展开形式
\[ \frac{\partial \rho}{\partial t} + \vec{v} \cdot \nabla \rho + \rho (\nabla \cdot \vec{v}) = 0 \]

#### 3. 实质导数形式
\[ \frac{D \rho}{D t} + \rho (\nabla \cdot \vec{v}) = 0 \]

### 不同术语的物理意义
- **实质导数**（Substantial/Material Derivative） \( \frac{D \rho}{D t} \)：
  - **局部导数**（Local derivative）：描述在固定位置上随时间的变化。
  - **对流导数**（Convective derivative）：描述由于流体运动引起的变化。
  - 实质导数是相对于时间的总导数。
  - 物理解释：实质导数给出了当观察者沿着流线（pathline）随流体元素漂浮时，函数 \( f \) 的时间变化率。

### 图示说明
右侧的图示展示了一个流体元素（fluidic element）沿着流线（pathline）运动的情况。

---

## P19

### 动量守恒 (Conservation of Momentum)

#### x方向上的动量方程 (The momentum equation in x-direction):

\[ \rho \left( \frac{\partial v_x}{\partial t} + v_x \frac{\partial v_x}{\partial x} + v_y \frac{\partial v_x}{\partial y} + v_z \frac{\partial v_x}{\partial z} \right) = \left( \frac{\partial \tau_{xx}}{\partial x} + \frac{\partial \tau_{yx}}{\partial y} + \frac{\partial \tau_{zx}}{\partial z} \right) + \rho g_x \]

- \(\rho\) 是密度 (density)
- \(v_x, v_y, v_z\) 分别是速度在x, y, z方向上的分量 (velocity components)
- \(\tau_{xx}, \tau_{yx}, \tau_{zx}\) 是应力张量 (stress tensor) 的分量
- \(g_x\) 是重力加速度在x方向上的分量 (gravitational acceleration)

#### 如何消除 \(\tau_{ij}\) (How to get rid of \(\tau_{ij}\))？

右侧的方程需要进一步转换 (The RHS needs to be further transformed):

- 假设各向同性的牛顿流体 (isotropic Newtonian fluid)，可以将应力张量 \(\tau\) 与粘度 \(\eta\) 和速度的偏导数联系起来 (relate the stress tensor \(\tau\) to the viscosity \(\eta\) and partial derivatives of the velocity)。
- 正应力可以与压力和正粘性应力相关联 (Normal stresses can be related to pressure and normal viscous stresses)。

#### 转换后的方程：

\[ \rho \left( \frac{\partial \vec{v}}{\partial t} + (\vec{v} \cdot \nabla) \vec{v} \right) = f_{\text{pressure}} + f_{\text{viscous}} + f_{\text{volume}} \]

进一步简化为：

\[ \rho \left( \frac{\partial \vec{v}}{\partial t} + (\vec{v} \cdot \nabla) \vec{v} \right) = -\nabla p + \nabla \cdot (\eta \nabla \vec{v}) + f_{\text{volume}} \]

- \(\frac{\partial \vec{v}}{\partial t}\) 是速度的时间导数 (time derivative of velocity)
- \((\vec{v} \cdot \nabla) \vec{v}\) 是对流项 (convective term)
- \(-\nabla p\) 是压力梯度力 (pressure gradient force)
- \(\nabla \cdot (\eta \nabla \vec{v})\) 是粘性力 (viscous force)
- \(f_{\text{volume}}\) 是体积力 (volume force)

#### 实质性加速度 (substantial acceleration):

\[ \rho \left( \frac{\partial \vec{v}}{\partial t} + (\vec{v} \cdot \nabla) \vec{v} \right) \]

这个表达式表示流体质点的实质性加速度 (substantial acceleration of a fluid particle)，包括局部加速度 (local acceleration) 和对流加速度 (convective acceleration)。

---

## P20

### 纳维-斯托克斯方程 (Navier-Stokes Equations)

#### 质量守恒 (Mass Conservation)
\[ \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \vec{v}) = 0 \]

- \(\rho\) 是密度 (density)
- \(\vec{v}\) 是速度矢量 (velocity vector)
- \(\nabla \cdot\) 表示散度 (divergence)

这个方程表示质量守恒，即流体的质量在时间和空间上保持不变。

#### 动量守恒 (Momentum Conservation)
\[ \frac{\partial}{\partial t} (\rho \vec{v}) + \vec{v} \cdot \nabla (\rho \vec{v}) = -\nabla p + \nabla \cdot (\eta \nabla \vec{v}) + f_{\text{volume}} \]

- \(\frac{\partial}{\partial t} (\rho \vec{v})\) 是动量的时间变化率 (time rate of change of momentum)
- \(\vec{v} \cdot \nabla (\rho \vec{v})\) 是对流项 (convective term)
- \(-\nabla p\) 是压力梯度力 (pressure gradient force)
- \(\nabla \cdot (\eta \nabla \vec{v})\) 是粘性力 (viscous force)
- \(f_{\text{volume}}\) 是体积力 (volume force)

这个方程表示动量守恒，即流体的动量在时间和空间上保持不变。

#### 备注 (Remarks)

- **梯度的表现形式**：梯度的表现形式取决于所使用的坐标系（例如笛卡尔坐标系、柱坐标系等）。
- **不可压缩牛顿流体的进一步简化**：对于不可压缩的牛顿流体，可以进一步简化方程。
- **热问题**：对于热问题，还需要考虑能量方程（这部分在本讲座中不涉及）。
- **体积力的类型**：体积力的类型包括重力 (\(f_{\text{vol}} = \rho \vec{g}\))、离心力 (\(f_{\text{vol}} = \rho \omega^2 \vec{r}\)) 或静电力 (\(f_{\text{vol}} = \rho_q \vec{E}(\vec{x})\)) 等。

---

## P23

### 微流体力学的特性：斯托克斯流动 (Characteristics of Microfluidics: Stokes Flow)

斯托克斯流动（Stokes Flow），也称为低雷诺数流动或爬行流动，是一种特殊的流体流动状态，通常发生在流体的惯性力可以忽略不计的情况下。斯托克斯流动的主要特征是流体的粘性力占主导地位，而惯性力非常小。这种流动状态通常出现在非常缓慢的流动或非常高粘度的流体中。

#### 斯托克斯流动的主要特征

1. **低雷诺数 (Low Reynolds Number)**：
   - 斯托克斯流动通常发生在雷诺数 \(Re < 1\) 的情况下。雷诺数是一个无量纲数，用来描述流体流动的惯性力与粘性力的比值。
   - 低雷诺数意味着粘性力远大于惯性力。

2. **线性化的纳维-斯托克斯方程 (Linearized Navier-Stokes Equations)**：
   - 在斯托克斯流动中，纳维-斯托克斯方程可以简化为线性形式，因为惯性项可以忽略不计。
   - 简化后的方程为：
     \[ \nabla p = \eta \nabla^2 \vec{v} \]
     其中 \(p\) 是压力，\(\eta\) 是流体的粘度，\(\vec{v}\) 是速度矢量。

3. **稳态流动 (Steady Flow)**：
   - 斯托克斯流动通常假设为稳态流动，即流体的速度和压力场不随时间变化。

4. **可预测性 (Predictability)**：
   - 由于惯性力可以忽略，斯托克斯流动是高度可预测的，流体的运动可以通过解析解或数值解精确描述。

#### 斯托克斯流动的应用

斯托克斯流动在许多科学和工程领域都有重要应用，特别是在微流体力学和生物流体力学中。例如：

- **微流体装置 (Microfluidic Devices)**：在微流体装置中，流体的流动通常是斯托克斯流动，因为流动速度非常低，且装置尺寸非常小。
- **生物流体力学 (Biological Fluid Mechanics)**：在生物系统中，例如细胞内部的流动，通常也是斯托克斯流动，因为流体的流动速度非常低，且粘性力占主导地位。
- **润滑理论 (Lubrication Theory)**：在润滑剂的流动中，斯托克斯流动模型可以用来描述润滑剂在狭窄间隙中的流动。

#### 斯托克斯流动的例子

- **悬浮颗粒的沉降 (Sedimentation of Suspended Particles)**：在低雷诺数条件下，颗粒在流体中的沉降速度可以通过斯托克斯定律计算。
- **毛细管中的流动 (Flow in Capillaries)**：在毛细管中，流体的流动通常是斯托克斯流动，因为毛细管的直径非常小，流动速度非常低。

总之，斯托克斯流动是一种重要的流动状态，适用于描述低雷诺数条件下的流体行为。

#### 如何简化纳维-斯托克斯方程以适用于斯托克斯流动？ (How can the NSE be simplified for Stokes flow?)

纳维-斯托克斯方程 (NSE):
\[ \frac{\partial}{\partial t} (\rho \vec{v}) + \vec{v} \cdot \nabla (\rho \vec{v}) = -\nabla p + \nabla \cdot (\mu \nabla \vec{v}) + f_{\text{volume}} \]

#### 简化条件 (Simplifications)
- **雷诺数 \(Re < 1\)**：惯性力可以忽略 (inertial forces can be neglected)。
- **稳态流动 (Steady flow)**：没有时间依赖性 (no time dependency)。
- **无体积力 (No volume forces)**。

#### 斯托克斯流动的泊松方程 (Poisson Equation for Stokes Flow)
\[ \nabla p = \eta \nabla^2 \vec{v} \]
- 驱动压力和摩擦力平衡 (Driving pressure and friction are balanced)。
- 可以得到解析解 (Analytical solution is possible)。

#### 详细解释

1. **纳维-斯托克斯方程 (NSE)**：
   - 这个方程描述了流体的动量守恒，包括惯性力、压力梯度力、粘性力和体积力。

2. **简化条件**：
   - **雷诺数 \(Re < 1\)**：在低雷诺数条件下，惯性力相对于粘性力可以忽略，因此可以简化方程。
   - **稳态流动**：假设流动是稳态的，即流体的性质不随时间变化。
   - **无体积力**：假设没有体积力作用，例如重力或电场力。

3. **泊松方程 (Poisson Equation)**：
   - 通过上述简化条件，纳维-斯托克斯方程可以简化为泊松方程。
   - 这个方程表明驱动压力和摩擦力之间的平衡。
   - 由于方程的简化，可以得到解析解，从而更容易分析和计算斯托克斯流动。

这些简化使得在微流体力学中分析斯托克斯流动变得更加可行和直观。

---

## P24

### 微流体力学的特性：雷诺数 (Characteristics of Microfluidics: Reynolds Number)

#### 使用雷诺数定义典型的流动状态 (Using the Reynolds number, typical flow regimes can be defined)

1. **层流：爬行/斯托克斯流动 (Laminar: Creeping / Stokes flow)**
   - \(Re < 1\)
   - **无横向对流 (No lateral convection)**：流体层之间没有横向的混合。
   - **相邻层流不干扰 (Adjacent lamellae do not interfere)**：相邻的流体层之间没有干扰。

2. **层流：中间状态 (Laminar: Intermediate)**
   - \(1 < Re < Re^*\)
   - **横向对流变得重要 (Lateral convection becomes important)**：流体层之间开始有横向的混合。

3. **湍流 (Turbulent)**
   - \(Re > Re^*\)
   - 流动变得不规则和混乱。

#### 详细解释

#### 雷诺数 (Reynolds Number)
雷诺数是一个无量纲数，用来描述流体流动的特性。它的定义为：
\[ Re = \frac{\rho v L}{\mu} \]
其中：
- \(\rho\) 是流体的密度 (density)
- \(v\) 是流体的速度 (velocity)
- \(L\) 是特征长度 (characteristic length)
- \(\mu\) 是流体的动力粘度 (dynamic viscosity)

#### 流动状态 (Flow Regimes)
- **层流 (Laminar Flow)**：流体分层流动，各层之间没有混合。低雷诺数（\(Re < 1\)）下，流动是稳定的，称为斯托克斯流动。
- **中间层流 (Intermediate Laminar Flow)**：在中等雷诺数范围内（\(1 < Re < Re^*\)），横向对流开始变得重要，流体层之间开始有混合。
- **湍流 (Turbulent Flow)**：高雷诺数（\(Re > Re^*\)）下，流动变得不规则和混乱，流体层之间有强烈的混合。

#### 图示说明
- **上图**：展示了层流状态下的流动，流体层之间没有混合。
- **下图**：展示了湍流状态下的流动，流动变得不规则和混乱。

---

## P25

### 层流与湍流 (Laminar vs Turbulent Flow)

#### 层流 (Laminar Flow)
- **由摩擦主导 (Dominated by friction)**：流体层之间的相互作用主要是由于粘性摩擦力。
- **液体层（层流）以不同速度平滑地滑动 (Liquid sheets (lamellae) with different velocities slide smoothly along each other)**：
  - **混合仅由于扩散 (Mixing only due to diffusion)**：流体层之间的混合仅通过分子扩散进行，没有宏观的混合。
- **层流是可预测的 (Laminar flow is predictable)**：流动是稳定和可预测的。

右侧图示：
- **上图**：展示了层流状态下的流动，流体层之间没有混合，流动方向一致。

#### 湍流 (Turbulent Flow)
- **由对流主导 (Dominated by convection)**：流体层之间的相互作用主要是由于对流。
- **液体层分解并形成涡流、旋涡或漩涡 (Lamellae disintegrate and form eddies, swirls or vortices)**：流体层之间的界限变得不清晰，形成复杂的流动结构。
- **湍流是混乱的 (Turbulent flow is chaotic)**：流动是不规则和不可预测的。

右侧图示：
- **下图**：展示了湍流状态下的流动，流体层之间有强烈的混合，流动方向不一致，形成涡流和旋涡。

### 图示说明
- **左侧图表**：
  - **上图**：层流的速度随时间变化图，显示速度是恒定的。
  - **下图**：湍流的速度随时间变化图，显示速度是波动和不规则的。

---

# Examples

## P30

### 1. Reynold number in microfluidics

### 临界雷诺数及其在微流体装置中的影响 (Critical Reynolds Number and Consequences for Micro Devices)

#### 临界雷诺数 \(Re^*\) 取决于实际问题 (The critical Reynolds number \(Re^*\) depends on the actual problem)
- **对于管道流动 (For pipe flows)**：\(Re^* \approx 2300\)
- **随着雷诺数的增加，流动的湍流特性增加 (As Re increases further, the turbulent character of flow increases)**

#### 示例：在微流体装置中达到临界雷诺数所需的速度 (Example: Velocity that is necessary to reach the critical Reynolds number in a micro device)
- 给定参数：
  - \( l = 100 \, \mu m \)
  - \( \rho = 1000 \, \frac{kg}{m^3} \)
  - \( \eta = 1.0016 \, mPa \)（水的粘度）

- 计算速度 \( v^* \)：
  \[ v^* = \frac{Re^* \cdot \eta}{l \cdot \rho} = \frac{2300 \cdot 1.0016 \times 10^{-3} \, Pa \cdot s}{100 \times 10^{-6} \, m \cdot 1000 \, \frac{kg}{m^3}} = 23 \, \frac{m}{s} \]

- **在微流体装置中，临界雷诺数很难达到 (In microfluidics the critical Reynolds number is hardly reached)**。
- **一般来说，可以假设微流体装置中的流动是层流 (In general, it can be assumed that flow in micro devices is laminar)**。

---

## P33

### 管道中压力驱动流动的建模 (Pressure Driven Flow in a Pipe – Modelling)

#### 建模参数 (Parameters)
- **半径 \(R\) (Radius \(R\))**：管道的半径。
- **流体性质 (Fluid properties)**：
  - 动力粘度 \(\eta\) (dynamic viscosity \(\eta\))
  - 密度 \(\rho\) (density \(\rho\))
- **管道长度 \(L\) (Length of the channel/pipe \(L\))**：管道的长度。
- **压力差 \(\Delta P\) (Pressure difference \(\Delta P\))**：管道两端的压力差。

#### 假设 (Assumptions)
- **无滑移边界条件 (No slip boundary conditions)**：在管壁处，流体速度为零，即 \(\vec{v}|_{\text{wall}} = 0\)。
- **无体积力 (No volume forces)**：假设没有体积力作用，例如重力或电场力。
- **稳态流动 (Stationary flow)**：假设流动是稳态的，即流体的性质不随时间变化。
- **恒定压力差 (Constant pressure difference)**：假设管道两端的压力差是恒定的。
- **完全发展的层流 (Fully developed laminar flow)**：假设流动已经完全发展，速度分布不再变化。

#### 方法 (Approach)
- **圆柱对称性 (Cylindrical symmetry)**：使用圆柱坐标系 \((r, \phi, z)\) 来描述三维问题的二维简化。
  - \(r\)：径向坐标
  - \(\phi\)：角向坐标
  - \(z\)：轴向坐标

这张幻灯片展示了不可压缩牛顿流体在圆柱坐标系下的纳维-斯托克斯方程（NSE），用于描述管道中压力驱动流动的数学模型。

### 管道中压力驱动流动的数学描述 (Pressure Driven Flow in a Pipe – Mathematical Description)

#### 圆柱坐标系下不可压缩牛顿流体的纳维-斯托克斯方程 (NSE for an Incompressible, Newtonian Fluid in Cylindrical Coordinates)

1. **连续性方程 (Continuity Equation)**：
   \[ \frac{1}{r} \frac{\partial (r v_r)}{\partial r} + \frac{1}{r} \frac{\partial v_\phi}{\partial \phi} + \frac{\partial v_z}{\partial z} = 0 \]

2. **动量方程 (Momentum Equations)**：
   - **径向动量方程 (Radial Momentum Equation)**：
     \[
     \rho \left( \frac{\partial v_r}{\partial t} + v_r \frac{\partial v_r}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_r}{\partial \phi} - \frac{v_\phi^2}{r} + v_z \frac{\partial v_r}{\partial z} \right) = -\frac{\partial p}{\partial r} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_r}{\partial r} \right) - \frac{v_r}{r^2} + \frac{1}{r^2} \frac{\partial^2 v_r}{\partial \phi^2} - \frac{2}{r^2} \frac{\partial v_\phi}{\partial \phi} + \frac{\partial^2 v_r}{\partial z^2} \right) + f_r
     \]

   - **角向动量方程 (Azimuthal Momentum Equation)**：
     \[
     \rho \left( \frac{\partial v_\phi}{\partial t} + v_r \frac{\partial v_\phi}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_\phi}{\partial \phi} + \frac{v_r v_\phi}{r} + v_z \frac{\partial v_\phi}{\partial z} \right) = -\frac{1}{r} \frac{\partial p}{\partial \phi} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_\phi}{\partial r} \right) - \frac{v_\phi}{r^2} + \frac{1}{r^2} \frac{\partial^2 v_\phi}{\partial \phi^2} + \frac{2}{r^2} \frac{\partial v_r}{\partial \phi} + \frac{\partial^2 v_\phi}{\partial z^2} \right) + f_\phi
     \]

   - **轴向动量方程 (Axial Momentum Equation)**：
     \[
     \rho \left( \frac{\partial v_z}{\partial t} + v_r \frac{\partial v_z}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_z}{\partial \phi} + v_z \frac{\partial v_z}{\partial z} \right) = -\frac{\partial p}{\partial z} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_z}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 v_z}{\partial \phi^2} + \frac{\partial^2 v_z}{\partial z^2} \right) + f_z
     \]

#### 方程中的符号解释
- \(\rho\)：流体密度
- \(v_r, v_\phi, v_z\)：分别是径向、角向和轴向的速度分量
- \(p\)：压力
- \(\eta\)：流体的动力粘度
- \(f_r, f_\phi, f_z\)：分别是径向、角向和轴向的体积力

### 管道中压力驱动流动的数学描述 (Pressure Driven Flow in a Pipe – Mathematical Description)

#### 简化后的纳维-斯托克斯方程 (Simplified Navier-Stokes Equations)

1. **连续性方程 (Continuity Equation)**：
   \[ \frac{1}{r} \frac{\partial (r v_r)}{\partial r} + \frac{1}{r} \frac{\partial v_\phi}{\partial \phi} + \frac{\partial v_z}{\partial z} = 0 \]

2. **动量方程 (Momentum Equations)**：
   - **径向动量方程 (Radial Momentum Equation)**：
     \[
     \rho \left( v_r \frac{\partial v_r}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_r}{\partial \phi} - \frac{v_\phi^2}{r} + v_z \frac{\partial v_r}{\partial z} \right) = -\frac{\partial p}{\partial r} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_r}{\partial r} \right) - \frac{v_r}{r^2} + \frac{1}{r^2} \frac{\partial^2 v_r}{\partial \phi^2} - \frac{2}{r^2} \frac{\partial v_\phi}{\partial \phi} + \frac{\partial^2 v_r}{\partial z^2} \right)
     \]

   - **角向动量方程 (Azimuthal Momentum Equation)**：
     \[
     \rho \left( v_r \frac{\partial v_\phi}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_\phi}{\partial \phi} + \frac{v_r v_\phi}{r} + v_z \frac{\partial v_\phi}{\partial z} \right) = -\frac{1}{r} \frac{\partial p}{\partial \phi} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_\phi}{\partial r} \right) - \frac{v_\phi}{r^2} + \frac{1}{r^2} \frac{\partial^2 v_\phi}{\partial \phi^2} + \frac{2}{r^2} \frac{\partial v_r}{\partial \phi} + \frac{\partial^2 v_\phi}{\partial z^2} \right)
     \]

   - **轴向动量方程 (Axial Momentum Equation)**：
     \[
     \rho \left( v_r \frac{\partial v_z}{\partial r} + \frac{v_\phi}{r} \frac{\partial v_z}{\partial \phi} + v_z \frac{\partial v_z}{\partial z} \right) = -\frac{\partial p}{\partial z} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_z}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 v_z}{\partial \phi^2} + \frac{\partial^2 v_z}{\partial z^2} \right)
     \]

#### 简化条件 (Simplifications)

1. **二维描述 (2-D Description)**：
   - 假设流动是轴对称的，因此可以忽略角向变化，即 \(\frac{\partial}{\partial \phi} = 0\)。

2. **稳态流动 (Steady/Stationary Flow)**：
   - 假设流动是稳态的，即不随时间变化，因此可以忽略时间导数项，即 \(\frac{\partial}{\partial t} = 0\)。

3. **无重力/外力 (No Gravity/External Forces)**：
   - 假设没有体积力作用，例如重力或电场力，因此可以忽略体积力项 \(f_r, f_\phi, f_z\)。

4. **完全发展的流动 (Fully Developed Flow)**：
   - 假设流动已经完全发展，即速度分布不再变化，因此可以忽略径向和角向的速度导数项。

### 管道中压力驱动流动的求解 (Pressure Driven Flow in a Pipe - Solving)

#### 简化后的方程 (Simplified Equations)

1. **连续性方程 (Continuity Equation)**：
   \[ \frac{1}{r} \frac{\partial (r v_r)}{\partial r} = 0 \quad \text{(I)} \]

2. **径向动量方程 (Radial Momentum Equation)**：
   \[ \rho \left( v_r \frac{\partial v_r}{\partial r} \right) = -\frac{\partial p}{\partial r} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_r}{\partial r} \right) - \frac{v_r}{r^2} \right) \quad \text{(II)} \]

3. **轴向动量方程 (Axial Momentum Equation)**：
   \[ -\frac{\partial p}{\partial z} + \eta \left( \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial v_z}{\partial r} \right) \right) = 0 \quad \text{(III)} \]

#### 使用简化后的连续性方程求解 \(v_r\) (Using the Simplified Continuity Equation to Solve for \(v_r\))

1. **连续性方程 (I)**：
   \[ \frac{1}{r} \frac{\partial (r v_r)}{\partial r} = 0 \]
   这意味着：
   \[ r v_r = c \]
   其中 \(c\) 是一个常数。

2. **边界条件 (Boundary Condition)**：
   在管壁处，流体速度为零，即：
   \[ v_r(R) = 0 \]
   因此：
   \[ c = 0 \]
   所以：
   \[ v_r(r) = 0 \]

3. **径向动量方程 (II)**：
   由于 \(v_r = 0\)，径向动量方程简化为：
   \[ 0 = -\frac{\partial p}{\partial r} \]
   这意味着：
   \[ \frac{\partial p}{\partial r} = 0 \]

---

## P41

### 3. Hagen-Poiseuille Law

#### Question: 

如何通过管道中的流量和压力之间的关系？ (How to Obtain the Relation Between Flowrate and Pressure Through the Channel?)

#### 起点：压力驱动管道内的速度分布 (Starting Point: Velocity Profile Inside a Pressure Driven Pipe)
\[ v_z(r) = \frac{\Delta P}{4 \eta L} (R^2 - r^2) \]

- \(v_z(r)\)：轴向速度分布
- \(\Delta P\)：压力差
- \(\eta\)：流体的动力粘度
- \(L\)：管道长度
- \(R\)：管道半径
- \(r\)：径向位置

#### 通过速度积分得到流量 (Integration of the Velocity Yields the Flowrate)
\[ Q = \iint v_z \, dA \]

- \(Q\)：流量
- \(dA\)：微小面积元

具体积分过程：
\[ \int_0^{2\pi} \int_0^R v_z \, r \, dr \, d\phi = \int_0^{2\pi} \int_0^R \left( \frac{\Delta P}{4 \eta L} (R^2 - r^2) \right) r \, dr \, d\phi \]

计算结果：
\[ \int_0^{2\pi} \int_0^R \left( \frac{\Delta P}{4 \eta L} (R^2 - r^2) \right) r \, dr \, d\phi = \frac{\pi R^4 \Delta P}{8 \eta L} \]

#### Hagen-Poiseuille定律 (Hagen-Poiseuille Law)
\[ \Delta P = \frac{8 \eta L}{\pi R^4} Q \]

---

## P42

### Hagen-Poiseuille定律 (Hagen-Poiseuille Law)

#### 例子：通过泵驱动的圆形微通道中的水流 (Example: Water Through a Circular Microchannel Driven by a Pump)

给定参数：
- \(\Delta P = 0.1 \, \text{bar} = 10000 \, \text{Pa}\)
- \(D = 100 \, \mu m\)（直径）
- \(L = 10 \, \text{cm}\)（长度）
- \(\eta = 0.001 \, \text{Pa} \cdot \text{s}\)（水的动力粘度）
- \(\rho = 997 \, \text{kg/m}^3\)（水的密度）

#### 结果 (Results)

1. **最大速度 \(v_{z,\text{max}}\) 和平均速度 \(v_{z,\text{mean}}\)**：
   \[ v_{z,\text{max}} = \frac{\Delta P}{4 \eta L} R^2 = 0.25 \, \frac{m}{s} \]
   \[ v_{z,\text{mean}} = \frac{\Delta P}{8 \eta L} R^2 = 0.125 \, \frac{m}{s} = 0.45 \, \frac{km}{h} \]

   - 比较示例1中的结果：\(v_{\text{crit}} = 23 \, \frac{m}{s} = 82.8 \, \frac{km}{h}\)

2. **流量 \(Q\)**：
   \[ Q = \frac{\pi R^4 \Delta P}{8 \eta L} \approx 3.9 \, \mu L/s \]

3. **雷诺数 \(Re\)**：
   \[ Re = \frac{\rho l_{\text{char}} v_{\text{mean}}}{\eta} \approx 12.5 \]

4. **达到抛物线速度分布所需的长度 \(l_{\text{developing}}\)**：
   \[ l_{\text{developing}} = 0.05 \cdot Re \cdot D = 62.5 \, \mu m \]

达到抛物线速度分布所需的长度 \(l_{\text{developing}}\) 和题目中给的管道长度 \(L\) 是两个不同的概念，它们在流体力学中的意义和应用有所不同。

- ##### 达到抛物线速度分布所需的长度 \(l_{\text{developing}}\)
  - **定义**：这是流体从进入管道开始，到达到完全发展流动（即抛物线速度分布）所需的距离。
  - **意义**：在这个长度范围内，流体的速度分布从入口处的平坦分布逐渐发展为稳定的抛物线分布。这个过程称为流动发展过程。
  - **计算公式**：
   \[ l_{\text{developing}} = 0.05 \cdot Re \cdot D \]
   其中 \(Re\) 是雷诺数，\(D\) 是管道直径。
   - \(l_{\text{developing}}\) 是管道长度 \(L\) 的一部分，表示流动从入口到达到完全发展所需的距离。
     - 如果 \(L > l_{\text{developing}}\)，则在 \(L - l_{\text{developing}}\) 的长度范围内，流动是完全发展的。
     - 如果 \(L \leq l_{\text{developing}}\)，则整个管道内的流动可能都处于发展阶段，尚未达到完全发展。

