# 机器学习概述

## 监督学习
监督学习（Supervised Learning）是机器学习的一种主要范式，其基本任务是从有标签的训练数据中学习出一个模型，然后用该模型对新的数据进行预测或分类。

在监督学习中，训练数据由输入和对应的期望输出（标签）组成。学习过程就是通过训练数据来学习输入和输出之间的映射关系，最终得到一个能够对未知数据进行预测的模型。这个预测可以是连续的（回归任务），也可以是离散的类别标签（分类任务）。

主要的监督学习算法包括但不限于：

1. **线性回归（Linear Regression）**：用于预测连续数值的算法，通过拟合一条直线或超平面来建模数据之间的线性关系。

2. **逻辑回归（Logistic Regression）**：用于二分类问题的算法，通过sigmoid函数将线性回归的结果映射到概率空间。

3. **决策树（Decision Trees）**：通过树状结构进行分类和回归的算法，根据特征的条件将数据集分割成不同的子集。

4. **支持向量机（Support Vector Machines，SVM）**：用于分类和回归的算法，通过构建超平面在特征空间中分割不同类别的数据点。

5. **神经网络（Neural Networks）**：一类复杂的模型，通过多层神经元网络进行学习和预测，适用于各种复杂的非线性问题。

在监督学习中，关键的步骤包括数据的预处理、选择合适的模型和算法、训练模型并进行评估。监督学习的目标是建立一个能够泛化到新数据的模型，使其在面对未标记的数据时也能做出准确的预测或分类。

## 无监督学习

无监督学习（Unsupervised Learning）是机器学习中的一种范式，与监督学习相对。在无监督学习中，模型通过分析没有标签的输入数据来发现数据中的模式、结构或特征。

无监督学习的主要任务包括：

1. **聚类（Clustering）**：将数据集中的样本划分为若干个类别或簇，使得同一类别内的样本相似度较高，不同类别之间的相似度较低。

2. **降维（Dimensionality Reduction）**：将高维数据转换为低维表示，同时保留数据的重要特征，以便于可视化、数据压缩或更高效的处理。

3. **关联规则学习（Association Rule Learning）**：发现数据集中项之间的关联关系，例如购物篮分析中的“如果购买A，那么可能会购买B”的规则。

无监督学习与监督学习的主要区别在于，无监督学习中的训练数据没有预先定义的目标输出。模型需要自行发现数据的内在结构或模式，而不是根据标签进行学习和预测。

常见的无监督学习算法包括但不限于：

- **K均值聚类（K-means Clustering）**：将数据集中的样本划分为K个簇，以最小化各样本与其所属簇中心的距离平方和。

- **层次聚类（Hierarchical Clustering）**：通过不断合并或分割簇来构建树状的聚类结构，以便可视化和分析。

- **主成分分析（Principal Component Analysis，PCA）**：通过线性变换将数据投影到低维空间，保留尽可能多的原始数据方差，以实现数据降维和特征提取。

- **生成对抗网络（Generative Adversarial Networks，GANs）**：通过生成器和判别器之间的对抗训练来学习生成新数据样本，无监督地学习数据分布。

无监督学习在处理没有明确标签或类别的数据集时尤为有用，可以帮助揭示数据中的隐藏结构和关系，从而为进一步的数据分析和决策提供洞察力。

## 强化学习

强化学习（Reinforcement Learning）是机器学习的一个分支，其主要目标是让智能体（agent）通过与环境的交互学习如何在特定的环境中采取行动，以使累积的奖励最大化。

在强化学习中，智能体通过试错的方式学习，不需要事先标记的数据集。其基本思想类似于人类学习的过程：通过尝试不同的行动来探索环境，根据行动的结果（奖励或惩罚）调整策略，以便在未来的决策中获得更好的结果。

强化学习的核心概念包括：

1. **智能体（Agent）**：学习和决策的实体，它感知环境的状态并选择行动以最大化长期奖励。

2. **环境（Environment）**：智能体所处的外部环境，它根据智能体的行动给予奖励或惩罚，并更新状态。

