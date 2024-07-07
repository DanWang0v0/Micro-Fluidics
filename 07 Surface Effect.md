## P4

### Surface tension: origin

#### 表面效应的起源

- **液体**内部的分子与其他分子形成非永久性的化学键（例如范德华力）。
- 表面的分子缺少朝向表面方向的其他分子的力（例如气体中的分子比液体中的少）。

液体表面表现得像被拉伸的**弹性膜**：

- 向内的力导致液体收缩。
- 切向力。

---

## P6

### Surface tension: shape

典型的形态是什么？

- 给定体积下最小的表面积是球体。
- 通过球形可以实现流体气体界面的能量最小化。
- 例如：球体对比立方体
  - 球体的表面积公式：\[A_{\text{Sphere}} = 4\pi R^2\]
  - 球体的体积公式：\[V_{\text{Sphere}} = \frac{4}{3}\pi R^3\]
  - 立方体的表面积公式：\[A_{\text{Cube}} = 6B^2\]
  - 立方体的体积公式：\[V_{\text{Cube}} = B^3\]
  - 当球体体积等于立方体体积时，\[V_{\text{Sphere}} = V_{\text{Cube}} \Rightarrow B = \left(\frac{4}{3}\pi R^3\right)^{\frac{1}{3}}\]
  - 立方体的表面积公式可简化为：\[A_{\text{Cube}} = 6 \left(\frac{4}{3}\pi\right)^{\frac{2}{3}} R^2 \approx 15.59 R^2 > 4\pi R^2 = 12.57 R^2\]
 
---

## P7

### Surface tension: Young-Laplace equation

如何描述复杂表面上的压力？

Young-Laplace方程：
\[ \Delta p_{\text{Laplace}} = \kappa \sigma \]

曲率（curvature）κ的示例：
- 圆形：\[ \kappa = \frac{1}{R} \]
- 平面：\[ \kappa = 0 \]
- 随机表面：\[ \kappa = \nabla \cdot \mathbf{n} \]（法向量的散度）

在这里：
- \(\Delta p_{\text{Laplace}}\) 表示由表面张力引起的压差
- \(\kappa\) 表示曲率
- \(\sigma\) 表示表面张力
- \(\mathbf{n}\) 表示法向量

---

## P10

### Contact angle: regimes

#### 系统（液体和固体）被称为：
- 亲水性（Hydrophilic）如果接触角 \(\theta < 90^\circ\)
- 疏水性（Hydrophobic）如果接触角 \(\theta > 90^\circ\)

#### 在微流体系统中需要考虑系统的润湿行为：

- \(\cos \theta = \frac{\sigma_{\text{SL}} - \sigma_{\text{GS}}}{\sigma_{\text{LG}}}\)
- 当 \(\theta = 0^\circ\) 时：\(\sigma_{\text{GS}} - \sigma_{\text{SL}} = \sigma_{\text{LG}}\)，表示完全润湿
- 当 \(\theta = 90^\circ\) 时：\(\sigma_{\text{GS}} = \sigma_{\text{SL}}\)
- 当 \(\theta = 180^\circ\) 时：\(\sigma_{\text{GS}} - \sigma_{\text{SL}} = -\sigma_{\text{LG}}\)，表示不润湿

在这些公式中：
- \(\sigma_{\text{SL}}\) 表示固-液界面的表面张力
- \(\sigma_{\text{GS}}\) 表示固-气界面的表面张力
- \(\sigma_{\text{LG}}\) 表示液-气界面的表面张力

---

## P11

### Contact angle: contact angle dynamics

#### 移除和添加液体到液滴：
- 观察
  - 当接触线移动时，接触角发生变化
  - 前进接触角（Advancing contact angle）和后退接触角（Receding contact angle）
- 接触角取决于
  - 静态情况下：运动方向 \(\theta_{\text{Adv}}\) 和 \(\theta_{\text{Rec}}\)
  - 动态情况下：运动速度 \(\theta_{\text{Dyn}}\)

截至目前：关于接触角动态还没有完整的理论。

---

## P12

毛细压力在微流体系统中的作用：接触角和表面张力的综合影响
Klatt & Hess - Microfluidics 1

在微流体系统中，计算压力时需要考虑表面张力和接触角。

例如：圆形通道中的毛细压力

- 参数
  - 半径 \(r\)
  - 接触角 \(\theta\)
  - 表面张力 \(\sigma\)

- 计算
  - Laplace压差：\[\Delta p_{\text{Laplace}} = \kappa \sigma = \frac{2\sigma}{r'}\]
  - 有效半径：\[r' = r \cos \theta\]
  - 圆形通道中的压力：\[\Delta p_{\text{Laplace}} = \frac{2\sigma \cos \theta}{r}\]

---

## P13

毛细压力在微流体系统中的作用：Concus-Finn猜想
Klatt & Hess - Microfluidics 1

如何计算更复杂的表面？

- 接口上的压力积分等于周界 \(P\) 处的表面张力力。
- 方程：\[
\iint_{A} p_{\text{Laplace}} \, dA = P \sigma \cos \theta \, dw
\]
- 结果：\[
\Delta p_{\text{Laplace}} = \sigma \sum_i \frac{\cos \theta_i}{w_i}
\]

例如：矩形通道中的毛细压力

- 参数
  - 宽度 \(w_1\) 和 \(w_2\)
  - 接触角 \(\theta\)
  - 表面张力 \(\sigma\)

- 矩形通道中的计算：\[
\Delta p_{\text{Laplace}} = 2\sigma \left( \frac{\cos \theta}{w_1} + \frac{\cos \theta}{w_2} \right)
\]