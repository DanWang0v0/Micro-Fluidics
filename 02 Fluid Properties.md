## P07

### 状态变量和材料属性

#### 状态变量/状态属性：
- 描述系统的状态（例如压力 \( P \)、体积 \( V \) 和温度 \( T \)）。
- 状态变量通过状态方程相关联： \( f(P, V, T) = 0 \)。

#### 材料/流体属性：
- 描述材料的属性（例如粘度、密度）。

#### 属性分类：

**广延属性（Extensive properties）：**
- 与存在的物质量成正比。
- 例如：质量、体积、能量等。

**强度属性（Intensive properties）：**
- 与存在的物质量无关。
- 例如：密度、粘度、压力等。

### 详细解释：

1. **状态变量/状态属性：**
   - 这些变量用于描述一个系统的当前状态。例如，压力 \( P \)、体积 \( V \) 和温度 \( T \) 是常见的状态变量。
   - 状态变量之间存在一定的关系，这种关系可以通过状态方程来表示，例如 \( f(P, V, T) = 0 \)。这个方程描述了系统在不同状态下这些变量之间的相互关系。

2. **材料/流体属性：**
   - 这些属性用于描述材料或流体的特性。例如，粘度描述了流体的流动阻力，密度描述了单位体积内的质量。

3. **属性分类：**
   - **广延属性（Extensive properties）：**
     - 这些属性与系统中物质的总量成正比。例如，质量是物质的总量，体积是物质占据的空间，能量是系统中包含的总能量。
   - **强度属性（Intensive properties）：**
     - 这些属性与系统中物质的总量无关。例如，密度是单位体积内的质量，粘度是流体的流动阻力，压力是单位面积上的力。

## P14

### 流体属性

**流体行为由流体属性决定：**
- 密度（Density）
- 粘度（Viscosity）
- 可压缩性（Compressibility）
- 表面效应（Surface effects）

**流体的任何属性都依赖于状态变量（P, V, T）：**
- 流体属性随状态变量变化的关系由材料定律描述。
- 依赖性较弱的属性可以视为常数。

### 详细解释：

1. **密度（Density）：**
   - 密度是单位体积内的质量。它是一个强度属性，与流体的总量无关。
   - 密度通常用 \( \rho \) 表示，单位为 \( \text{kg/m}^3 \)。

2. **粘度（Viscosity）：**
   - 粘度是流体内部阻力的度量，描述了流体流动时的内摩擦力。
   - 粘度可以分为动力粘度（dynamic viscosity）和运动粘度（kinematic viscosity），分别用 \( \mu \) 和 \( \nu \) 表示。

3. **可压缩性（Compressibility）：**
   - 可压缩性描述了流体在压力变化下体积变化的能力。
   - 理想气体的可压缩性可以通过状态方程 \( PV = nRT \) 来描述。

4. **表面效应（Surface effects）：**
   - 表面效应包括表面张力和界面现象，这些效应在微流体系统中尤为重要。
   - 表面张力是液体表面收缩的趋势，通常用 \( \gamma \) 表示，单位为 \( \text{N/m} \)。

5. **状态变量（P, V, T）：**
   - 压力（P）、体积（V）和温度（T）是描述流体状态的基本变量。
   - 流体的任何属性都依赖于这些状态变量。例如，密度可以随温度和压力变化而变化。

6. **材料定律：**
   - 材料定律描述了流体属性随状态变量变化的关系。例如，理想气体定律 \( PV = nRT \) 描述了气体的压力、体积和温度之间的关系。
   - 对于依赖性较弱的属性，可以将其视为常数，以简化分析和计算。

---

## P16

### 流体属性：粘度

**动力粘度（Dynamic viscosity） \( \eta \)**：
- 定义为剪切速率（shear rate）和剪切应力（shear stress）之间的比例因子，单位为帕斯卡·秒（Pa·s）。
- 公式：
  \[ \eta = \frac{dF/dA}{dv/dx} \]
  其中：
  - \( \eta \) 是动力粘度
  - \( dF \) 是微小的力
  - \( dA \) 是微小的面积
  - \( dv \) 是速度变化
  - \( dx \) 是位置变化