3. **状态（State）**：描述环境的特定瞬时情况，对智能体来说是观察到的信息。

4. **行动（Action）**：智能体基于当前状态所选择的决策或动作。

5. **奖励（Reward）**：行动后环境给予的反馈，用来评估行动的好坏，目标是最大化累积奖励。

强化学习的经典算法包括：

- **Q学习（Q-Learning）**：基于动态规划的无模型强化学习算法，通过更新行动值函数Q来学习最优策略。

- **深度Q网络（Deep Q-Networks，DQN）**：结合深度神经网络和Q学习，用于处理状态空间复杂的问题。

- **策略梯度方法（Policy Gradient Methods）**：直接优化策略参数，使得智能体能够直接在策略空间中寻找最优策略。

强化学习在许多领域有广泛的应用，如机器人控制、游戏策略优化、自动驾驶汽车、资源管理等。它的核心挑战包括探索与利用的平衡（exploration-exploitation trade-off）、长期回报最大化等问题，需要灵活的算法和策略来应对复杂的环境和任务。


---
<br>
<br>

---

## Introduction
## supervised learning 监督学习
监督学习模型定义了从一个或多个输入到一个或多个输出的映射关系。例如，输入可以是一辆二手 Toyota Prius 的年龄和里程，输出可以是车辆估算的美元价值。

模型本质上是一个数学方程；当输入通过这个方程时，它计算出输出，这个过程被称为推断。模型方程中还包含参数。不同的参数值会改变计算的结果；模型方程描述了输入和输出之间可能的关系族群，而参数则指定了具体的关系形式。

当我们训练或学习一个模型时，我们寻找能够描述输入和输出真实关系的参数。学习算法会使用一组输入/输出对的训练集，并调整参数，直到输入能够尽可能准确地预测其对应的输出。如果模型在这些训练对上表现良好，我们希望它在新的输入上（真实输出未知的情况下）也能做出良好的预测。

本章的目标是扩展这些概念。首先，我们更加正式地描述这个框架，并引入一些符号表示法。然后，我们通过一个简单的例子来演示，使用一条直线来描述输入和输出之间的关系。这个线性模型不仅熟悉而且易于可视化，但它也展示了监督学习的所有主要思想。
### 损失函数 loss function
一般使用均方差表示，这与最小二乘法有异曲同工之妙。

除了均方误差（Mean Squared Error，MSE），还有一些其他常用的损失函数，具体取决于所面对的问题和模型的性质。以下是一些常见的替代损失函数：

1. **平均绝对误差（Mean Absolute Error，MAE）**：
   平均绝对误差是预测值与真实值之间差异的绝对值的平均值，定义如下：
   $$ L(\phi) = \frac{1}{I} \sum_{i=1}^{I} |\hat{y}_i - y_i| $$
   <!-- $$ L(\phi) = \frac 1 I \sum _{i=1} ^ I  $$ -->
   
   MAE 对异常值不敏感，因为它使用的是绝对误差而不是平方误差。

2. **Huber损失**：
   Huber损失结合了均方误差和平均绝对误差的优点，对异常值具有一定的鲁棒性。它在误差较小的情况下使用均方误差，而在误差较大时转换为平均绝对误差，定义如下：

   $$ L_\delta(\phi) = \frac{1}{I} \sum_{i=1}^{I} \begin{cases} 
   \frac{1}{2} (\hat{y}_i - y_i)^2 & \text{if } |\hat{y}_i - y_i| \leq \delta \\\delta |\hat{y}_i - y_i| - \frac{1}{2} \delta^2 & \text{otherwise}\end{cases} $$

   其中，$\delta$  是一个阈值参数，通常是一个小正数，用于控制转换点。

3. **对数损失（Logarithmic Loss）**：
   适用于分类问题，对数损失（也称为逻辑损失或交叉熵损失）用于评估分类模型输出的概率分布与真实标签之间的差异。对于二分类问题，定义如下：
   $$ L(\phi) = -\frac{1}{I} \sum_{i=1}^{I} 
   \left[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \right] $$
   其中，$ \hat{y}_i $ 是模型对第 $ i $ 个样本的预测概率，$ y_i $ 是真实标签（0或1）。

