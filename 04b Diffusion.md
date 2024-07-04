## P7

### 菲克定律：第一定律

#### 如何在宏观尺度上确定扩散通量？

==**菲克第一定律**==（Fick's first law）描述了粒子通量取决于浓度梯度：
\[
\colorbox{lightblue}{$\vec{J}_{\text{Diff}} = -D \nabla c$}
\]
- **\(\vec{J}_{\text{Diff}}\)**：扩散通量（Diffusion flux）
- **\(D\)**：扩散系数（Diffusion coefficient）
- **\(\nabla c\)**：浓度梯度（Concentration gradient）

#### 详细解释

##### 菲克第一定律
- **菲克第一定律**指出，扩散通量 \(\vec{J}_{\text{Diff}}\) 与浓度梯度 \(\nabla c\) 成正比，并且方向相反。
- **数学表达式**：\(\vec{J}_{\text{Diff}} = -D \nabla c\)
  - **\(-D\)**：负号表示扩散是从高浓度区域向低浓度区域进行的。
  - **\(D\)**：扩散系数，表示物质扩散的速率，单位为面积/时间（例如，\(\text{m}^2/\text{s}\)）。
  - **\(\nabla c\)**：浓度梯度，表示浓度随空间位置的变化率。

##### 图示解释
- **状态1（State 1）**：初始状态，有CO\(_2\)和O\(_2\)两种气体，分别在不同区域。
- **状态2（State 2）**：经过一段时间后，CO\(_2\)和O\(_2\)在界面处开始扩散。
- **扩散通量（Diffusion Flux）**：
  - \(\vec{J}_{\text{Diff, CO2}}\)：CO\(_2\)从高浓度区域（左侧）向低浓度区域（右侧）扩散。
  - \(\vec{J}_{\text{Diff, O2}}\)：O\(_2\)从高浓度区域（右侧）向低浓度区域（左侧）扩散。

#### 实际应用
菲克第一定律在许多科学和工程领域中都有广泛应用，包括：
- **化学工程**：描述反应器中物质的扩散。
- **生物学**：解释细胞膜上分子的扩散行为。
- **环境科学**：预测污染物在水体或大气中的扩散。

---

## P8

### 菲克定律：第二定律

#### 如何在宏观尺度上确定扩散流？

==**菲克第二定律**==（Fick's second law）描述了浓度随时间的演变：
\[
\colorbox{lightblue}{$\frac{\partial c}{\partial t} = -\nabla \cdot \vec{J}_{\text{Diff}} + S = D \Delta c + S$}
\]
- **\(\frac{\partial c}{\partial t}\)**：浓度的时间变化率（Temporal evolution of concentration）
- **\(\vec{J}_{\text{Diff}}\)**：扩散通量（Diffusion flux）
- **\(S\)**：源/汇项（Source/sink terms）
- **\(D\)**：扩散系数（Diffusion coefficient）
- **\(\Delta c\)**：浓度的拉普拉斯算子（Laplacian of concentration）

#### 详细解释

##### 菲克第二定律
- **菲克第二定律**提供了一个关于浓度随时间变化的偏微分方程，描述了扩散过程中浓度的动态变化。
- **数学表达式**：\(\frac{\partial c}{\partial t} = -\nabla \cdot \vec{J}_{\text{Diff}} + S = D \Delta c + S\)
  - **\(\frac{\partial c}{\partial t}\)**：浓度的时间变化率。
  - **\(-\nabla \cdot \vec{J}_{\text{Diff}}\)**：扩散通量的散度，表示通量的变化。
  - **\(S\)**：源/汇项，表示系统中生成或消耗的物质。
  - **\(D \Delta c\)**：扩散系数乘以浓度的拉普拉斯算子，描述浓度的空间变化对时间变化的影响。

##### 对比其他方程
- **热扩散方程（Heat diffusion equation）**：
  \[
  \rho c \frac{\partial T}{\partial t} = -\nabla \cdot \vec{J}_{\text{Cond}} + S = \lambda \Delta T + S
  \]
  - **\(\frac{\partial T}{\partial t}\)**：温度的时间变化率。
  - **\(\vec{J}_{\text{Cond}}\)**：导热通量（Heat conduction flux）。
  - **\(\lambda \Delta T\)**：热导率乘以温度的拉普拉斯算子。
- **纳维-斯托克斯方程（Navier-Stokes equations）**：
  \[
  \frac{\partial}{\partial t} (\rho \vec{v}) + \vec{v} \cdot \nabla (\rho \vec{v}) = -\nabla p + \eta \Delta \vec{v} + f_{\text{volume}}
  \]
  - **\(\frac{\partial}{\partial t} (\rho \vec{v})\)**：动量的时间变化率。
  - **\(\vec{v} \cdot \nabla (\rho \vec{v})\)**：动量的对流项（Convective term）。
  - **\(-\nabla p\)**：压力梯度项。
  - **\(\eta \Delta \vec{v}\)**：粘性扩散项（Viscous diffusion term）。
  - **\(f_{\text{volume}}\)**：体积力项（Body force term）。

---

# Example

## P12

### 氢扩散建模

#### 墙壁氢损失量是多少？

##### 假设
- **稳态条件**：系统在稳态下运行，所有变量随时间不变。
- **墙内外浓度恒定**：墙的内部和外部的氢浓度保持不变。
- **y 和 z 方向无扩散传输**：氢扩散仅在 x 方向进行，忽略 y 和 z 方向的扩散。
- **墙中无物种生成**：墙中没有氢的生成或消耗。

##### 参数
- **墙的宽度** \( w \)
- **墙的高度和长度** \( h \) 和 \( l \)
- **墙中氢的扩散系数** \( D \)
- **罐内氢浓度** \( c_{\text{in}} \) 和环境中氢浓度 \( c_{\text{out}} \)
- **通过墙的体积流量** \( Q_{\text{out}} \)

#### 详细解释

##### 基本方程
根据菲克定律，稳态条件下氢通过墙的扩散流量可以表示为：
\[
J_{\text{Diff}} = -D \frac{d c}{d x}
\]
其中：
- \( J_{\text{Diff}} \) 是扩散通量。
- \( D \) 是扩散系数。
- \( \frac{d c}{d x} \) 是浓度梯度。

##### 氢的流量
氢的流量可以通过扩散通量乘以墙的面积得到：
\[
Q_{\text{out}} = J_{\text{Diff}} \cdot A = -D \frac{c_{\text{in}} - c_{\text{out}}}{w} \cdot (h \cdot l)
\]
其中：
- \( A = h \cdot l \) 是墙的面积。

##### 求解步骤
1. **确定浓度梯度**：
   - 墙内外氢浓度差：\( \Delta c = c_{\text{in}} - c_{\text{out}} \)
   - 浓度梯度：\( \frac{d c}{d x} = \frac{c_{\text{in}} - c_{\text{out}}}{w} \)

2. **计算扩散通量**：
   - \( J_{\text{Diff}} = -D \frac{\Delta c}{w} \)

3. **计算氢流量**：
   - 墙的面积：\( A = h \cdot l \)
   - 体积流量：\( Q_{\text{out}} = J_{\text{Diff}} \cdot A \)

#### 总结
通过以上假设和参数，可以使用菲克定律计算氢通过墙的损失量。这个模型假设稳态条件和简单的扩散过程，是分析氢气泄漏和储存的基础。