- 动力粘度是与流体“内摩擦”相关的强度属性，即流体流动的能力。
- 粘度越低，通过摩擦耗散的能量越少。

**运动粘度（Kinematic viscosity） \( \nu \)**：
- 定义为动力粘度和流体密度的比率，单位为平方毫米每秒（mm²/s）。
- 公式：
  \[ \nu = \frac{\eta}{\rho} \]
  其中：
  - \( \nu \) 是运动粘度
  - \( \eta \) 是动力粘度
  - \( \rho \) 是密度

### 详细解释：

1. **动力粘度（Dynamic viscosity） \( \eta \)**：
   - 动力粘度是描述流体内部阻力的度量。它表示流体在流动时内部层之间的摩擦力。
   - 动力粘度的单位是帕斯卡·秒（Pa·s），表示每单位面积上的力与速度梯度的比率。
   - 公式 \( \eta = \frac{dF/dA}{dv/dx} \) 表示剪切应力（单位面积上的力）与剪切速率（速度梯度）之间的关系。

2. **运动粘度（Kinematic viscosity） \( \nu \)**：
   - 运动粘度是动力粘度与流体密度的比率，表示流体在重力作用下流动的能力。
   - 运动粘度的单位是平方毫米每秒（mm²/s），表示流体在单位时间内流动的距离。
   - 公式 \( \nu = \frac{\eta}{\rho} \) 表示动力粘度与密度之间的关系。

3. **粘度的影响**：
   - 粘度越高，流体的流动阻力越大，流动越困难。例如，蜂蜜的粘度比水高得多，因此蜂蜜流动得更慢。
   - 粘度越低，流体的流动阻力越小，流动越容易。例如，水的粘度比橄榄油低，因此水流动得更快。

---

## P19

# 流体性质：可压缩性（compressibility）

## 定义
流体的**可压缩性**（compressibility）κ定义为**体积**（volume）相对于**压力**（pressure）的**相对变化**（relative change），单位为[1/Pa]。

公式表示为：
\[ \kappa = -\frac{1}{V} \left( \frac{\partial V}{\partial P} \right) \]

## 液体（Liquids）
液体几乎是**不可压缩的**（incompressible）。这意味着在施加压力时，液体的体积变化非常小。

## 气体（Gases）
气体是**可压缩的**（compressible）。这意味着在施加压力时，气体的体积会显著变化。

对于理想气体（ideal gas）的等温可压缩性（isothermal compressibility），根据**波义耳-马略特定律**（Boyle-Mariotte Law），公式为：
\[ pV = \text{const.} \]

因此，可压缩性κ可以表示为：
\[ \kappa = -\frac{1}{V} \left( \frac{\partial V}{\partial P} \right)_T = \frac{1}{p} \]

## 图示说明
- **液体**：在施加力（F）后，液体的体积变化很小。
- **气体**：在施加力（F）后，气体的体积显著减少。

---

## P20

# 蒸发（Evaporation）

## 流体在气相和液相之间的转变
- 所有液体都有**蒸发**（evaporate）成气相的趋势。
- 所有气体都有**凝结**（condense）回液相的趋势。

## 蒸气压（Vapour pressure）
- 在一个密闭容器中，蒸发和凝结之间会达到平衡。
  - 蒸气达到**饱和**（saturated），即 \( p_{\text{vessel}} = p_{\text{vap}} = p_{\text{sat}} \)。
  - 蒸气压是**温度依赖的**（temperature dependent）。
  - 液体的**沸点**（boiling point）定义为饱和蒸气压等于周围大气压的温度。

## 图示说明
- 左图：液体表面有分子逃逸到气相，表示蒸发过程。
- 右图：气相中的分子返回液体，表示凝结过程。

---

## P21

# 蒸发与沸腾的区别（Difference between evaporation and boiling）

