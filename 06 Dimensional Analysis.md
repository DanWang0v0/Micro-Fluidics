## P4

### Motivation for Dimensional Analysis

#### 1. 压降的参数分析

**问题描述**：
为了确定在管道流动中每单位长度的压降，相关的参数包括：
- 管道直径 \( D \)
- 流体密度 \( \rho \)
- 流体的动力粘度 \( \eta \)
- 流体的平均流速 \( v \)

这些参数共同决定了管道中的压降。

**数学表示**：
压降 \( \Delta p \) 作为各参数的函数可以表示为：
\[ \Delta p_l = f(D, \rho, \eta, v) \]
其中 \( \Delta p_l \) 是每单位长度的压降。

#### 2. 需要大量实验来评估功能关系

**复杂性**：
直接通过实验来确定这些参数之间的关系可能非常复杂，涉及大量实验数据：
- 每个参数变化都需要进行一系列实验，以捕捉其对压降的影响。
- 随着参数数量的增加，实验的数量成倍增加，使得实验设计和数据分析变得非常复杂且费时费力。

通过量纲分析，可以减少需要考虑的独立参数数量，从而简化实验设计和数据分析过程。

#### 3. 使用量纲分析简化问题

**简化方法**：
通过量纲分析，我们可以将相关参数组合成无量纲组，这些组在物理上具有明确的意义。这样做有以下优点：
- 减少独立变量的数量，简化问题的复杂性。
- 通过无量纲数，可以更容易地理解和预测物理现象。

量纲分析的主要目的是通过将物理量组合成无量纲组，减少问题的复杂性，使得实验和分析更为简便和直观。

---

## P7:

### "Guessing" Dimensional Numbers

如何通过合理推测和物理关系导出无量纲数。

#### 无量纲数的特点

无量纲数通常表示物理量的比值：
- 力、能量或速度
- 通过适当的物理量关系可以导出无量纲数

#### 例子：管道中的压降

以管道中的压降为例：

- **压降 \(\Delta p_l\)** 可以解释为压降，动态压强表示为 \(\frac{\rho v^2}{2}\)
- 无量纲数 \(\frac{\Delta p_l}{\frac{\rho v^2}{2}}\) 表示压降与动态压强的比值
- 另一个无量纲数 \(\frac{\rho v D}{\eta}\) 表示惯性力与粘性力的比值（即Reynolds数）

##### 解释：

- 压降 \(\Delta p_l\) 与动态压强的比值可以用来衡量流动中的阻力。
- Reynolds数 \(\text{Re} = \frac{\rho v D}{\eta}\) 用于描述流动的特性，帮助判断流动是层流还是湍流。

#### 图示解释

- 右上角的示意图展示了一个管道流动的模型，其中流速为 \(v\)，管径为 \(D\)，流体密度为 \(\rho\)，粘度为 \(\eta\)，以及单位长度的压降 \(\Delta p_l\)。
- 右下角的图表展示了压降与Reynolds数的关系，表明随着Reynolds数的变化，压降的无量纲比值变化情况。

### 总结

这一页通过示例展示了如何通过推测和物理关系导出无量纲数。具体来说，通过管道流动的例子，我们看到无量纲数如压降比值和Reynolds数如何帮助我们理解流体力学中的不同现象和特性。

---

## P8

### Dimensionless Form of the Navier-Stokes Equation

#### 1. 基本方程

首先，我们有纳维-斯托克斯方程：
\[ \rho \left( \frac{\partial \vec{v}}{\partial t} + \vec{v} \cdot \nabla \vec{v} \right) = -\nabla p + \eta \nabla^2 \vec{v} + \rho \vec{g} \]

#### 2. 引入无量纲变量

通过引入无量纲变量，将方程无量纲化：
\[ \tilde{v}_x = \frac{v_x}{v_s}, \quad \tilde{v}_y = \frac{v_y}{v_s}, \quad \tilde{v}_z = \frac{v_z}{v_s} \]
\[ \tilde{x} = \frac{x}{L_s}, \quad \tilde{y} = \frac{y}{L_s}, \quad \tilde{z} = \frac{z}{L_s} \]
\[ \tilde{t} = \frac{t}{t_s}, \quad \tilde{p} = \frac{p}{p_s}, \quad \tilde{g} = \frac{g}{g_s} \]