4. **Hinge损失**：
   用于支持向量机（SVM）等分类模型，Hinge损失评估了预测标签与真实标签之间的边界超平面的间隔。对于二分类问题，定义如下：

   $$ L(\phi) = \frac{1}{I} \sum_{i=1}^{I} \max(0, 1 - y_i \cdot \hat{y}_i) $$

   其中, $\hat{y}_i$ 是模型对第 $i$ 个样本的预测标签（通常是一个分数）, $y_i$ 是真实标签（通常是1或-1）。

这些损失函数适用于不同类型的机器学习任务和模型，并且根据问题的特性和数据的分布进行选择。
### 模型训练 model training
找到能够最小化损失的参数的过程被称为模型拟合、训练或学习。基本方法是随机选择初始参数，然后通过“下降”损失函数来改进它们，直到达到最低点（见图2.4）。一种做法是在当前位置测量表面的梯度，并朝最陡峭的下坡方向迈出一步。然后重复这个过程，直到梯度变平且无法进一步改进为止。

### 比较 comparison
#### lost functions and  cost functions 损失函数和代价函数
损失函数与代价函数：在许多机器学习领域以及本书中，损失函数和代价函数这两个术语通常可以互换使用。然而，更准确地说，损失函数是与每个数据点相关联的个别项（即方程式2.5右侧的每个平方项），而代价函数则是要最小化的整体量（即方程式2.5的整个右侧）。代价函数可能包含与个别数据点无关的额外项（请参见第9.1节）。更一般地说，目标函数是任何需要最大化或最小化的函数。

损失函数（Loss Function）和代价函数（Cost Function）在机器学习和优化问题中有一些微妙的区别，尽管它们通常可以互换使用，但有时会根据上下文来区分它们的具体含义。

1. **损失函数（Loss Function）**：
   - 损失函数通常是针对单个样本或单个数据点定义的。它衡量了在给定模型参数下，模型预测值与实际观测值之间的差异或误差。
   - 例如，在线性回归中，平方损失函数 \( L(\hat{y}, y) = (\hat{y} - y)^2 \) 是一个常见的损失函数，其中 \( \hat{y} \) 是模型的预测值，\( y \) 是实际观测值。

2. **代价函数（Cost Function）**：
   - 代价函数是指整个训练集上的损失函数的平均值或总和。它是在训练模型时要最小化的目标函数。
   - 在机器学习中，通常使用代价函数来评估模型的性能和指导参数优化的过程。代价函数考虑了整个训练集上所有损失函数的贡献。
   - 例如，对于线性回归，代价函数可以定义为平均平方误差（MSE）：\[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} (\hat{y}^{(i)} - y^{(i)})^2 \] 其中 \( m \) 是训练集中的样本数量，\( \hat{y}^{(i)} \) 是模型对第 \( i \) 个样本的预测值，\( y^{(i)} \) 是实际第 \( i \) 个样本的观测值。

3. **区别总结**：
   - 损失函数是针对单个数据点定义的，用于衡量单个预测值的误差。
   - 代价函数是整个训练集上的损失函数的总体度量，用于衡量整个模型的性能。
   - 代价函数可以包含额外的惩罚项或正则化项，这些项不一定与单个数据点的损失直接相关。

在实践中，这两个术语有时会被交换使用，但理解它们之间的微妙区别可以帮助更清晰地思考和描述模型的训练和优化过程。

#### Generative vs. discriminative models 生成模型和判别模型
字面意思

本章中的模型 y = f[x, ϕ] 是判别模型。这些模型根据真实世界的测量值 x 进行输出预测 y。另一种方法是构建生成模型 x = g[y, ϕ]，其中真实世界的测量值 x 是输出 y 的函数。

生成方法的缺点在于它不直接预测 y。为了进行推断，我们必须**反转生成方程**，即 y = g^(-1)[x, ϕ]，这可能很困难。然而，生成模型的优点在于我们可以融入关于数据生成方式的先验知识。例如，如果我们想预测图像中汽车的三维位置和方向 y，则可以将关于汽车形状、三维几何和光传输的知识融入函数 x = g[y, ϕ] 中。

