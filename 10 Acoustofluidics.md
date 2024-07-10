## P20

### 扰动理论

#### 对速度和密度做同样的处理
    - 密度场：\(\rho(\vec{r}, t) = \rho_0 + \tilde{\rho}_1(\vec{r}, t)\)
    - 压力场：\(p(\vec{r}, t) = p_0 + \tilde{p}_1(\vec{r}, t)\)
    - 速度场：\(\vec{v}(\vec{r}, t) = \vec{v}_0 + \tilde{\vec{v}}_1(\vec{r}, t) = \vec{0} + \tilde{\vec{v}}_1(\vec{r}, t)\)

#### 将这些表达式代入以下方程
    - \[\frac{\partial}{\partial t} (\rho_0 + \tilde{\rho}_1) + \nabla \cdot ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) = 0\]
    - \[\frac{\partial}{\partial t} ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) + \tilde{\vec{v}}_1 \cdot \nabla ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) = -\nabla(p_0 + \tilde{p}_1) + \nabla \cdot (\eta \nabla \tilde{\vec{v}}_1)\]

#### 简化这些方程，使用以下规则
    - 假设一阶场的乘积为零。
    - 一阶场是时谐的，满足 \(\frac{\partial}{\partial t}\tilde{\rho}_1(\vec{r}, t) = -i\omega \tilde{\rho}_1(\vec{r}, t)\)。

---

## P21

### 连续性方程

#### 原方程
    - \[\frac{\partial}{\partial t} (\rho_0 + \tilde{\rho}_1) + \nabla \cdot ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) = 0\]

#### 代入 \(\vec{v}_0 = 0\)，并且 \(\rho_0\) 是常数：
    - \[\frac{\partial}{\partial t} \tilde{\rho}_1 + \nabla \cdot (\rho_0 \tilde{\vec{v}}_1) = 0\]

#### 使用时谐假设：
    - \[-i\omega \rho_1 = -\nabla \cdot (\rho_0 \tilde{\vec{v}}_1)\]
    - \[-i\omega \rho_1 = -\rho_0 \nabla \cdot \tilde{\vec{v}}_1\]

在这里，连续性方程可以这样化简的原因是基于以下几点：
1. **小扰动假设**：假设扰动较小，忽略一阶以上的项，这样使得方程线性化。
2. **时谐场**：假设扰动是时谐的，即具有特定的频率 \(\omega\)，使得时间导数可以转换为乘以 \(-i\omega\)。
3. **初始场的特性**：假设背景场（例如密度 \(\rho_0\) 和速度 \(\vec{v}_0\)）是常数或零，从而简化了方程。

### 纳维-斯托克斯方程

1. 原方程：
    - \[\frac{\partial}{\partial t} ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) + \tilde{\vec{v}}_1 \cdot \nabla ((\rho_0 + \tilde{\rho}_1)\tilde{\vec{v}}_1) = -\nabla(p_0 + \tilde{p}_1) + \nabla \cdot (\eta \nabla \tilde{\vec{v}}_1)\]

2. 代入简化后：
    - \[-i\omega \rho_0 \tilde{\vec{v}}_1 = -c_0^2 \nabla \rho_1 + \eta_0 \nabla^2 \tilde{\vec{v}}_1 + \beta \eta_0 \nabla (\nabla \cdot \tilde{\vec{v}}_1)\]

为了详细解释纳维-斯托克斯方程（NSE）的化简步骤，我们需要逐步代入扰动理论假设，并进行必要的数学操作。下面是详细的化简步骤：

### 原始的纳维-斯托克斯方程

原始的纳维-斯托克斯方程是：
\[ \frac{\partial}{\partial t} (\rho \vec{v}) + \nabla \cdot (\rho \vec{v} \vec{v}) = -\nabla p + \nabla \cdot (\eta \nabla \vec{v}) \]

在扰动理论中，我们假设密度、压力和速度场都有小扰动：

- 密度场：\(\rho(\vec{r}, t) = \rho_0 + \tilde{\rho}_1(\vec{r}, t)\)
- 压力场：\(p(\vec{r}, t) = p_0 + \tilde{p}_1(\vec{r}, t)\)
- 速度场：\(\vec{v}(\vec{r}, t) = \vec{v}_0 + \tilde{\vec{v}}_1(\vec{r}, t) = \vec{0} + \tilde{\vec{v}}_1(\vec{r}, t)\)

将这些表达式代入原始的纳维-斯托克斯方程：

\[ \frac{\partial}{\partial t} ((\rho_0 + \tilde{\rho}_1) \tilde{\vec{v}}_1) + \nabla \cdot ((\rho_0 + \tilde{\rho}_1) \tilde{\vec{v}}_1 \tilde{\vec{v}}_1) = -\nabla (p_0 + \tilde{p}_1) + \nabla \cdot (\eta \nabla \tilde{\vec{v}}_1) \]

### 化简步骤

1. **忽略高阶小项：**

   根据扰动理论的假设，忽略一阶以上的扰动项，因此：
   \[ \nabla \cdot ((\rho_0 + \tilde{\rho}_1) \tilde{\vec{v}}_1 \tilde{\vec{v}}_1) \approx \rho_0 \nabla \cdot (\tilde{\vec{v}}_1 \tilde{\vec{v}}_1) \]