- 速度：\( \tilde{v}_x, \tilde{v}_y, \tilde{v}_z \)
- 空间坐标：\( \tilde{x}, \tilde{y}, \tilde{z} \)
- 时间：\( \tilde{t} \)
- 压力：\( \tilde{p} \)
- 重力加速度：\( \tilde{g} \)

这里，\( v_s \)、\( L_s \)、\( t_s \)、\( p_s \)、\( g_s \) 是相应的标度参数，用于无量纲化。

#### 3. 导数的规则

对导数的无量纲化规则为：
\[ \frac{d^n x}{d t^n} = \frac{L_s}{t_s^n} \frac{d^n \tilde{x}}{d \tilde{t}^n} \]

---

## P9

### Dimensionless Form of the NSE

#### 纳维-斯托克斯方程的无量纲形式

这一页详细展示了如何将纳维-斯托克斯方程无量纲化的步骤。

#### 1. NSE的有量纲形式

首先，我们从有量纲的纳维-斯托克斯方程开始：
\[ \rho \left( \frac{\partial \vec{v}}{\partial t} + \vec{v} \cdot \nabla \vec{v} \right) = -\nabla p + \eta \nabla^2 \vec{v} + \rho \vec{g} \]

#### 2. 代入无量纲变量

将无量纲变量代入NSE中：
\[ \tilde{\vec{v}} = \frac{\vec{v}}{v_s}, \quad \tilde{\vec{x}} = \frac{\vec{x}}{L_s}, \quad \tilde{t} = \frac{t}{t_s}, \quad \tilde{p} = \frac{p}{p_s} \]
\[ \nabla = \frac{1}{L_s} \tilde{\nabla} \]

代入后的方程为：
\[ \rho \left( \frac{v_s}{t_s} \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + v_s \tilde{\vec{v}} \cdot \frac{1}{L_s} \tilde{\nabla} \tilde{\vec{v}} \right) = -\frac{p_s}{L_s} \tilde{\nabla} \tilde{p} + \eta \left( \frac{v_s}{L_s} \right)^2 \tilde{\nabla}^2 \tilde{\vec{v}} + \rho g_s \tilde{\vec{g}} \]

#### 3. 归一化方程

将方程中的每一项除以 \(\frac{\eta v_s}{L_s^2}\)，得到：
\[ \frac{\rho L_s}{\eta t_s} \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \frac{\rho v_s L_s}{\eta} \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} = -\frac{p_s L_s}{\eta v_s} \tilde{\nabla} \tilde{p} + \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{\rho g_s L_s^2}{\eta v_s} \tilde{\vec{g}} \]

---

## P10

### Dimensionless Form of the NSE (Continued)

#### 纳维-斯托克斯方程的无量纲形式（续）

#### 1. 无量纲化后的方程

前一页我们得到了如下形式的方程：
\[ \frac{\rho L_s^2}{\eta t_s} \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \frac{\rho v_s L_s}{\eta} \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} = -\frac{p_s L_s}{\eta v_s} \tilde{\nabla} \tilde{p} + \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{\rho g_s L_s^2}{\eta v_s} \tilde{\vec{g}} \]

#### 2. 设定时间标度

设定时间标度 \( t_s = \frac{L_s}{v_s} \)，代入方程得到：
\[ \frac{\rho L_s^2}{\eta t_s} = \frac{\rho L_s^2}{\eta \frac{L_s}{v_s}} = \frac{\rho v_s L_s}{\eta} \]

于是方程变为：
\[ \frac{\rho v_s L_s}{\eta} \left( \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} \right) = -\frac{p_s L_s}{\eta v_s} \tilde{\nabla} \tilde{p} + \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{\rho g_s L_s^2}{\eta v_s} \tilde{\vec{g}} \]

#### 3. 引入Reynolds数

通过除以 \(\frac{\rho v_s L_s}{\eta}\) 可以引入Reynolds数：
\[ \text{Re} \left( \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} \right) = -\frac{p_s L_s}{\eta v_s} \tilde{\nabla} \tilde{p} + \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{\rho g_s L_s^2}{\eta v_s} \tilde{\vec{g}} \]