这似乎是一个不错的想法，但事实上，判别模型在现代机器学习中占据主导地位；利用生成模型中的先验知识所带来的优势通常被学习非常灵活、具有大量训练数据的判别模型所超越。

生成模型（Generative models）和判别模型（Discriminative models）是机器学习中两种不同类型的建模方法，它们的主要区别在于它们如何学习和利用数据。

1. **生成模型**：
   - 生成模型的目标是学习数据的生成过程，即学习数据的联合概率分布 \( P(X, Y) \)，其中 \( X \) 是输入（特征），\( Y \) 是输出（标签）。
   - 生成模型能够生成新的数据，因为它们对数据的整体分布进行建模。通过学习数据的分布，生成模型可以从中采样生成类似的新数据点。
   - 典型的生成模型包括朴素贝叶斯分类器、隐马尔可夫模型（HMM）、生成对抗网络（GAN）等。

2. **判别模型**：
   - 判别模型的目标是学习并预测类别标签 \( Y \) 与输入 \( X \) 之间的条件概率分布 \( P(Y \mid X) \)。
   - 判别模型关注的是对给定输入 \( X \) 直接进行分类或回归预测，而不是关心输入的
  


## shallow neural network 浅层神经网络


本章介绍了浅层神经网络。这些网络描述了分段线性函数，并且具有足够的表达能力来逼近多维输入和输出之间任意复杂的关系。

浅层神经网络是具有参数 ϕ 的函数 y = f[x, ϕ]，将多变量输入 x 映射到多变量输出 y。我们将完整的定义推迟到第3.4节，并通过一个示例网络 f[x, ϕ] 来介绍主要思想，该网络将标量输入 x 映射到标量输出 y，并具有十个参数 ϕ = {ϕ0, ϕ1, ϕ2, ϕ3, θ10, θ11, θ20, θ21, θ30, θ31}：

\[ y = f[x, ϕ]  = ϕ0 + ϕ1 \cdot a[\theta_{10} + θ_{11}x] + ϕ2 \cdot a[\theta_{20} + θ_{21}x] + ϕ3 \cdot a[\theta_{30} + θ_{31}x]. \quad (3.1) \]

我们可以将这个计算分解为三个部分：首先，计算输入数据的三个线性函数（θ10 + θ11x, θ20 + θ21x 和 θ30 + θ31x）。其次，通过激活函数 a[•] 处理这三个结果。最后，用 ϕ1、ϕ2 和 ϕ3 加权这三个生成的激活值，将它们相加，并加上偏移量 ϕ0。

为了完成描述，我们必须定义激活函数 a[•]。有许多可能性，但最常见的选择是修正线性单元（ReLU）：

\[ a[z] = \text{ReLU}[z] = \begin{cases} 
0 & z < 0 \\
z & z \geq 0 
\end{cases} \quad (3.2) \]

这个函数在输入为正时返回输入值，否则返回零（见图3.1）。



我们定义了以下隐藏单元：
\[ h1 = a[θ10 + θ11x] \]
\[ h2 = a[θ20 + θ21x] \]
\[ h3 = a[θ30 + θ31x] \] \[ \quad（3.3）\]

其中，我们将 \( h1 \)、\( h2 \) 和 \( h3 \) 称为隐藏单元。接着，我们通过将这些隐藏单元与线性函数结合来计算输出：
\[ y = ϕ0 + ϕ1h1 + ϕ2h2 + ϕ3h3  \quad （3.4）\]

图3.4描绘了神经网络。
a) 输入x位于左侧，隐藏单元h1、h2和h3位于中间，输出y位于右侧。计算流程从左向右进行。输入用于计算隐藏单元，这些单元组合起来生成输出。图中的每根箭头代表一个参数（截距用橙色表示，斜率用黑色表示）。每个参数将其来源相乘，然后将结果加到其目标上。例如，我们将参数ϕ1乘以源h1，并将其加到y上。我们引入额外的节点，包含数值为1的圆圈（橙色），将偏置纳入这个方案，因此我们将ϕ0乘以1（没有效果），并加到y上。在隐藏单元上应用ReLU函数。
b) 更典型地，省略了截距、ReLU函数和参数名称；这种更简单的描述代表了同一个网络。
![神经网络图3.4](3.2.png "神经网络")