## 蒸发（Evaporation）：表面现象（surface phenomenon）
- **蒸气压**（vapour pressure）小于等于**大气压**（atmospheric pressure），即 \( p_{\text{vap}} \leq p_{\text{atm}} \)。
  - 在液体内部无法形成气泡。
  - 没有沸腾，但在液体表面发生蒸发。

## 沸腾（Boiling）：体积现象（volume phenomenon）
- **蒸气压**（vapour pressure）大于等于**大气压**（atmospheric pressure），即 \( p_{\text{vap}} \geq p_{\text{atm}} \)。
  - 在液体内部形成气泡。
  - 液体的温度不能超过其沸点温度。

## 图示说明
- **蒸发**：液体表面有分子逃逸到气相，表示蒸发过程。
- **沸腾**：液体内部和表面都有气泡形成，表示沸腾过程。

---

## P22

# 流体性质：蒸气压（Vapour Pressure）

## 定义
蒸气压是指气体与其液相在平衡状态下的压力。

## 温度依赖性
蒸气压与温度呈指数关系。可以通过**安托万方程**（Antoine equation）来描述：
\[ \log_{10} P = A - \frac{B}{C + T} \]

### 备注
- A、B 和 C 是常数（与液体有关）。
- 在沸点以上，A、B 和 C 会发生变化。
- 结果以毫米汞柱（mmHg）为单位给出。

## 气体混合物
在气体混合物中，每种气体对总蒸气压贡献一个**分压**（partial pressure）。

## 图示说明
右侧的图表显示了水的蒸气压随温度变化的关系。可以看到，随着温度的升高，水的蒸气压显著增加。

---

## P23

# 统计物理（Statistical Physics）

## 定义
统计物理提供了一个多体系统宏观性质的描述，这些宏观性质是基于微观结构（原子描述）的。

## 假设（Assumptions）
1. **粒子数目**（Number of particles）很大（\( N \rightarrow \infty \)）。
2. 粒子的运动学由经典力学或量子力学控制。
3. **遍历假设**（Ergodic hypothesis）：
   - 粒子的运动是随机的。
   - 从微观集合中得出的平均值可以用来描述宏观性质。

## 图示说明
右侧的图示展示了粒子的随机运动，这些粒子的运动可以通过统计物理的方法来描述其宏观性质。

---

## P24

# 宏观视角与微观视角（Macroscopic and Microscopic View）

## 宏观视角（Macroscopic View，即热力学）
- **性质**（Properties）：可以直接测量的性质（例如温度）。
- 最常见的一组状态变量：
  - \( (P, T, N) \)：“等压-等温系综”（isobaric-isotherm ensemble）。

## 微观视角（Microscopic View，即原子描述）
- **力学定律**（Force laws）：例如**Lennard-Jones 势**（Lennard Jones potential）描述粒子之间的相互作用。
- 从力学定律出发，确定粒子的运动学，并计算统计状态密度。
- 宏观性质可以从微观状态密度的平均值中得出：
  \[ \langle E_{\text{kin}} \rangle = \int_{\text{all states}} E(x) dn(x) = \frac{3}{2} kT \equiv \frac{1}{2} mv_{\text{mean}}^2 \]
- 最常见的一组状态变量：
  - \( (E, V, N) \)：“微正则系综”（microcanonical ensemble）。

## 详细解释

### 宏观视角（Macroscopic View）
- **性质**：在宏观视角下，我们关注的是可以直接测量的物理量，例如温度、压力和体积。这些量是系统的整体表现。
- **状态变量**：最常见的一组状态变量是压力（P）、温度（T）和粒子数（N）。在等压-等温系综中，这些变量保持恒定。

### 微观视角（Microscopic View）
- **力学定律**：在微观视角下，我们关注的是粒子之间的相互作用。例如，Lennard-Jones 势描述了粒子之间的相互作用力。
- **粒子运动学**：通过力学定律，可以确定粒子的运动学行为，并计算出系统的统计状态密度。
- **宏观性质的推导**：宏观性质可以通过微观状态密度的平均值来推导。例如，系统的平均动能可以通过积分所有状态的能量密度来计算。
- **状态变量**：最常见的一组状态变量是能量（E）、体积（V）和粒子数（N）。在微正则系综中，这些变量保持恒定。