其中Reynolds数定义为：
\[ \text{Re} = \frac{\rho v_s L_s}{\eta} \]

---

## P11

### Dimensionless Form of the NSE

#### 1. 除以Reynolds数

我们从前一页得到的无量纲化方程开始：
\[ \frac{\rho v_s L_s}{\eta} \left( \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} \right) = -\frac{p_s L_s}{\eta v_s} \tilde{\nabla} \tilde{p} + \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{\rho g_s L_s^2}{\eta v_s} \tilde{\vec{g}} \]

将方程除以Reynolds数：
\[ \text{Re} = \frac{\rho v_s L_s}{\eta} \]

方程变为：
\[ \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} = -\frac{p_s}{\rho v_s^2} \tilde{\nabla} \tilde{p} + \frac{\eta}{\rho v_s L_s} \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{g_s L_s}{v_s^2} \tilde{\vec{g}} \]

#### 2. 引入Euler数和Froude数

我们定义：
\[ \text{Eu} = \frac{p_s}{\rho v_s^2} \]
\[ \text{Fr} = \frac{v_s}{\sqrt{g_s L_s}} \]

方程变为：
\[ \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} = -\text{Eu} \tilde{\nabla} \tilde{p} + \frac{1}{\text{Re}} \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{1}{\text{Fr}^2} \tilde{\vec{g}} \]

#### 3. 解释所得到的项

- **Euler数（Eu）** 表示压力力与惯性力的比值：
\[ \text{Eu} = \frac{p_s}{\rho v_s^2} \]
- **Froude数（Fr）** 表示惯性力与重力的比值：
\[ \text{Fr} = \frac{v_s}{\sqrt{g_s L_s}} \]

---

## P12

### 无量纲化的纳维-斯托克斯方程

#### 1. 无量纲方程的形式

无量纲的纳维-斯托克斯方程的最常见形式为：
\[ \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \tilde{\nabla} \tilde{\vec{v}} = -\text{Eu} \tilde{\nabla} \tilde{p} + \frac{1}{\text{Re}} \tilde{\nabla}^2 \tilde{\vec{v}} + \frac{1}{\text{Fr}^2} \tilde{\vec{g}} \]

其中：
- \(\text{Eu}\) 是欧拉数，表示压力力与惯性力的比值。
- \(\text{Re}\) 是雷诺数，表示惯性力与粘性力的比值。
- \(\text{Fr}\) 是弗劳德数，表示惯性力与重力的比值。

#### 2. 备注

- **NSE的无量纲化可以通过多种不同方式完成**
  不同的方法会导致方程的无量纲形式有所不同。

- **最终形式取决于尺度常数的任意选择**
  尺度常数的选择是无量纲化过程中的一个重要步骤，不同的选择会导致不同的无量纲数。

- **“合适”的尺度常数/无量纲数的选择取决于需要考虑的物理效应和问题类型**
  在进行无量纲化时，需要根据具体的物理问题和需要分析的物理效应选择合适的尺度常数和无量纲数。

- **并非所有方法都能得到有物理意义的无量纲数**
  只有在正确选择尺度常数的情况下，得到的无量纲数才具有物理意义。

---

## P13

### Buckingham Π Theorem

布金汉姆π定理是一个正式的方法，用于推导给定问题的无量纲数，即使控制方程的形式尚不明确。

#### 陈述

- **如果一个物理有意义的方程 \( f \) 涉及一定数量 \( n \) 的物理变量，并且 \( k \) 是维度矩阵的秩，则原始表达式等同于一个由 \( p = n - k \) 个由原始变量构造的无量纲参数组成的方程。**

  这一陈述指出，在一个物理问题中，涉及 \( n \) 个物理变量，并且这些变量的维度矩阵具有秩 \( k \)，那么可以将这个问题表示为一个包含 \( p = n - k \) 个无量纲参数的方程。

#### “数学”表述