2. **时谐场假设：**

   设一阶场是时谐的，即：
   \[ \frac{\partial \tilde{\vec{v}}_1}{\partial t} = -i\omega \tilde{\vec{v}}_1 \]
   因此：
   \[ \frac{\partial}{\partial t} (\rho_0 \tilde{\vec{v}}_1) = -i\omega \rho_0 \tilde{\vec{v}}_1 \]

3. **简化压力项和粘性项：**

   假设初始压力 \( p_0 \) 是常数，其梯度为零，只剩下扰动项的梯度：
   \[ \nabla p = \nabla (p_0 + \tilde{p}_1) = \nabla \tilde{p}_1 \]

   对于粘性项，由于初始速度场 \( \vec{v}_0 = 0 \)：
   \[ \nabla \cdot (\eta \nabla \vec{v}) = \nabla \cdot (\eta \nabla \tilde{\vec{v}}_1) \]

### 代入简化后的表达式

代入这些简化后的表达式，得到：

\[ -i\omega \rho_0 \tilde{\vec{v}}_1 + \rho_0 \tilde{\vec{v}}_1 \cdot \nabla \tilde{\vec{v}}_1 = -\nabla \tilde{\rho}_1 - \nabla \tilde{p}_1 + \nabla \cdot (\eta \nabla \tilde{\vec{v}}_1) \]

### 应用连续性方程

从简化后的连续性方程中：

\[ -i\omega \tilde{\rho}_1 = -\rho_0 \nabla \cdot \tilde{\vec{v}}_1 \]
所以：
\[ \tilde{\rho}_1 = \frac{\rho_0}{\omega} \nabla \cdot \tilde{\vec{v}}_1 \]

### 用声速关系代替压力项

假设扰动压力与扰动密度之间的关系为：
\[ \tilde{p}_1 = c_0^2 \tilde{\rho}_1 \]

其中 \( c_0 \) 为声速。代入上式：
\[ \tilde{p}_1 = c_0^2 \frac{\rho_0}{\omega} \nabla \cdot \tilde{\vec{v}}_1 \]

### 最终化简

将所有这些代入简化的纳维-斯托克斯方程，得到：

\[ -i\omega \rho_0 \tilde{\vec{v}}_1 = -c_0^2 \nabla \left(\frac{\rho_0}{\omega} \nabla \cdot \tilde{\vec{v}}_1 \right) + \eta_0 \nabla^2 \tilde{\vec{v}}_1 + \beta \eta_0 \nabla (\nabla \cdot \tilde{\vec{v}}_1) \]

这一步中，使用了声速关系和粘性项的简化。最终结果是：

\[ -i\omega \rho_0 \tilde{\vec{v}}_1 = -c_0^2 \nabla \tilde{\rho}_1 + \eta_0 \nabla^2 \tilde{\vec{v}}_1 + \beta \eta_0 \nabla (\nabla \cdot \tilde{\vec{v}}_1) \]

其中 \(\tilde{\rho}_1 = \frac{\rho_0}{\omega} \nabla \cdot \tilde{\vec{v}}_1\)。

这就是纳维-斯托克斯方程在扰动理论下的详细化简过程。通过这些步骤，可以得到适用于小扰动和线性分析的简化方程。

在流体力学中，\(\beta\) 通常用来表示流体的体积粘性系数或二阶粘性系数。具体来说，它与动量扩散有关，用来描述流体在体积变化（膨胀或压缩）过程中对粘性力的响应。

在一些流体力学模型中，动量扩散（粘性效应）不仅与剪切应变相关，还与体积应变（体积变化率）相关。为了描述这些效应，可以引入体积粘性系数 \(\beta\)。它表示的是流体在体积变化时的粘性阻力。

### 纳维-斯托克斯方程中的 \(\beta\)

在纳维-斯托克斯方程的扰动理论化简过程中，粘性项可以写成：

\[ \eta_0 \nabla^2 \tilde{\vec{v}}_1 + \beta \eta_0 \nabla (\nabla \cdot \tilde{\vec{v}}_1) \]

其中：

- \(\eta_0\) 是剪切粘性系数（或第一粘性系数），它与流体的剪切应变速率相关。
- \(\beta \eta_0\) 是体积粘性系数乘以 \(\eta_0\)，它与流体的体积变化率（膨胀或压缩）相关。

因此，\(\beta\) 在这种情况下，是一个无量纲系数，用来调整体积粘性相对于剪切粘性的比例。

### 体积粘性系数的作用

当流体发生体积变化（例如通过压缩波或膨胀波）时，体积粘性系数会影响流体的阻力。如果 \(\beta\) 较大，流体对体积变化的阻力也较大，表现为更显著的粘性效应。

### 具体化简

在我们的纳维-斯托克斯方程化简过程中，如果考虑到体积粘性系数，那么完整的粘性项会包含：

\[ \eta_0 \nabla^2 \tilde{\vec{v}}_1 + \beta \eta_0 \nabla (\nabla \cdot \tilde{\vec{v}}_1) \]

这个项中的 \(\beta\) 乘以 \(\eta_0\) 就是体积粘性系数。这个项描述的是流体在体积变化过程中由于粘性产生的额外应力。

### 总结

\(\beta\) 是一个无量纲系数，用来表示体积粘性相对于剪切粘性的比例。在纳维-斯托克斯方程的扰动理论化简中，它影响的是与流体体积变化相关的粘性力。