---

# Examples

## P29

### 1. 理想气体定律的推导（Derivation of the Ideal Gas Law）

#### 问题
如何将气体的**压力**（pressure）、**温度**（temperature）、**体积**（volume）和**气体量**（amount of gas）相互关联？

#### 参数（Parameters）
- 气体原子的数量 \( N \)（Number of gas atoms）
- 立方体的边长 \( L \)（Length of the cube）
- 原子的质量 \( m \) 和速度 \( v \)（Mass \( m \) and velocity \( v \) of the atom）

#### 假设（Assumptions）
1. 原子与容器壁之间的相互作用可以描述为**弹性碰撞**（elastic collisions）。
2. 原子之间没有相互作用。
   
#### 方法
我们考虑一个原子在 \( x \) 方向上在两个墙壁之间弹跳，并进行以下计算。

#### 计算步骤

##### 1. 原子撞击同一侧两次所需的时间
原子在 \( x \) 方向上撞击同一侧两次所需的时间为：
\[ \Delta t = \frac{2L}{v_x} \]

##### 2. 单个原子在墙壁上施加的平均力（在 \( x \) 方向上）是动量的变化
单个原子在墙壁上施加的平均力（在 \( x \) 方向上）是动量的变化：
\[ |F_{1,x}| = \left| \frac{\Delta p}{\Delta t} \right| = \left| \frac{\Delta p}{\frac{2L}{v_x}} \right| \]

##### 3. 动量的变化是碰撞前原子动量的两倍
动量的变化是碰撞前原子动量的两倍：
\[ |F_{1,x}| = \left| \frac{2p_x}{\frac{2L}{v_x}} \right| = \left| \frac{2mv_x}{\frac{2L}{v_x}} \right| = \frac{mv_x^2}{L} \]

##### 4. 原子在墙壁上施加的力
原子在墙壁上施加的力为：
\[ |F_{1,x}| = \left| \frac{mv_x^2}{L} \right| \]

##### 5. 墙壁上的压力（P）
墙壁上的压力为：
\[ |P_{1,x}| = \left| \frac{F_{1,x}}{A} \right| = \left| \frac{mv_x^2}{L^3} \right| \]

##### 6. 假设：没有优先的运动方向
假设原子的运动没有优先方向，即：
\[ v_x = v_y = v_z \]
\[ v^2 = v_x^2 + v_y^2 + v_z^2 = 3v_x^2 \]
\[ v_x^2 = \frac{1}{3}v^2 \]

##### 7. 用任意方向的速度表示压力
用任意方向的速度表示压力为：
\[ |P_1| = \left| \frac{mv^2}{3L^3} \right| \]

##### 8. 含有 \( N \) 个原子的理想气体的压力
对于含有 \( N \) 个原子的理想气体，压力为：
\[ P = \frac{N \cdot mv^2}{3L^3} = N \cdot \frac{mv^2}{V} \cdot \frac{1}{3} = N \cdot \frac{\left(\frac{1}{2}mv^2\right)}{V} \cdot \frac{2}{3} \]

##### 9. 动能的定义
根据原子的动能定义 \( E_{\text{kin}} = \frac{1}{2}mv^2 \)，可以得到：
\[ P = N \cdot \frac{E_{\text{kin}}}{V} \cdot \frac{2}{3} \]

##### 10. 总能量等于动能
由于原子之间没有相互作用，总能量等于动能：
\[ P = N \cdot \frac{E}{V} \cdot \frac{2}{3} \]

##### 11. 根据能量均分定理
根据能量均分定理，热能对应于：
\[ E = \frac{3}{2}kT \]

#### 公式总结
通过以上步骤，可以推导出理想气体定律的公式：
\[ P = \frac{N k T}{V} \]

---

## P36