- **如果一个方程 \( f(q_1, q_2, ..., q_n) \) 包含 \( n \) 个物理变量，并且这些变量可以用 \( k \) 个独立的物理单位表示，则存在一个函数 \( F(\pi_1, \pi_2, ..., \pi_p) \)，其中 \( \pi_i \) 是由 \( q_i \) 构造的无量纲参数。**

  数学上，可以将物理方程转换为无量纲方程。设 \( f \) 是一个包含 \( n \) 个物理变量 \( q_1, q_2, ..., q_n \) 的方程，这些变量可以用 \( k \) 个独立的物理单位表示。根据布金汉姆π定理，这个方程可以表示为一个新的方程 \( F(\pi_1, \pi_2, ..., \pi_p) \)，其中 \( \pi_i \) 是由 \( q_i \) 构造的无量纲参数，且 \( p = n - k \)。

  \[ \pi_i = q_1^{a_1} q_2^{a_2} ... q_n^{a_n} \]

  这意味着，可以通过将原始物理变量 \( q_i \) 组合成 \( p \) 个无量纲参数 \( \pi_i \)，来简化物理问题的分析。

#### 应用

布金汉姆π定理广泛应用于流体力学、热力学和其他工程领域，用于无量纲化控制方程，以简化分析和实验设计。

---

## P14

### Buckingham Π Theorem: manual

#### 1. 识别 \( k \) 个独立的物理单位
- 基本单位不能从其他单位推导出来（例如：长度 \([m]\)，时间 \([s]\)）。
- 导出单位/次要单位可以从基本单位构建（例如：速度 \([m/s]\)）。
- 根据所选的物理单位集，无量纲参数会有所不同！无量纲参数不是唯一的！

#### 2. 写下维度矩阵 \( M \)
- 维度矩阵 \( M \) 的行是 \( k \) 个物理单位（“维度”），列是 \( n \) 个变量。

#### 3. 求解方程 \( M \cdot \vec{v} = 0 \)
- 通过求解该方程，可以得到无量纲参数的表达式。

#### 4. 解释得到的无量纲参数
- 对所获得的无量纲参数进行物理意义上的解释和分析。

---

## P15

### Scaling laws

#### 如何解释宏观世界和微观世界之间的差异？
- 物理量（例如力）随着尺寸的不同而不同

#### 比例定律
- 比例定律表达了在保持其他量不变的情况下，物理量随给定系统或物体的大小变化。
  - 密度、粘度等强度性质通常与尺寸无关

图示展示了两种不同的尺度情况下的比例变化。左图是举重者展示力量，右图是蚂蚁展示力量。这两者之间的比例差异明显，通过比例定律可以解释为何蚂蚁在其尺度下能承载远超自身重量的物体，而人类在宏观尺度下不能。

---

## P16 

### Scaling laws

#### 物理量的比例

- **面积 (A) ∝ [L²]**
  - 表面力的比例如 [L²]
- **体积 (V) ∝ [L³]**
  - 体积力的比例如 [L³]

右侧图示说明了一个边长为L的立方体的面积和体积。将边长缩小为L/10，则新立方体的面积和体积分别缩小为原来的1/100和1/1000。

#### 各种力/物理量的比例定律可在文献中找到

- 结果取决于选择的尺寸不变量属性
  - 例如：势能 $E_p$ 与质量 ($m$)、重力加速度 ($g$)、高度 ($h$) 相关
  - 若 h 不变：$E_p$ = m · g · h ∝ [L³]
  - 若 h ∝ [L]：E_pot = m · g · h ∝ [L⁴]

--- 

## P17

### Some consequences of scaling laws for microfluidics

#### 毛细力在小尺度下变得非常重要

- **毛细力 F_capillary ∝ [L]**
  - 毛细力在微小尺度下起主要作用。图示中显示了液体在毛细管中的毛细上升现象，与重力相比，毛细力占主导地位。

#### 微流体系统中的流动通常是层流，因为在小长度尺度下，粘性力主导惯性力
- **雷诺数 (Re) = ρLv/η ∝ [L²] (v ∝ [L])**
  - 在小尺度下，粘性力（与流体的粘度相关）占主导地位，使得流动更趋向于层流而非湍流。