### Universal approximation theorem 通用逼近定理

Universal Approximation Theorem（通用逼近定理）是指神经网络的一类理论结果，表明一个具有至少一层隐藏层的神经网络可以以任意精度逼近任何连续函数，只要给予足够数量的隐藏单元和适当的参数调整。具体来说，这个定理说明了在理论上，一个具有足够多神经元的单隐藏层神经网络可以近似于任何从一个有限维实数空间到另一个有限维实数空间的Borel可测函数。

简单来说，Universal Approximation Theorem告诉我们，单层隐藏层的神经网络（MLP）在理论上可以以任何精度逼近任何连续函数。这个结果对神经网络的实际应用具有重要意义，它表明即使是相对简单的神经网络结构，也可以在理论上实现复杂的函数逼近和模式识别任务。

在前面的部分中，我们介绍了一个具有一个输入、一个输出、ReLU激活函数和三个隐藏单元的示例神经网络。现在我们稍微推广一下，考虑具有D个隐藏单元的情况，其中第d个隐藏单元定义为：
\[ h_d = a[\theta_{d0} + \theta_{d1} x], \quad \text{(3.5)} \]
这些隐藏单元线性组合以生成输出：
\[ y = \phi_0 + \sum_{d=1}^{D} \phi_d h_d. \quad \text{(3.6)} \]
浅层网络中隐藏单元的数量是网络容量的一种度量。使用ReLU激活函数时，具有D个隐藏单元的网络的输出至多具有D个连接点，因此是一个至多具有D+1个线性区域的分段线性函数。随着隐藏单元的增加，模型可以逼近更复杂的函数。
事实上，具有足够容量（隐藏单元）的浅层网络可以以任意精度描述定义在实数线紧致子集上的任何连续1D函数。为了看到这一点，考虑每次增加一个隐藏单元，函数都会增加另一个线性区域。随着这些线性区域变得更多，它们表示函数的部分会变得越来越小，这些部分越来越能够通过一条直线来良好逼近（见图3.5）。神经网络逼近任意连续函数的能力可以进行正式的证明，这就是通用逼近定理。
![](3.2-1.png "逼近定理")
###  Multivariate inputs and outputs
#### outputs

为了将网络扩展到多变量输出 y，我们简单地为每个输出使用隐藏单元的不同线性函数。因此，对于具有标量输入 x、四个隐藏单元 h1、h2、h3 和 h4，以及2维多变量输出 y = [y1, y2]^T 的网络，定义如下：
\[ h1 = a[\theta_{10} + \theta_{11} x] \]
\[ h2 = a[\theta_{20} + \theta_{21} x] \]
\[ h3 = a[\theta_{30} + \theta_{31} x] \]
\[ h4 = a[\theta_{40} + \theta_{41} x], \quad \text{(3.7)} \]
以及\[ y1 = \phi_{10} + \phi_{11} h1 + \phi_{12} h2 + \phi_{13} h3 + \phi_{14} h4 \]
\[ y2 = \phi_{20} + \phi_{21} h1 + \phi_{22} h2 + \phi_{23} h3 + \phi_{24} h4. \quad \text{(3.8)} \]

这两个输出分别是隐藏单元的两个不同线性函数。正如我们在图3.3中看到的那样，“关节”在分段函数中的位置取决于在隐藏单元处由ReLU函数截断的初始线性函数 \(\theta_{•0} + \theta_{•1} x\)。由于输出 y1 和 y2 都是相同四个隐藏单元的不同线性函数，每个输出中的四个“关节”必须在相同的位置。然而，线性区域的斜率和整体垂直偏移可以不同（见图3.6）。

这个就是说单变量可以对应多变量，也就是可以通过一个向量经过一个感知机转化成另外一个向量。
![](3.3.png "多变量输出")
#### inputs