### 2. 原子描述与连续性假设（Atomistic Description and the Continuity Assumption）

#### 计算步骤

##### 1. 水在一个1阿托升（1 attoliter = \(10^{-18}\) 升）的盒子中
- **密度**（Density）：\( \rho = 0.998 \frac{g}{ml} \)
- **摩尔质量**（Molar mass）：\( m_{\text{mol}} = 18g \)
- **摩尔体积**（Molar volume）：\( V_{\text{mol}} = 18.036 ml = 18.036 \times 10^9 \mu m^3 \)

##### 2. 计算盒子中的分子数 \( N \)
\[ N = \frac{N_a \cdot 10^{-3} \mu m^3}{V_{\text{mol}}} = \frac{6.022 \times 10^{23} \cdot 10^{-3} \mu m^3}{18.036 \times 10^9 \mu m^3} = 0.3339 \times 10^{11} = 33.39 \times 10^9 \]

#### 结论
- **连续性假设**（Continuum assumption）即使在非常小的长度尺度下也是有效的。
- 对于稀薄气体或通过纳米孔的传输（\( y \ll 0.1 \mu m \)），连续性假设不成立。

---

## P38

### 3. 温度控制的主动阀（Temperature Controlled Active Valve）

#### 问题描述（Problem Description）
- 需要什么温差才能在控制通道中产生足够的压力以关闭阀门？

#### 建模（Modelling）

###### 1. 如何建模几何结构？
- 需要确定阀门的几何形状，包括膜（membrane）、控制层（control layer，空气）和流体层（fluid layer）。

##### 2. 相关参数是什么？
- 初始气压 \( p_{G,0} = 1.013 \, \text{bar} \)
- 初始温度 \( T_{G,0} = 23^\circ \text{C} = 296 \, \text{K} \)
- 气体常数 \( R = 8.314 \, \frac{J}{\text{mol} \cdot \text{K}} \)
- 初始体积 \( V_{G,0} = 2.5 \times 10^{-4} \, \text{m}^3 \)
- 膜的压差 \( \Delta p_{\text{membrane}} = 250 \, \text{mbar} \)

##### 3. 假设哪些简化？
- 可以忽略由于膜变形引起的额外体积。

#### 数学描述（Mathematical Description）
- 使用**理想气体定律**（Ideal gas law）进行描述。

#### 求解步骤（Solving）

##### 1. 需要克服的压力差以关闭阀门
- 膜的压差 \( \Delta p_{\text{membrane}} = 250 \, \text{mbar} \)
- 最终气压 \( p_{G,1} = 1.263 \, \text{bar} \)

##### 2. 应用理想气体定律（常数 \( n \)）
理想气体定律为：
\[ pV = nRT \]

温度 \( T_1 \) 的计算公式为：
\[ T_1 = \frac{p_1 V_1}{nR} = \frac{p_1 V_1}{p_0 V_0} \cdot T_0 \]

##### 3. 假设可以忽略额外体积
\[ T_1 = \frac{126300 \, \text{Pa} \cdot 2.5 \times 10^{-4} \, \text{m}^3}{101300 \, \text{Pa} \cdot 2.5 \times 10^{-4} \, \text{m}^3} \cdot 296 \, \text{K} = 369 \, \text{K} = 95.85^\circ \text{C} \]

##### 4. 假设膜变形导致体积增加1%
假设膜变形导致体积增加1%，则温度 \( T_1^* \) 的计算公式为：
\[ T_1^* = \frac{126300 \, \text{Pa} \cdot 1.01 \cdot 2.5 \times 10^{-4} \, \text{m}^3}{101300 \, \text{Pa} \cdot 2.5 \times 10^{-4} \, \text{m}^3} \cdot 296 \, \text{K} = 98.85^\circ \text{C} \]

#### 图示说明
右侧的图示展示了阀门的结构：
- **膜**（Membrane）：位于控制层和流体层之间。
- **控制层**（Control layer，空气）：通过温度变化控制压力。
- **流体层**（Fluid layer）：流体流动的区域。