#### 扩散在小尺度下变得非常重要
- **佩克莱数 (Pe) = advective transport rate / diffusive transport rate = Lv/D ∝ [L²]**
  - 在小尺度下，扩散过程（物质分子随机运动导致的物质运输）变得非常重要。佩克莱数衡量了对流运输与扩散运输的相对重要性。

右侧图示显示了在微小管道中毛细力和重力的对比，强调了毛细力在微流体系统中的重要性。

---

# Examples

## P22

#### 通过管道的层流（Buckingham-Π定理）

1. **简介：**
   - 本部分讨论了确定层流管道流动中压降的参数。
   - 它区分了考虑压降（$ΔP$）和单位长度的压降（$Δp_l$）。

2. **物理变量：**
   - 涉及六个物理变量：
     1. **ΔP**：压差（帕 = 千克/米·秒²）
     2. **η**：动力粘度（帕·秒 = 千克/米·秒）
     3. **ρ**：密度（千克/米³）
     4. **L**：管道长度（米）
     5. **D**：管道直径（米）
     6. **v**：流动的平均速度（米/秒）

3. **独立的物理单位（MLT）：**
   - 问题涉及三个独立的物理单位：
     - **M**：质量（千克）
     - **L**：长度（米）
     - **T**：时间（秒）

4. **构建量纲矩阵 M：**
   - 构建量纲矩阵 \( M \) 将这些物理变量与其基本单位（M, L, T）联系起来：
     \[
     M = \begin{bmatrix}
     \text{ΔP} & \eta & \rho & L & D & v \\
     \text{kg} \cdot \text{m}^{-1} \cdot \text{s}^{-2} & \text{kg} \cdot \text{m}^{-1} \cdot \text{s}^{-1} & \text{kg} \cdot \text{m}^{-3} & \text{m} & \text{m} & \text{m} \cdot \text{s}^{-1}
     \end{bmatrix}
     \]

5. **量纲矩阵表示：**
   - 矩阵填充了每个变量维度的指数：
     \[
     M = \begin{bmatrix}
     1 & 1 & 1 & 0 & 0 & 0 \\
     -1 & -1 & -3 & 1 & 1 & 1 \\
     -2 & -1 & 0 & 0 & 0 & -1
     \end{bmatrix}
     \]

6. **求解量纲矩阵：**
   - 下一步是求解方程 \( M \cdot \mathbf{v} = 0 \) 以找到无量纲参数Πi。
   - 这些无量纲参数有助于简化物理变量之间的复杂关系。

7. **结果的解释：**
   - 得出的无量纲参数将以减少的影响参数描述系统。
   - 这一分析对于理解管道流动中的流体行为，特别是在确定压降时至关重要。

---
## P24

### 1. 如何建立量纲矩阵 \( M \)？

在这一页中，我们讨论了如何为管道中的层流压降问题建立量纲矩阵。

#### 物理变量：

考虑的物理变量有：
1. 压降 \( \Delta P \)（帕 = 千克/米·秒²）
2. 动力粘度 \( \eta \)（帕·秒 = 千克/米·秒）
3. 密度 \( \rho \)（千克/米³）
4. 管道长度 \( L \)（米）
5. 管道直径 \( D \)（米）
6. 流体的平均速度 \( v \)（米/秒）

#### 基本单位：

使用三个独立的基本单位：
- 质量 \( m \) [千克]
- 长度 \( l \) [米]
- 时间 \( t \) [秒]

### 2. 物理量在基本单位中的表示：

每个物理量可以用基本单位表示为：
- \( [\Delta P] = \text{Pa} = \text{kg}^1 \cdot \text{m}^{-1} \cdot \text{s}^{-2} \)
- \( [\eta] = \text{Pa} \cdot \text{s} = \text{kg}^1 \cdot \text{m}^{-1} \cdot \text{s}^{-1} \)
- \( [\rho] = \text{kg}^1 \cdot \text{m}^{-3} \)
- \( [L] = \text{m} \)
- \( [D] = \text{m} \)
- \( [v] = \text{m} \cdot \text{s}^{-1} \)

### 3. 插入量纲矩阵：

将这些量的基本单位指数填入量纲矩阵中：
\[
M = \begin{bmatrix}
\Delta P & \eta & \rho & L & D & v \\
\text{kg} & \text{kg} & \text{kg} & - & - & - \\
\text{m}^{-1} & \text{m}^{-1} & \text{m}^{-3} & \text{m} & \text{m} & \text{m} \\
\text{s}^{-2} & \text{s}^{-1} & - & - & - & \text{s}^{-1}
\end{bmatrix}
\]

用量纲指数填入矩阵：
\[
M = \begin{bmatrix}
1 & 1 & 1 & 0 & 0 & 0 \\
-1 & -1 & -3 & 1 & 1 & 1 \\
-2 & -1 & 0 & 0 & 0 & -1
\end{bmatrix}
\]

---

## P25

### 解决方程 \( M \cdot \vec{v} = 0 \)

这一页展示了如何解决管道层流中的无量纲参数问题，具体通过解量纲矩阵方程 \( M \cdot \vec{v} = 0 \) 来实现。

#### 1. 构建代数方程组

首先，我们列出之前构建的量纲矩阵 \( M \)：
\[ 
M = \begin{bmatrix}
1 & 1 & 1 & 0 & 0 & 0 \\
-1 & -1 & -3 & 1 & 1 & 1 \\
-2 & -1 & 0 & 0 & 0 & -1
\end{bmatrix}
\]

将矩阵方程表示为：
\[ 
M \cdot \vec{v} = \begin{bmatrix}
1 & 1 & 1 & 0 & 0 & 0 \\
-1 & -1 & -3 & 1 & 1 & 1 \\
-2 & -1 & 0 & 0 & 0 & -1
\end{bmatrix} \cdot \begin{bmatrix}
v_1 \\
v_2 \\
v_3 \\
v_4 \\
v_5 \\
v_6
\end{bmatrix} = \begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}
\]

#### 2. 代数方程的展开形式

展开矩阵方程得到一组代数方程：
\[ 
\begin{cases}
v_1 + v_2 + v_3 = 0 \\
-v_1 - v_2 - 3v_3 + v_4 + v_5 + v_6 = 0 \\
-2v_1 - v_2 - v_6 = 0
\end{cases}
\]

#### 3. 方程组的特点

- 通常，得到的代数方程系统是欠定的。
  - 这意味着变量的数量多于独立方程的数量，因此解不是唯一的。

#### 4. 无量纲参数的非唯一性

由于方程组是欠定的，无量纲参数可能不是唯一的。这意味着在不同情况下可能会有不同的无量纲参数组合来描述同一个物理现象。

---

## P26

#### 1. 方程组的建立

从之前的量纲矩阵 \( M \cdot \vec{v} = 0 \) 得到的代数方程组：
\[ 
\begin{cases}
v_1 + v_2 + v_3 = 0 \quad \text{(I)} \\
-v_1 - v_2 - 3v_3 + v_4 + v_5 + v_6 = 0 \quad \text{(II)} \\
-2v_1 - v_2 - v_6 = 0 \quad \text{(III)}
\end{cases}
\]

#### 2. 设定初始变量
设定 \( v_1 = a \), \( v_2 = b \), \( v_4 = c \) 作为自由变量。

#### 3. 解方程组

**结合方程 (I) 和 (III)：**

从方程 (I):
\[ v_1 + v_2 + v_3 = 0 \]
得到：
\[ v_3 = -a - b \]

从方程 (III):
\[ -2v_1 - v_2 - v_6 = 0 \]
得到：
\[ v_6 = -2a - b \]

**代入方程 (II) 进行计算：**

将 \( v_3 \) 和 \( v_6 \) 代入方程 (II):
\[ -a - b - 3(-a - b) + c + v_5 + (-2a - b) = 0 \]
化简得到：
\[ -a - b + 3a + 3b + c + v_5 - 2a - b = 0 \]
\[ a + b + c + v_5 = 0 \]
因此：
\[ v_5 = -b - c \]

#### 4. 通解

综合以上结果，得到变量的通解：
\[ 
\vec{v} = \begin{pmatrix}
a \\
b \\
-a - b \\
c \\
-b - c \\
-2a - b
\end{pmatrix}
\]

---

## P27

#### 1. 解决方案

上一页我们得到了方程组的通解：
\[ 
\vec{v} = \begin{pmatrix}
a \\
b \\
-a - b \\
c \\
-b - c \\
-2a - b
\end{pmatrix}
\]

#### 2. 特定解

我们可以选择特定的 \( a \)、\( b \)、\( c \) 值来得到特定的无量纲参数组合：

1. \( a = 1 \), \( b = 0 \), \( c = 0 \)
\[ 
\vec{v} = \begin{pmatrix}
1 \\
0 \\
-1 \\
0 \\
0 \\
-2
\end{pmatrix}
\]

2. \( a = 0 \), \( b = 1 \), \( c = 0 \)
\[ 
\vec{v} = \begin{pmatrix}
0 \\
1 \\
-1 \\
0 \\
-1 \\
-1
\end{pmatrix}
\]

3. \( a = 0 \), \( b = 0 \), \( c = 1 \)
\[ 
\vec{v} = \begin{pmatrix}
0 \\
0 \\
0 \\
1 \\
-1 \\
0
\end{pmatrix}
\]

#### 3. 无量纲参数的确定

使用上述特定解，我们可以确定无量纲参数：

\[ \Pi_i = (\Delta p, \eta, \rho, L, D, v) \cdot \vec{v}_i \]

根据特定解：
1. 对于第一个特定解 \( \vec{v}_1 = \begin{pmatrix} 1 \\ 0 \\ -1 \\ 0 \\ 0 \\ -2 \end{pmatrix} \):
\[ \Pi_1 = \frac{\Delta P}{\rho v^2} = \text{Euler数} \]

2. 对于第二个特定解 \( \vec{v}_2 = \begin{pmatrix} 0 \\ 1 \\ -1 \\ 0 \\ -1 \\ -1 \end{pmatrix} \):
\[ \Pi_2 = \frac{\eta}{\rho D v} = \frac{1}{\text{Reynolds数}} \]

3. 对于第三个特定解 \( \vec{v}_3 = \begin{pmatrix} 0 \\ 0 \\ 0 \\ 1 \\ -1 \\ 0 \end{pmatrix} \):
\[ \Pi_3 = \frac{L}{D} \]

---

## P28

#### 无量纲参数的总结

我们已经确定了三个主要的无量纲参数：

1. \(\Pi_1 = \frac{\Delta P}{\rho v^2} = \text{Eu}\) (Euler数)
2. \(\Pi_2 = \frac{\eta}{\rho D v} = \frac{1}{\text{Re}}\) (Reynolds数的倒数)
3. \(\Pi_3 = \frac{L}{D}\) (长度比)

#### 如何确定压降与这些无量纲参数的关系？

\[ \Delta P = f(\rho v^2, \text{Re}, \frac{L}{D}) \]

#### Hagen-Poiseuille流动

对于哈根-泊肃叶流动，压降可以表示为：
\[ \Delta P = \frac{8 \eta L}{\pi R^4} \cdot Q \]

通过无量纲化，可以得到：
\[ \frac{8 \eta L}{\pi R^4} \cdot Q = \frac{128}{\pi} \cdot \frac{\eta}{D^3} \cdot \frac{L}{D} \cdot \frac{\pi D^2}{4} \cdot v = 32 \cdot \frac{\eta}{D} \cdot \frac{L}{D} \cdot v \]

进一步简化：
\[ 32 \cdot \frac{\eta}{D \rho v} \cdot \rho v^2 \cdot \frac{L}{D} = 32 \cdot \frac{1}{\text{Re}} \cdot \rho v^2 \cdot \frac{L}{D} \]

最终得到：
\[ \Delta P = 64 \cdot \frac{L}{D} \cdot \frac{1}{\text{Re}} \cdot \frac{\rho v^2}{2} \]

---

## P29

### Laminar Flow Through a Pipe (Buckingham-Π) - Comparison between Buckingham-Π Approach and Nondimensionalization of NSE

### 比较Buckingham-Π方法和NSE的无量纲化

#### 1. 通过Buckingham-Π定理得到的无量纲参数

对于层流管道流动，Buckingham-Π定理给出的无量纲参数为：
- \(\text{Re}\)（Reynolds数）
- \(\text{Eu}\)（Euler数）

#### 2. 通过NSE无量纲化得到的无量纲参数

通过NSE的无量纲化，可以得到以下无量纲参数：
- \(\text{Re}\)（Reynolds数）
- \(\text{Eu}\)（Euler数）
- \(\text{Fr}\)（Froude数）

NSE无量纲化后的形式为：
\[ \frac{\partial \tilde{\vec{v}}}{\partial \tilde{t}} + \tilde{\vec{v}} \cdot \nabla \tilde{\vec{v}} = -\text{Eu} \nabla \tilde{p} + \frac{1}{\text{Re}} \nabla^2 \tilde{\vec{v}} + \frac{1}{\text{Fr}^2} \tilde{\vec{g}} \]

#### 3. 忽略重力作用力

在问题定义过程中，忽略了重力作用力：
- 当忽略重力作用力时，不能得到Froude数（\(\text{Fr}\)）。
- 长度比 \( \frac{L}{D} \) 是一个特定问题的无量纲参数，与几何形状有关。

### 结论

通过比较可以看出，Buckingham-Π方法和NSE无量纲化方法在确定无量纲参数上有所不同：
- Buckingham-Π方法没有考虑重力作用力，因此没有Froude数。
- NSE无量纲化方法则包括了Froude数，但在特定情况下（如忽略重力作用力时）Froude数不会出现。

---

## P30

### Discussion Solution

#### 1. 无量纲参数的数量

无量纲参数的数量取决于物理变量的数量：
- 如果考虑管道的粗糙度 \( \epsilon \)，我们会得到一个额外的参数：
  \[ \Pi_4 = \frac{\epsilon}{D} \]

#### 2. 压降的一般解

我们之前得到的解是管道压降问题的一种特殊情况。一般来说，管道中的压降可以表示为：
\[ \Delta P = f_{\text{friction}} \cdot \frac{L}{D} \cdot \frac{\rho v^2}{2} \]

##### 层流情况下：
\[ f_{\text{friction}} = \frac{64}{\text{Re}} \]

##### 湍流情况下：
我们使用Moody图来确定 \( f_{\text{friction}} \)。Moody图展示了不同Reynolds数和相对粗糙度下的摩擦因子。

#### 3. Moody图解释

右侧的图是Moody图，它展示了不同流态（层流、过渡流和湍流）下的摩擦因子随Reynolds数和相对粗糙度的变化关系。具体而言：
- 左侧区域代表层流，此时摩擦因子 \( f_{\text{friction}} = \frac{64}{\text{Re}} \)。
- 中间过渡区域逐渐从层流过渡到湍流。
- 右侧区域代表完全湍流，摩擦因子与相对粗糙度有关。

---

## P31

### Final Remarks on the Pipe Flow Example

#### 1. 三种不同压降解决方案的来源

**不同的建模方法：**
- 不同的假设
- 模型中包含的不同参数

#### 2. 具体说明

根据模型的不同，分析将产生不同的结果和无量纲参数：

- **第一个模型：**
  - 只考虑单位长度的压降 \(\Delta p_l\)。
  - 参数：密度 \(\rho\)、动力粘度 \(\eta\)、管道直径 \(D\)、平均速度 \(v\)。
  - 无量纲参数：例如，Reynolds数、Euler数等。

- **第二个模型：**
  - 考虑总压降 \(\Delta P\) 和管道长度 \(L\)。
  - 参数：密度 \(\rho\)、动力粘度 \(\eta\)、管道直径 \(D\)、平均速度 \(v\)、管道长度 \(L\)。
  - 无量纲参数：例如，\(\frac{L}{D}\) 比例。

- **第三个模型：**
  - 考虑总压降 \(\Delta P\) 和管道长度 \(L\)，以及管道粗糙度 \(\epsilon\)。
  - 参数：密度 \(\rho\)、动力粘度 \(\eta\)、管道直径 \(D\)、平均速度 \(v\)、管道长度 \(L\)、管道粗糙度 \(\epsilon\)。
  - 无量纲参数：例如，\(\frac{L}{D}\)、\(\frac{\epsilon}{D}\) 比例。

