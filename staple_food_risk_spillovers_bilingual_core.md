# Multiscale risk spillovers and external driving factors: Evidence from the global futures and spot markets of staple foods
# 多尺度风险溢出与外部驱动因素：来自全球主粮期货与现货市场的证据

> 说明：这是基于用户上传论文 Markdown 生成的中英对照核心阅读版。正文按原文逻辑逐段翻译，保留论文结构、主要段落、公式位置、图表题名和表注；大型数值表未逐格翻译，建议与原文表格配合使用。

## Abstract / 摘要

**EN**  
Stable and efficient food markets are crucial for global food security, yet international staple food markets are increasingly exposed to complex risks, including intensified risk contagion and escalating external uncertainties. This paper systematically investigates risk spillovers in global staple food markets and explores the key determinants of these spillover effects, combining innovative decomposition-reconstruction techniques, risk connectedness analysis, and random forest models. The findings reveal that short-term components exhibit the highest volatility, with futures components generally more volatile than spot components. Further analysis identifies two main risk transmission patterns, namely cross-grain and cross-timescale transmission, and clarifies the distinct roles of each component in various net risk spillover networks. Additionally, price drivers, external uncertainties, and core supply-demand indicators significantly influence these spillover effects, with heterogeneous importance of varying factors in explaining different risk spillovers. This study provides valuable insights into the risk dynamics of staple food markets, offers evidence-based guidance for policymakers and market participants to enhance risk warning and mitigation efforts, and supports the stabilization of international food markets and the safeguarding of global food security.

**中文**  
稳定而高效的粮食市场对全球粮食安全至关重要。然而，国际主粮市场正越来越多地暴露于复杂风险之中，包括风险传染加剧和外部不确定性上升。本文结合创新性的分解—重构技术、风险连通性分析与随机森林模型，系统考察全球主粮市场的风险溢出，并探究这些溢出效应的关键决定因素。研究发现，短期成分波动性最高，且期货成分通常比现货成分更为波动。进一步分析识别出两种主要风险传导模式，即跨粮食品种传导和跨时间尺度传导，并阐明了各成分在不同净风险溢出网络中的差异化作用。此外，价格驱动因素、外部不确定性和核心供需指标会显著影响这些溢出效应，不同因素对不同风险溢出的解释重要性也存在异质性。本文为理解主粮市场风险动态提供了有价值的洞见，也为政策制定者和市场参与者加强风险预警与缓释提供了经验证据，并有助于稳定国际粮食市场、维护全球粮食安全。

**Keywords / 关键词**  
Staple food; Risk spillover; ICEEMDAN; $R^{2}$ decomposed connectedness; Random forest model  
主粮；风险溢出；ICEEMDAN；$R^{2}$ 分解连通性；随机森林模型

---

## 1 Introduction / 引言

**EN**  
Food is the cornerstone of national stability and the foundation of human survival. However, global and local food security is becoming increasingly precarious, with numerous nations and regions grappling with mounting risks and challenges. According to The State of Food Security and Nutrition in the World 2024, an estimated 9.1% of the global population remained undernourished in 2023, and approximately 2.33 billion people experienced moderate or severe food insecurity. The report underscores the intensifying severity of key challenges, including armed conflicts, extreme weather events, and economic slowdowns. Furthermore, persistent structural issues, such as increasing food costs, heightened food price volatility, and pronounced regional imbalances in supply and demand, exacerbate the current food crisis.

**中文**  
粮食是国家稳定的基石，也是人类生存的基础。然而，全球和地方层面的粮食安全正变得愈发脆弱，许多国家和地区都在应对持续上升的风险与挑战。根据《2024年世界粮食安全和营养状况》，2023 年全球约 9.1% 的人口仍处于营养不足状态，约 23.3 亿人经历了中度或重度粮食不安全。该报告强调，武装冲突、极端天气事件和经济放缓等关键挑战日益严峻。此外，粮食成本上升、粮价波动加剧以及供需区域失衡突出等持续性结构问题，也进一步加深了当前粮食危机。

**EN**  
Addressing global food insecurity has thus become an urgent priority, with the stability and efficiency of food markets playing a pivotal role. Futures and spot markets for agricultural commodities are critical components of the global food system. They facilitate global food trade and production through price discovery and risk management functions while simultaneously influencing food security through resource allocation and transmission of external shocks. Futures prices reflect market expectations of future supply and demand conditions, whereas spot prices directly represent current market conditions.

**中文**  
因此，应对全球粮食不安全已成为紧迫任务，而粮食市场的稳定性和效率在其中具有关键作用。农产品期货市场和现货市场是全球粮食体系的重要组成部分。它们通过价格发现和风险管理功能促进全球粮食贸易与生产，同时又通过资源配置和外部冲击传导影响粮食安全。期货价格反映市场对未来供需状况的预期，而现货价格直接反映当前市场状况。

**EN**  
A critical concern lies in developing a comprehensive understanding of how risks transmit within international staple crop markets, spanning food futures and spots, across different commodities, and over varying timescales. These spillover effects may magnify market instability, disrupt supply chains, and increase uncertainties for producers, traders, and policymakers. External shocks and internal drivers, such as climate policy uncertainty, energy prices, and transportation costs, may further exacerbate these risk spillover effects.

**中文**  
一个关键问题在于，需要全面理解风险如何在国际主粮市场内部传导：这种传导既可能跨越粮食期货与现货市场，也可能跨越不同商品，并在不同时间尺度上发生。这些溢出效应可能放大市场不稳定性、扰乱供应链，并增加生产者、贸易商和政策制定者面对的不确定性。气候政策不确定性、能源价格和运输成本等外部冲击与内部驱动因素，也可能进一步加剧这些风险溢出效应。

**EN**  
This paper systematically investigates risk contagion within the international food market and identifies the underlying determinants of spillover effects. By employing a novel decomposition-reconstruction methodology, futures and spot returns of wheat, maize, soybean, and rice are decomposed into short-, medium-, and long-term components. Risk connectedness analysis uncovers two main patterns of risk transmission: stronger spillovers occur between same-timescale components of different grains and between same-grain components at different timescales. Both static and dynamic analyses consistently demonstrate significant and robust cross-grain and cross-timescale spillovers.

**中文**  
本文系统考察国际粮食市场内部的风险传染，并识别溢出效应背后的决定因素。通过采用新的分解—重构方法，本文将小麦、玉米、大豆和稻米的期货与现货收益率分解为短期、中期和长期成分。风险连通性分析揭示了两类主要风险传导模式：不同粮食品种相同时间尺度成分之间存在较强溢出，同一粮食品种不同时间尺度成分之间也存在较强溢出。静态和动态分析均一致表明，跨粮食品种和跨时间尺度的风险溢出显著且稳健。

**EN**  
From a dual perspective of cross-grain and cross-timescale, this study utilizes advanced and integrative methods to clarify the mechanisms of risk transmission and identify critical drivers of risk spillovers in the global staple food market. Unlike previous research, which predominantly relies on original prices or returns, this paper introduces decomposition and reconstruction techniques to reveal the intrinsic characteristics of grain futures and spot returns, thereby proposing a new analytical framework for examining risk contagion across multiple dimensions.

**中文**  
本文从跨粮食品种和跨时间尺度两个视角出发，利用较为先进且整合性的研究方法，阐明全球主粮市场中的风险传导机制，并识别风险溢出的关键驱动因素。不同于以往主要依赖原始价格或收益率的研究，本文引入分解与重构技术，以揭示粮食期货与现货收益率的内在特征，并据此提出一个考察多维风险传染的新分析框架。

---

## 2 Literature review / 文献综述

**EN**  
Risk transmission across financial markets or assets, often referred to as risk spillover, has attracted substantial academic attention. With globalization and financial market integration deepening, localized risk events can propagate rapidly through different channels and may trigger systemic financial crises. The 2008 global financial crisis and the COVID-19 pandemic highlight the importance of understanding risk spillover effects.

**中文**  
金融市场或资产之间的风险传导通常被称为风险溢出，已引起学界广泛关注。随着全球化和金融市场一体化加深，局部风险事件可以通过不同渠道迅速传播，并可能引发系统性金融危机。2008 年全球金融危机和新冠疫情凸显了理解风险溢出效应的重要性。

**EN**  
Risk spillover measurement has evolved from traditional linear analysis to dynamic modeling. Early studies relied on Granger causality tests and linear regression models, but these methods struggled to capture asymmetric, nonlinear, and dynamic risk transmission relationships. Advanced methods such as CoVaR and dynamic connectedness frameworks were therefore developed. CoVaR focuses on tail risk and bilateral dependence, while the generalized connectedness framework can capture risk transmission dynamics across multiple time series simultaneously.

**中文**  
风险溢出测度方法已经从传统线性分析逐步发展到动态建模。早期研究主要依赖格兰杰因果检验和线性回归模型，但这些方法难以捕捉非对称、非线性以及动态风险传导关系。因此，CoVaR 和动态连通性框架等更先进的方法被提出。CoVaR 关注尾部风险和双边依赖，而广义连通性框架能够同时刻画多个时间序列之间的风险传导动态。

**EN**  
The connectedness method uses generalized forecast error variance decomposition within vector autoregressive models to construct total and directional spillover indices. It has been widely used in multi-asset and cross-market studies. Later extensions include frequency-domain connectedness, high-dimensional connectedness based on sparse networks, and the $R^{2}$ decomposed connectedness approach, which improves interpretability and avoids biases caused by certain standardization procedures.

**中文**  
连通性方法利用向量自回归模型中的广义预测误差方差分解，构建总溢出指数和方向性溢出指数。该方法已广泛用于多资产和跨市场研究。后续扩展包括频域连通性、基于稀疏网络的高维连通性，以及 $R^{2}$ 分解连通性方法。后者增强了模型解释性，并避免了某些标准化处理可能带来的偏差。

**EN**  
The increasing financialization of commodities has heightened price volatility and market linkages in agricultural markets. Given the role of agricultural markets in global food security, risk spillovers in these markets have become increasingly important. Existing studies show that energy market spillovers can significantly increase risk exposure in agricultural markets, and that agricultural futures are particularly susceptible to shocks during turbulent periods.

**中文**  
商品金融化程度提升增强了农业市场的价格波动和市场联动。鉴于农业市场在全球粮食安全中的作用，农业市场风险溢出研究变得越来越重要。现有研究表明，能源市场溢出会显著增加农业市场的风险暴露，且农产品期货在动荡时期尤其容易受到冲击影响。

**EN**  
A smaller body of literature explores drivers of food price volatility, including biofuel demand, climate-induced yield reductions, energy price hikes, declining inventories, export restrictions, supply-demand fundamentals, policy changes, oil price volatility, geopolitical risks, and extreme events such as the COVID-19 pandemic and the Russia-Ukraine conflict.

**中文**  
另有少量文献探讨食品价格波动的驱动因素，包括生物燃料需求、气候导致的减产、能源价格上涨、库存下降、出口限制、供需基本面、政策变化、油价波动、地缘政治风险，以及新冠疫情和俄乌冲突等极端事件。

**EN**  
However, several gaps remain. First, risk transmission across grain markets at different timescales remains underexplored. Second, the ability of potential drivers to explain different dimensions of risk spillovers and their relative importance has received limited attention. This study addresses these gaps by examining risk contagion in international staple food markets from both cross-grain and cross-timescale perspectives.

**中文**  
然而，现有研究仍存在若干空白。首先，不同时间尺度下粮食市场之间的风险传导研究仍不充分。其次，潜在驱动因素解释不同维度风险溢出的能力及其相对重要性尚未得到足够关注。本文通过从跨粮食品种和跨时间尺度两个视角考察国际主粮市场中的风险传染，试图弥补这些不足。

---

## 3 Methodology / 研究方法

### 3.1 Empirical mode decomposition / 经验模态分解

**EN**  
Empirical mode decomposition (EMD) is a signal decomposition method designed for nonlinear and non-stationary data. Unlike wavelet or Fourier decomposition, which rely on predefined basis functions, EMD adapts to the intrinsic timescale features of the data and is therefore theoretically applicable to many types of signals.

**中文**  
经验模态分解（EMD）是一种用于处理非线性和非平稳数据的信号分解方法。不同于依赖预设基函数的小波分解或傅里叶分解，EMD 能够适应数据自身的内在时间尺度特征，因此在理论上适用于多种类型的信号。

**EN**  
The core concept behind EMD is the Hilbert-Huang Transform. The original time series is extracted step by step according to different time periods, producing several data sequences with distinct characteristic scales. Each sequence can be regarded as an intrinsic mode function (IMF). An IMF must satisfy two conditions: the number of extrema and zero crossings must be equal or differ by at most one, and the mean of the upper and lower envelopes must be zero at any time.

**中文**  
EMD 的核心思想来自 Hilbert-Huang 变换。该方法按照不同时间周期逐步提取原始时间序列，从而生成若干具有不同特征尺度的数据序列。每个序列可视为一个本征模态函数（IMF）。IMF 需要满足两个条件：极值点数量与过零点数量相等或最多相差一个；任意时刻上、下包络线的均值为零。

**EN**  
A complex time series $x(t)$ can be decomposed into multiple IMFs and a residue through sifting:
$$
x(t)=\sum_{n=1}^{N}c_{n}(t)+u(t),\quad t=1,\dots,T.
$$

Here, $N$ is the number of IMFs, $c_n$ is the $n$-th IMF, and $u(t)$ is the residue. This study uses cubic spline interpolation because it provides smoother envelope curves than Hermite interpolation.

**中文**  
复杂时间序列 $x(t)$ 可通过筛分过程分解为多个 IMF 和一个残差项：
$$
x(t)=\sum_{n=1}^{N}c_{n}(t)+u(t),\quad t=1,\dots,T.
$$

其中，$N$ 为 IMF 数量，$c_n$ 为第 $n$ 个 IMF，$u(t)$ 为残差项。本文采用三次样条插值，因为其包络曲线通常比 Hermite 插值更平滑。

**EN**  
Although EMD has advantages, it also faces problems such as mode mixing, stopping criteria, and end effects. To address these issues, this paper applies ICEEMDAN, an improved complete ensemble EMD with adaptive noise. ICEEMDAN adds adaptive white-noise components, computes local envelope means, and obtains IMFs sequentially, thereby reducing residual noise and reconstruction error.

**中文**  
尽管 EMD 具有优势，但也面临模态混叠、停止准则设定和端点效应等问题。为解决这些问题，本文采用 ICEEMDAN，即改进的自适应噪声完备集合经验模态分解。ICEEMDAN 通过加入自适应白噪声成分、计算局部包络均值并按顺序提取 IMF，降低残余噪声和重构误差。

### 3.2 Mode reconstruction method / 模态重构方法

**EN**  
After decomposing the data into IMFs and a residual term, the paper improves the KMC-RLN reconstruction method and proposes a GMM-RLN method. The run-length number is an indicator of volatility: higher run-length values imply greater volatility. Each IMF is transformed into a symbolic sequence around its mean, and consecutive identical symbols are counted as runs.

**中文**  
在将数据分解为 IMF 和残差项之后，本文改进了 KMC-RLN 重构方法，并提出 GMM-RLN 方法。游程数是衡量波动性的指标：游程数越高，表示波动性越强。每个 IMF 会根据其均值转化为符号序列，连续相同符号被计为一个游程。

**EN**  
The Gaussian mixture model is then used for clustering these run-length numbers. Compared with existing reconstruction methods, GMM-RLN considers both data fluctuation characteristics and data length, and is more flexible when cluster boundaries are fuzzy. The number of clusters is set to 3, corresponding to short-term high-frequency, medium-term medium-frequency, and long-term low-frequency components.

**中文**  
随后，本文使用高斯混合模型对这些游程数进行聚类。与既有重构方法相比，GMM-RLN 同时考虑数据波动特征和数据长度，并且在聚类边界模糊时具有更高灵活性。本文将聚类数量设为 3，对应短期高频成分、中期中频成分和长期低频成分。

### 3.3 $R^{2}$ decomposed connectedness approach / $R^{2}$ 分解连通性方法

**EN**  
The paper uses the $R^{2}$ decomposed connectedness approach to measure risk transmission. A VAR model is represented in its VMA form, and generalized forecast error variance decomposition is used to quantify directional spillovers. Under random-walk assumptions, GFEVD can be simplified into a squared correlation term, equivalent to an $R^{2}$ measure from a bivariate regression.

**中文**  
本文使用 $R^{2}$ 分解连通性方法衡量风险传导。首先将 VAR 模型表示为 VMA 形式，并利用广义预测误差方差分解度量方向性溢出。在随机游走假设下，GFEVD 可简化为平方相关项，等价于双变量回归中的 $R^{2}$ 指标。

**EN**  
Instead of normalizing GFEVD row sums, the $R^{2}$ decomposed connectedness approach uses multivariate regression and principal component analysis to decompose the $R^{2}$ contribution of each explanatory variable. The main indices include $TO_i$, $FROM_i$, $NET_i$, $NPDC_{ij}$, and $TCI$.

**中文**  
与直接对 GFEVD 行和进行标准化不同，$R^{2}$ 分解连通性方法使用多元回归和主成分分析，分解各解释变量对 $R^{2}$ 的贡献。主要指标包括 $TO_i$、$FROM_i$、$NET_i$、$NPDC_{ij}$ 和 $TCI$。

**Formula / 公式**  
$$
TO_i=\sum_{j=1}^{k}R_{ji}^{2G},\quad FROM_i=\sum_{j=1}^{k}R_{ij}^{2G},\quad NET_i=TO_i-FROM_i,
$$
$$
NPDC_{ij}=R_{ij}^{2G}-R_{ji}^{2G},\quad TCI=\frac{1}{k}\sum_{i=1}^{k}R_i^2.
$$

**EN**  
A positive $NET_i$ indicates that variable $i$ is a net risk transmitter, while a negative value indicates that it is a net risk receiver. The TCI measures the average risk spillover in the network and serves as a proxy for market risk.

**中文**  
$NET_i$ 为正表示变量 $i$ 是风险净输出者，为负则表示其为风险净接收者。TCI 衡量网络中的平均风险溢出水平，可作为市场风险的代理指标。

### 3.4 Random forest model / 随机森林模型

**EN**  
Random forest is a non-parametric method for classification and regression. It combines multiple decision trees, averages their predictions in regression problems, and is suitable for complex datasets because it can capture nonlinear relationships and resist noise, missing data, and overfitting.

**中文**  
随机森林是一种可用于分类和回归的非参数方法。它组合多棵决策树，并在回归问题中对各树预测结果取平均。由于能够捕捉非线性关系，并且对噪声、缺失数据和过拟合具有较强鲁棒性，随机森林适合处理复杂数据集。

**Formula / 公式**  
$$
Y=\frac{1}{K}\sum_{k=1}^{K}f_k(x),\quad
MAE=\frac{1}{Q}\sum_{q=1}^{Q}|y_q-\hat y_q|,\quad
MSE=\frac{1}{Q}\sum_{q=1}^{Q}(y_q-\hat y_q)^2.
$$

**EN**  
The paper applies random forest to examine the relationship between each risk-spillover network’s TCI and a series of explanatory variables. The dataset is split into 80% training and 20% testing, and grid search is used to tune hyperparameters such as the number of trees, maximum tree depth, and number of features used for splitting.

**中文**  
本文使用随机森林考察各风险溢出网络的 TCI 与一系列解释变量之间的关系。数据集被划分为 80% 训练集和 20% 测试集，并通过网格搜索调节超参数，如决策树数量、最大树深度和用于分裂的特征数量。

---

## 4 Data description / 数据说明

### 4.1 Data sources / 数据来源

**EN**  
The study focuses on wheat, maize, soybean, and rice. It obtains daily closing prices of continuous futures contracts for wheat, corn, soybean, and rough rice traded on CBOT from Wind, and daily price indices for wheat, maize, soybean, and rice from the International Grains Council. CBOT futures prices serve as global agricultural pricing benchmarks, while IGC indices reflect spot export quotations from major producers. The sample period runs from January 3, 2000, to December 29, 2023.

**中文**  
本文聚焦小麦、玉米、大豆和稻米四种主粮。研究从 Wind 获取 CBOT 交易的小麦、玉米、大豆和糙米期货连续合约日收盘价，并从国际谷物理事会获取小麦、玉米、大豆和稻米的日价格指数。CBOT 期货价格可视为全球农产品定价基准，而 IGC 指数反映主要生产国现货出口报价。样本期为 2000 年 1 月 3 日至 2023 年 12 月 29 日。

**EN**  
Twelve explanatory variables are selected: ARMI, FPI, EPI, BDI, GPR, EPU, CPU, GND, PROD, IMP, CONS, and ES. They cover price-driven factors, external shock factors, and core supply-demand indicators. BDI and GPR are daily; ARMI, FPI, EPI, EPU, CPU, and GND are monthly; and PROD, IMP, CONS, and ES are annual. Forward filling is used for data alignment.

**中文**  
本文选择 12 个解释变量：ARMI、FPI、EPI、BDI、GPR、EPU、CPU、GND、PROD、IMP、CONS 和 ES。这些变量覆盖价格驱动因素、外部冲击因素和核心供需指标。其中 BDI 和 GPR 为日度数据；ARMI、FPI、EPI、EPU、CPU 和 GND 为月度数据；PROD、IMP、CONS 和 ES 为年度数据。本文使用向前填充进行数据对齐。

### 4.2 Statistical description / 统计描述

**EN**  
Figures 1 and 2 show the evolution of prices and returns for the four staples. Futures and spot prices generally move together and exhibit statistically significant positive correlations. All four staples display notable volatility during the global food crises of 2006-2008, 2010-2012, and the period since 2020. Futures returns fluctuate more than spot returns, and all return series show volatility clustering.

**中文**  
图 1 和图 2 展示了四种主粮价格和收益率的演变。期货与现货价格总体走势一致，并具有统计显著的正相关关系。四种主粮在 2006—2008 年、2010—2012 年以及 2020 年以来的全球粮食危机期间均出现明显波动。期货收益率波动大于现货收益率，所有收益率序列都表现出波动聚集特征。

**EN**  
Table 1 reports descriptive statistics. Futures returns have larger maxima, smaller minima, and higher standard deviations than corresponding spot returns, implying stronger volatility in futures markets. The return distributions are asymmetric and fat-tailed. Jarque-Bera and ADF statistics are significant at the 1% level, indicating non-normality and stationarity.

**中文**  
表 1 报告描述性统计。期货收益率相较对应现货收益率具有更大的最大值、更小的最小值和更高的标准差，说明期货市场波动性更强。收益率分布存在非对称性和厚尾特征。Jarque-Bera 检验和 ADF 检验统计量均在 1% 水平上显著，说明序列不服从正态分布且为平稳序列。

---

## 5 Empirical analysis / 实证分析

### 5.1 Decomposition of grain return series / 粮食收益率序列分解

**EN**  
The ICEEMDAN method decomposes futures and spot return series for the four staple crops. The results for wheat futures are shown in Figure 3, and the other series are shown in Appendix A. IMFs are ordered from high to low frequency, followed by the residue. The series are usually decomposed into 10 or 11 IMFs.

**中文**  
本文使用 ICEEMDAN 方法分解四种主粮的期货和现货收益率序列。小麦期货结果见图 3，其他序列结果见附录 A。IMF 按照频率从高到低排列，最后为残差项。收益率序列通常被分解为 10 个或 11 个 IMF。

**EN**  
For each decomposed mode, the paper computes the mean period, Spearman correlation with the original series, and variance contribution. The results show that IMF mean periods increase gradually, while correlation and importance generally decrease with IMF order. IMF1 contributes the most to volatility, whereas the residue contributes very little.

**中文**  
对于每个分解模态，本文计算平均周期、与原始序列的 Spearman 相关系数以及方差贡献。结果显示，IMF 平均周期逐渐增加，而相关性和重要性通常随 IMF 阶数上升而下降。IMF1 对波动贡献最大，残差项贡献很小。

### 5.2 Reconstruction of grain return series / 粮食收益率序列重构

**EN**  
Using GMM-RLN, the decomposed IMFs are reconstructed into short-term, medium-term, and long-term components. IMF1 and IMF2 are grouped as short-term components; IMF3, IMF4, and IMF5 are grouped as medium-term components; IMF6 and the remaining longer IMFs are grouped as long-term components.

**中文**  
使用 GMM-RLN 方法后，分解得到的 IMF 被重构为短期、中期和长期成分。IMF1 与 IMF2 被划分为短期成分；IMF3、IMF4 和 IMF5 被划分为中期成分；IMF6 及其余更长期 IMF 被划分为长期成分。

**EN**  
Short-term components have an average period ceiling of about five working days, medium-term components about 44 working days, and long-term components up to about 3,021 working days. Short-term components fluctuate the most, followed by medium-term components, while long-term components fluctuate the least. Futures components are generally more volatile than spot components.

**中文**  
短期成分平均周期上限约为 5 个工作日，中期成分约为 44 个工作日，长期成分最长约为 3021 个工作日。短期成分波动最大，其次为中期成分，长期成分波动最小。期货成分通常比现货成分波动更强。

**EN**  
The reconstructed components show violent fluctuations during major crisis periods, including the 2006-2008 food crisis, the 2008 global financial crisis, the 2010-2012 food crisis, and the post-2020 food crisis triggered by COVID-19, extreme weather, and regional conflicts.

**中文**  
重构成分在若干重大危机期间出现剧烈波动，包括 2006—2008 年粮食危机、2008 年全球金融危机、2010—2012 年粮食危机，以及 2020 年后由新冠疫情、极端天气和地区冲突触发的粮食危机。

### 5.3 Static analysis of risk spillovers / 风险溢出的静态分析

**EN**  
After reconstructing all components, the paper uses the $R^{2}$ decomposed connectedness approach to calculate full-sample risk connectedness. Figure 5 reveals two major spillover patterns. First, stronger spillovers occur among same-timescale components across different grains. Second, significant spillovers also occur among different-timescale components within the same grain.

**中文**  
重构所有成分后，本文使用 $R^{2}$ 分解连通性方法计算全样本风险连通性。图 5 揭示了两类主要溢出模式。第一，不同粮食品种相同时间尺度成分之间存在更强溢出。第二，同一粮食品种不同时间尺度成分之间也存在显著溢出。

**EN**  
Table 4 shows that the TCI values for same-timescale components are large, indicating significant cross-grain spillovers. Soybean contributes most to short-term spillovers, followed by maize and wheat. Rice contributes little, which is related to its lower internationalization, limited futures trading volume, low market liquidity, and stable production-consumption structure.

**中文**  
表 4 显示，相同时间尺度成分的 TCI 值较高，说明跨粮食品种风险溢出显著。大豆对短期溢出贡献最大，其后为玉米和小麦。稻米贡献较小，这与其国际化程度较低、期货交易量有限、市场流动性较低以及生产消费结构较稳定有关。

**EN**  
Table 5 shows static spillovers across different timescales within each grain. The soybean market has the highest TCI, followed by wheat, maize, and rice. For wheat, maize, and soybean, short-term components contribute most to spillovers; for rice, long-term components contribute the most, although overall spillovers remain low.

**中文**  
表 5 展示了每种粮食品种内部不同时间尺度成分之间的静态溢出。大豆市场 TCI 最高，其后为小麦、玉米和稻米。对于小麦、玉米和大豆，短期成分对溢出的贡献最大；对于稻米，长期成分贡献最大，但整体溢出水平仍较低。

### 5.4 Dynamic analysis of risk spillovers / 风险溢出的动态分析

**EN**  
The dynamic analysis uses a one-year rolling window. Dynamic average TCIs are higher than static TCIs, suggesting that risk spillovers are more pronounced dynamically. Long-term components show especially high dynamic connectedness, possibly because long-term risk spillovers last longer within rolling windows.

**中文**  
动态分析采用一年滚动窗口。动态平均 TCI 高于静态 TCI，说明动态情形下风险溢出更为明显。长期成分的动态连通性尤其高，可能是因为长期风险溢出在滚动窗口内持续时间更长。

**EN**  
Across short-, medium-, and long-term components, soybean is the main risk transmitter and receiver in global staple crop markets, followed by maize and wheat, while rice has the weakest effect. In the long-term component network, soybean and maize act as net risk transmitters, while rice futures and spot act as net risk receivers.

**中文**  
综合短期、中期和长期成分来看，大豆是全球主粮市场中最主要的风险输出者和接收者，其后为玉米和小麦，稻米作用最弱。在长期成分网络中，大豆和玉米是风险净输出者，而稻米期货和现货是风险净接收者。

**EN**  
The dynamic TCI series show elevated spillovers during major crises, including the 2006 global food crisis, the 2008 global financial crisis, the 2012 global food crisis, and the food crisis since 2020. In recent years, medium- and long-term spillovers have shown a clear upward trend.

**中文**  
动态 TCI 序列显示，在重大危机期间风险溢出显著上升，包括 2006 年全球粮食危机、2008 年全球金融危机、2012 年全球粮食危机以及 2020 年以来的粮食危机。近年来，中期和长期溢出呈明显上升趋势。

**EN**  
Net risk spillover networks show that maize futures and wheat futures are the main risk transmitters among short-term components. The largest spillover paths are from wheat futures to wheat spot and from maize futures to maize spot, confirming substantial transmission from agricultural futures markets to corresponding spot markets.

**中文**  
净风险溢出网络显示，玉米期货和小麦期货是短期成分中的主要风险输出者。最大溢出路径分别是小麦期货到小麦现货、玉米期货到玉米现货，说明农产品期货市场向对应现货市场存在显著风险传导。

**EN**  
For cross-timescale spillovers, short-term components dominate internal risk transmission in soybean, maize, and wheat markets, while long-term components dominate in the rice market. Net spillover networks further show that the rice market has a distinct transmission pattern compared with the other three staple crops.

**中文**  
对于跨时间尺度溢出，短期成分主导大豆、玉米和小麦市场内部的风险传导，而长期成分主导稻米市场内部传导。净溢出网络进一步表明，稻米市场的传导模式与其他三类主粮市场不同。

### 5.5 Factors influencing risk spillovers / 风险溢出的影响因素

**EN**  
After identifying significant cross-grain and cross-timescale spillovers, the paper explores their drivers using random forest regression. Twelve explanatory variables are selected: ARMI, FPI, EPI, BDI, GPR, EPU, CPU, GND, PROD, IMP, CONS, and ES. These variables cover supply, demand, production, transportation, and external uncertainties.

**中文**  
在识别出显著跨粮食品种和跨时间尺度溢出后，本文使用随机森林回归探究其驱动因素。选取的十二个解释变量包括 ARMI、FPI、EPI、BDI、GPR、EPU、CPU、GND、PROD、IMP、CONS 和 ES，覆盖供给、需求、生产、运输和外部不确定性等方面。

**EN**  
The random forest model fits the training and test data well. The small MAE and MSE values indicate that the selected variables effectively explain variation in TCI. These drivers can therefore serve as potential early-warning indicators for systemic risks in the global food system.

**中文**  
随机森林模型在训练集和测试集上均拟合良好。较小的 MAE 和 MSE 说明所选变量能够有效解释 TCI 的变化。因此，这些驱动因素可作为全球粮食系统系统性风险的潜在早期预警指标。

**EN**  
For short-term components, ARMI and FPI are the two most important explanatory variables. ARMI reflects upstream agricultural input costs, while FPI reflects global food price dynamics and consumer-side market pressure. Together, they capture market dynamics from production and consumption price dimensions.

**中文**  
对于短期成分，ARMI 和 FPI 是最重要的两个解释变量。ARMI 反映上游农业投入成本，FPI 反映全球食品价格动态和消费端市场压力。两者共同从生产端和消费端价格维度刻画市场动态。

**EN**  
For medium-term components, ES and CONS also become important. ES reflects supply security and reserve capacity, while CONS represents actual grain usage and market demand. Thus, medium-term spillovers are driven by both price dynamics and supply-demand quantities.

**中文**  
对于中期成分，ES 和 CONS 也变得重要。ES 反映供给安全和储备能力，CONS 表示实际粮食使用量和市场需求。因此，中期溢出同时受到价格动态和供需数量因素驱动。

**EN**  
For long-term components, EPU, BDI, EPI, ARMI, and CPU play important roles. This indicates that long-term spillovers are shaped by a broader set of factors, including economic policy uncertainty, climate policy uncertainty, energy prices, production costs, and transportation costs.

**中文**  
对于长期成分，EPU、BDI、EPI、ARMI 和 CPU 发挥重要作用。这说明长期溢出由更广泛的因素塑造，包括经济政策不确定性、气候政策不确定性、能源价格、生产成本和运输成本。

**EN**  
For cross-timescale spillovers within each grain market, FPI, ARMI, and EPI consistently show high importance. ES strongly affects spillovers within wheat, maize, and soybean markets, but has limited impact on rice because rice production and consumption are regionally concentrated and many major producers intervene to stabilize domestic supply and prices.

**中文**  
对于各粮食品种市场内部的跨时间尺度溢出，FPI、ARMI 和 EPI 始终具有较高重要性。ES 显著影响小麦、玉米和大豆市场内部溢出，但对稻米影响有限，因为稻米生产和消费具有区域集中性，且许多主要生产国会采取政策干预以稳定国内供应和价格。

**EN**  
BDI is particularly important for wheat and rice spillovers. Wheat and rice are often transported as bulk commodities, and their supply chains are less flexible. By contrast, maize and soybean have more flexible transportation modes, storage infrastructure, and end-use substitution possibilities, making them less sensitive to spot transportation cost changes.

**中文**  
BDI 对小麦和稻米溢出尤其重要。小麦和稻米通常以散货形式运输，供应链灵活性较低。相比之下，玉米和大豆具有更灵活的运输方式、储藏基础设施和终端用途替代可能性，因此对现货运输成本变化的敏感性较低。

### 5.6 Robustness checks / 稳健性检验

**EN**  
The paper checks robustness by changing the rolling window length from 252 trading days to 200 and 300 trading days. The resulting TCIs show only minor numerical differences and highly consistent trends, suggesting that the dynamic spillover results are not sensitive to window-length choice.

**中文**  
本文通过将滚动窗口长度从 252 个交易日改为 200 个和 300 个交易日进行稳健性检验。得到的 TCI 仅存在较小数值差异，整体趋势高度一致，说明动态溢出结果对窗口长度选择并不敏感。

**EN**  
The random forest results are also checked by changing the train-test split from 80/20 to 70/30 and reselecting parameters through grid search. The evaluation metrics and factor-importance patterns remain broadly consistent, confirming the robustness of the random forest findings.

**中文**  
随机森林结果也通过将训练集/测试集划分由 80/20 改为 70/30，并重新通过网格搜索选择参数进行检验。评价指标和因素重要性模式基本一致，进一步确认随机森林分析结论稳健。

---

## 6 Conclusions / 结论

**EN**  
Multiple unfavorable factors, including cost disturbances, supply-demand imbalances, and external shocks, are posing escalating threats to global food security. To clarify risk spillovers in international staple food markets, this study adopts a dual perspective across grains and across timescales, and further examines how these spillovers are shaped by price-driven factors, external uncertainties, and core supply-demand indicators.

**中文**  
成本扰动、供需失衡和外部冲击等多重不利因素正对全球粮食安全构成不断升级的威胁。为阐明国际主粮市场中的风险溢出，本文采用跨粮食品种和跨时间尺度的双重视角，并进一步考察价格驱动因素、外部不确定性和核心供需指标如何塑造这些溢出。

**EN**  
The decomposition-reconstruction results show that intrinsic modes correspond to short-, medium-, and long-term scales, and that shorter timescale components are more volatile. Futures components are generally more volatile than spot components. The similarity of mode groupings across the four grains reflects common features of international staple food markets.

**中文**  
分解—重构结果显示，本征模态对应短期、中期和长期尺度，且时间尺度越短的成分波动性越强。期货成分通常比现货成分更为波动。四种粮食模态分组的相似性反映了国际主粮市场的共性。

**EN**  
The $R^{2}$ decomposed connectedness approach identifies two main spillover patterns: across grains at the same timescale and across timescales within the same grain. Static and dynamic analyses confirm significant risk transmission in global food markets. Soybean, maize, and wheat are important transmitters and receivers in cross-grain spillovers, while rice has much weaker spillovers due to lower internationalization and higher self-sufficiency among major consumers.

**中文**  
$R^{2}$ 分解连通性方法识别出两类主要溢出模式：相同时间尺度下的跨粮食品种溢出，以及同一粮食品种内部的跨时间尺度溢出。静态和动态分析均确认全球粮食市场存在显著风险传导。在跨粮食品种溢出中，大豆、玉米和小麦是重要输出者和接收者，而稻米由于国际化程度较低、主要消费国自给率较高，溢出效应较弱。

**EN**  
Random forest analysis shows that risk spillovers are significantly influenced by price drivers, external uncertainties, and supply-demand indicators. ARMI and FPI are central to short-term spillovers; ES and CONS are important for medium-term spillovers; and long-term spillovers are affected by a broader set of factors including EPU, CPU, BDI, EPI, and ARMI.

**中文**  
随机森林分析表明，风险溢出受到价格驱动因素、外部不确定性和供需指标的显著影响。ARMI 和 FPI 对短期溢出最为关键；ES 和 CONS 对中期溢出很重要；长期溢出则受到更广泛因素影响，包括 EPU、CPU、BDI、EPI 和 ARMI。

**EN**  
The study suggests that policymakers and market participants should monitor multidimensional risk transmission across grains and timescales, improve early-warning systems for food market risk, and adopt context-specific strategies to mitigate excessive food price volatility and cascading effects on food security.

**中文**  
本文建议政策制定者和市场参与者关注跨粮食品种和跨时间尺度的多维风险传导，完善食品市场风险早期预警系统，并采取因地制宜的策略，以缓解过度粮价波动及其对粮食安全的级联影响。

---

## Acknowledgment / 致谢

**EN**  
This work was supported by the National Natural Science Foundation of China, the China Scholarship Council, the Fundamental Research Funds for the Central Universities, and related central-university development programs.

**中文**  
本研究得到国家自然科学基金、中国国家留学基金委、中央高校基本科研业务费及相关中央高校发展项目支持。

## Data availability / 数据可得性

**EN**  
The price data are obtained from Wind and the International Grains Council, while influencing-factor data come from sources including the Policy Uncertainty website, EM-DAT, the IMF, and FAOSTAT.

**中文**  
价格数据来自 Wind 和国际谷物理事会，影响因素数据来自政策不确定性网站、EM-DAT、IMF 和 FAOSTAT 等来源。

## Appendix A / 附录 A

**EN**  
Appendix A contains decomposition results for wheat spot, maize futures, maize spot, soybean futures, soybean spot, rice futures, and rice spot returns.

**中文**  
附录 A 包含小麦现货、玉米期货、玉米现货、大豆期货、大豆现货、稻米期货和稻米现货收益率的分解结果。

# Multiscale risk spillovers and external driving factors: Evidence from the global futures and spot markets of staple foods
# 多尺度风险溢出与外部驱动因素：来自全球主粮期货与现货市场的证据

> 说明：这是基于用户上传论文 Markdown 生成的中英对照核心阅读版。正文按原文逻辑逐段翻译，保留论文结构、主要段落、公式位置、图表题名和表注；大型数值表未逐格翻译，建议与原文表格配合使用。

## Abstract / 摘要

**EN**  
Stable and efficient food markets are crucial for global food security, yet international staple food markets are increasingly exposed to complex risks, including intensified risk contagion and escalating external uncertainties. This paper systematically investigates risk spillovers in global staple food markets and explores the key determinants of these spillover effects, combining innovative decomposition-reconstruction techniques, risk connectedness analysis, and random forest models. The findings reveal that short-term components exhibit the highest volatility, with futures components generally more volatile than spot components. Further analysis identifies two main risk transmission patterns, namely cross-grain and cross-timescale transmission, and clarifies the distinct roles of each component in various net risk spillover networks. Additionally, price drivers, external uncertainties, and core supply-demand indicators significantly influence these spillover effects, with heterogeneous importance of varying factors in explaining different risk spillovers. This study provides valuable insights into the risk dynamics of staple food markets, offers evidence-based guidance for policymakers and market participants to enhance risk warning and mitigation efforts, and supports the stabilization of international food markets and the safeguarding of global food security.

**中文**  
稳定而高效的粮食市场对全球粮食安全至关重要。然而，国际主粮市场正越来越多地暴露于复杂风险之中，包括风险传染加剧和外部不确定性上升。本文结合创新性的分解—重构技术、风险连通性分析与随机森林模型，系统考察全球主粮市场的风险溢出，并探究这些溢出效应的关键决定因素。研究发现，短期成分波动性最高，且期货成分通常比现货成分更为波动。进一步分析识别出两种主要风险传导模式，即跨粮食品种传导和跨时间尺度传导，并阐明了各成分在不同净风险溢出网络中的差异化作用。此外，价格驱动因素、外部不确定性和核心供需指标会显著影响这些溢出效应，不同因素对不同风险溢出的解释重要性也存在异质性。本文为理解主粮市场风险动态提供了有价值的洞见，也为政策制定者和市场参与者加强风险预警与缓释提供了经验证据，并有助于稳定国际粮食市场、维护全球粮食安全。

**Keywords / 关键词**  
Staple food; Risk spillover; ICEEMDAN; $R^{2}$ decomposed connectedness; Random forest model  
主粮；风险溢出；ICEEMDAN；$R^{2}$ 分解连通性；随机森林模型

---

## 1 Introduction / 引言

**EN**  
Food is the cornerstone of national stability and the foundation of human survival. However, global and local food security is becoming increasingly precarious, with numerous nations and regions grappling with mounting risks and challenges. According to The State of Food Security and Nutrition in the World 2024, an estimated 9.1% of the global population remained undernourished in 2023, and approximately 2.33 billion people experienced moderate or severe food insecurity. The report underscores the intensifying severity of key challenges, including armed conflicts, extreme weather events, and economic slowdowns. Furthermore, persistent structural issues, such as increasing food costs, heightened food price volatility, and pronounced regional imbalances in supply and demand, exacerbate the current food crisis.

**中文**  
粮食是国家稳定的基石，也是人类生存的基础。然而，全球和地方层面的粮食安全正变得愈发脆弱，许多国家和地区都在应对持续上升的风险与挑战。根据《2024年世界粮食安全和营养状况》，2023 年全球约 9.1% 的人口仍处于营养不足状态，约 23.3 亿人经历了中度或重度粮食不安全。该报告强调，武装冲突、极端天气事件和经济放缓等关键挑战日益严峻。此外，粮食成本上升、粮价波动加剧以及供需区域失衡突出等持续性结构问题，也进一步加深了当前粮食危机。

**EN**  
Addressing global food insecurity has thus become an urgent priority, with the stability and efficiency of food markets playing a pivotal role. Futures and spot markets for agricultural commodities are critical components of the global food system. They facilitate global food trade and production through price discovery and risk management functions while simultaneously influencing food security through resource allocation and transmission of external shocks. Futures prices reflect market expectations of future supply and demand conditions, whereas spot prices directly represent current market conditions.

**中文**  
因此，应对全球粮食不安全已成为紧迫任务，而粮食市场的稳定性和效率在其中具有关键作用。农产品期货市场和现货市场是全球粮食体系的重要组成部分。它们通过价格发现和风险管理功能促进全球粮食贸易与生产，同时又通过资源配置和外部冲击传导影响粮食安全。期货价格反映市场对未来供需状况的预期，而现货价格直接反映当前市场状况。

**EN**  
A critical concern lies in developing a comprehensive understanding of how risks transmit within international staple crop markets, spanning food futures and spots, across different commodities, and over varying timescales. These spillover effects may magnify market instability, disrupt supply chains, and increase uncertainties for producers, traders, and policymakers. External shocks and internal drivers, such as climate policy uncertainty, energy prices, and transportation costs, may further exacerbate these risk spillover effects.

**中文**  
一个关键问题在于，需要全面理解风险如何在国际主粮市场内部传导：这种传导既可能跨越粮食期货与现货市场，也可能跨越不同商品，并在不同时间尺度上发生。这些溢出效应可能放大市场不稳定性、扰乱供应链，并增加生产者、贸易商和政策制定者面对的不确定性。气候政策不确定性、能源价格和运输成本等外部冲击与内部驱动因素，也可能进一步加剧这些风险溢出效应。

**EN**  
This paper systematically investigates risk contagion within the international food market and identifies the underlying determinants of spillover effects. By employing a novel decomposition-reconstruction methodology, futures and spot returns of wheat, maize, soybean, and rice are decomposed into short-, medium-, and long-term components. Risk connectedness analysis uncovers two main patterns of risk transmission: stronger spillovers occur between same-timescale components of different grains and between same-grain components at different timescales. Both static and dynamic analyses consistently demonstrate significant and robust cross-grain and cross-timescale spillovers.

**中文**  
本文系统考察国际粮食市场内部的风险传染，并识别溢出效应背后的决定因素。通过采用新的分解—重构方法，本文将小麦、玉米、大豆和稻米的期货与现货收益率分解为短期、中期和长期成分。风险连通性分析揭示了两类主要风险传导模式：不同粮食品种相同时间尺度成分之间存在较强溢出，同一粮食品种不同时间尺度成分之间也存在较强溢出。静态和动态分析均一致表明，跨粮食品种和跨时间尺度的风险溢出显著且稳健。

**EN**  
From a dual perspective of cross-grain and cross-timescale, this study utilizes advanced and integrative methods to clarify the mechanisms of risk transmission and identify critical drivers of risk spillovers in the global staple food market. Unlike previous research, which predominantly relies on original prices or returns, this paper introduces decomposition and reconstruction techniques to reveal the intrinsic characteristics of grain futures and spot returns, thereby proposing a new analytical framework for examining risk contagion across multiple dimensions.

**中文**  
本文从跨粮食品种和跨时间尺度两个视角出发，利用较为先进且整合性的研究方法，阐明全球主粮市场中的风险传导机制，并识别风险溢出的关键驱动因素。不同于以往主要依赖原始价格或收益率的研究，本文引入分解与重构技术，以揭示粮食期货与现货收益率的内在特征，并据此提出一个考察多维风险传染的新分析框架。

---

## 2 Literature review / 文献综述

**EN**  
Risk transmission across financial markets or assets, often referred to as risk spillover, has attracted substantial academic attention. With globalization and financial market integration deepening, localized risk events can propagate rapidly through different channels and may trigger systemic financial crises. The 2008 global financial crisis and the COVID-19 pandemic highlight the importance of understanding risk spillover effects.

**中文**  
金融市场或资产之间的风险传导通常被称为风险溢出，已引起学界广泛关注。随着全球化和金融市场一体化加深，局部风险事件可以通过不同渠道迅速传播，并可能引发系统性金融危机。2008 年全球金融危机和新冠疫情凸显了理解风险溢出效应的重要性。

**EN**  
Risk spillover measurement has evolved from traditional linear analysis to dynamic modeling. Early studies relied on Granger causality tests and linear regression models, but these methods struggled to capture asymmetric, nonlinear, and dynamic risk transmission relationships. Advanced methods such as CoVaR and dynamic connectedness frameworks were therefore developed. CoVaR focuses on tail risk and bilateral dependence, while the generalized connectedness framework can capture risk transmission dynamics across multiple time series simultaneously.

**中文**  
风险溢出测度方法已经从传统线性分析逐步发展到动态建模。早期研究主要依赖格兰杰因果检验和线性回归模型，但这些方法难以捕捉非对称、非线性以及动态风险传导关系。因此，CoVaR 和动态连通性框架等更先进的方法被提出。CoVaR 关注尾部风险和双边依赖，而广义连通性框架能够同时刻画多个时间序列之间的风险传导动态。

**EN**  
The connectedness method uses generalized forecast error variance decomposition within vector autoregressive models to construct total and directional spillover indices. It has been widely used in multi-asset and cross-market studies. Later extensions include frequency-domain connectedness, high-dimensional connectedness based on sparse networks, and the $R^{2}$ decomposed connectedness approach, which improves interpretability and avoids biases caused by certain standardization procedures.

**中文**  
连通性方法利用向量自回归模型中的广义预测误差方差分解，构建总溢出指数和方向性溢出指数。该方法已广泛用于多资产和跨市场研究。后续扩展包括频域连通性、基于稀疏网络的高维连通性，以及 $R^{2}$ 分解连通性方法。后者增强了模型解释性，并避免了某些标准化处理可能带来的偏差。

**EN**  
The increasing financialization of commodities has heightened price volatility and market linkages in agricultural markets. Given the role of agricultural markets in global food security, risk spillovers in these markets have become increasingly important. Existing studies show that energy market spillovers can significantly increase risk exposure in agricultural markets, and that agricultural futures are particularly susceptible to shocks during turbulent periods.

**中文**  
商品金融化程度提升增强了农业市场的价格波动和市场联动。鉴于农业市场在全球粮食安全中的作用，农业市场风险溢出研究变得越来越重要。现有研究表明，能源市场溢出会显著增加农业市场的风险暴露，且农产品期货在动荡时期尤其容易受到冲击影响。

**EN**  
A smaller body of literature explores drivers of food price volatility, including biofuel demand, climate-induced yield reductions, energy price hikes, declining inventories, export restrictions, supply-demand fundamentals, policy changes, oil price volatility, geopolitical risks, and extreme events such as the COVID-19 pandemic and the Russia-Ukraine conflict.

**中文**  
另有少量文献探讨食品价格波动的驱动因素，包括生物燃料需求、气候导致的减产、能源价格上涨、库存下降、出口限制、供需基本面、政策变化、油价波动、地缘政治风险，以及新冠疫情和俄乌冲突等极端事件。

**EN**  
However, several gaps remain. First, risk transmission across grain markets at different timescales remains underexplored. Second, the ability of potential drivers to explain different dimensions of risk spillovers and their relative importance has received limited attention. This study addresses these gaps by examining risk contagion in international staple food markets from both cross-grain and cross-timescale perspectives.

**中文**  
然而，现有研究仍存在若干空白。首先，不同时间尺度下粮食市场之间的风险传导研究仍不充分。其次，潜在驱动因素解释不同维度风险溢出的能力及其相对重要性尚未得到足够关注。本文通过从跨粮食品种和跨时间尺度两个视角考察国际主粮市场中的风险传染，试图弥补这些不足。

---

## 3 Methodology / 研究方法

### 3.1 Empirical mode decomposition / 经验模态分解

**EN**  
Empirical mode decomposition (EMD) is a signal decomposition method designed for nonlinear and non-stationary data. Unlike wavelet or Fourier decomposition, which rely on predefined basis functions, EMD adapts to the intrinsic timescale features of the data and is therefore theoretically applicable to many types of signals.

**中文**  
经验模态分解（EMD）是一种用于处理非线性和非平稳数据的信号分解方法。不同于依赖预设基函数的小波分解或傅里叶分解，EMD 能够适应数据自身的内在时间尺度特征，因此在理论上适用于多种类型的信号。

**EN**  
The core concept behind EMD is the Hilbert-Huang Transform. The original time series is extracted step by step according to different time periods, producing several data sequences with distinct characteristic scales. Each sequence can be regarded as an intrinsic mode function (IMF). An IMF must satisfy two conditions: the number of extrema and zero crossings must be equal or differ by at most one, and the mean of the upper and lower envelopes must be zero at any time.

**中文**  
EMD 的核心思想来自 Hilbert-Huang 变换。该方法按照不同时间周期逐步提取原始时间序列，从而生成若干具有不同特征尺度的数据序列。每个序列可视为一个本征模态函数（IMF）。IMF 需要满足两个条件：极值点数量与过零点数量相等或最多相差一个；任意时刻上、下包络线的均值为零。

**EN**  
A complex time series $x(t)$ can be decomposed into multiple IMFs and a residue through sifting:

$$
x(t)=\sum_{n=1}^{N}c_{n}(t)+u(t),\quad t=1,\dots,T.
$$

Here, $N$ is the number of IMFs, $c_n$ is the $n$-th IMF, and $u(t)$ is the residue. This study uses cubic spline interpolation because it provides smoother envelope curves than Hermite interpolation.

**中文**  
复杂时间序列 $x(t)$ 可通过筛分过程分解为多个 IMF 和一个残差项：
$$
x(t)=\sum_{n=1}^{N}c_{n}(t)+u(t),\quad t=1,\dots,T.
$$

其中，$N$ 为 IMF 数量，$c_n$ 为第 $n$ 个 IMF，$u(t)$ 为残差项。本文采用三次样条插值，因为其包络曲线通常比 Hermite 插值更平滑。

**EN**  
Although EMD has advantages, it also faces problems such as mode mixing, stopping criteria, and end effects. To address these issues, this paper applies ICEEMDAN, an improved complete ensemble EMD with adaptive noise. ICEEMDAN adds adaptive white-noise components, computes local envelope means, and obtains IMFs sequentially, thereby reducing residual noise and reconstruction error.

**中文**  
尽管 EMD 具有优势，但也面临模态混叠、停止准则设定和端点效应等问题。为解决这些问题，本文采用 ICEEMDAN，即改进的自适应噪声完备集合经验模态分解。ICEEMDAN 通过加入自适应白噪声成分、计算局部包络均值并按顺序提取 IMF，降低残余噪声和重构误差。

### 3.2 Mode reconstruction method / 模态重构方法

**EN**  
After decomposing the data into IMFs and a residual term, the paper improves the KMC-RLN reconstruction method and proposes a GMM-RLN method. The run-length number is an indicator of volatility: higher run-length values imply greater volatility. Each IMF is transformed into a symbolic sequence around its mean, and consecutive identical symbols are counted as runs.

**中文**  
在将数据分解为 IMF 和残差项之后，本文改进了 KMC-RLN 重构方法，并提出 GMM-RLN 方法。游程数是衡量波动性的指标：游程数越高，表示波动性越强。每个 IMF 会根据其均值转化为符号序列，连续相同符号被计为一个游程。

**EN**  
The Gaussian mixture model is then used for clustering these run-length numbers. Compared with existing reconstruction methods, GMM-RLN considers both data fluctuation characteristics and data length, and is more flexible when cluster boundaries are fuzzy. The number of clusters is set to 3, corresponding to short-term high-frequency, medium-term medium-frequency, and long-term low-frequency components.

**中文**  
随后，本文使用高斯混合模型对这些游程数进行聚类。与既有重构方法相比，GMM-RLN 同时考虑数据波动特征和数据长度，并且在聚类边界模糊时具有更高灵活性。本文将聚类数量设为 3，对应短期高频成分、中期中频成分和长期低频成分。

### 3.3 $R^{2}$ decomposed connectedness approach / $R^{2}$ 分解连通性方法

**EN**  
The paper uses the $R^{2}$ decomposed connectedness approach to measure risk transmission. A VAR model is represented in its VMA form, and generalized forecast error variance decomposition is used to quantify directional spillovers. Under random-walk assumptions, GFEVD can be simplified into a squared correlation term, equivalent to an $R^{2}$ measure from a bivariate regression.

**中文**  
本文使用 $R^{2}$ 分解连通性方法衡量风险传导。首先将 VAR 模型表示为 VMA 形式，并利用广义预测误差方差分解度量方向性溢出。在随机游走假设下，GFEVD 可简化为平方相关项，等价于双变量回归中的 $R^{2}$ 指标。

**EN**  
Instead of normalizing GFEVD row sums, the $R^{2}$ decomposed connectedness approach uses multivariate regression and principal component analysis to decompose the $R^{2}$ contribution of each explanatory variable. The main indices include $TO_i$, $FROM_i$, $NET_i$, $NPDC_{ij}$, and $TCI$.

**中文**  
与直接对 GFEVD 行和进行标准化不同，$R^{2}$ 分解连通性方法使用多元回归和主成分分析，分解各解释变量对 $R^{2}$ 的贡献。主要指标包括 $TO_i$、$FROM_i$、$NET_i$、$NPDC_{ij}$ 和 $TCI$。

**Formula / 公式**  
$$
TO_i=\sum_{j=1}^{k}R_{ji}^{2G},\quad FROM_i=\sum_{j=1}^{k}R_{ij}^{2G},\quad NET_i=TO_i-FROM_i,
$$
$$
NPDC_{ij}=R_{ij}^{2G}-R_{ji}^{2G},\quad TCI=\frac{1}{k}\sum_{i=1}^{k}R_i^2.
$$

**EN**  
A positive $NET_i$ indicates that variable $i$ is a net risk transmitter, while a negative value indicates that it is a net risk receiver. The TCI measures the average risk spillover in the network and serves as a proxy for market risk.

**中文**  
$NET_i$ 为正表示变量 $i$ 是风险净输出者，为负则表示其为风险净接收者。TCI 衡量网络中的平均风险溢出水平，可作为市场风险的代理指标。

### 3.4 Random forest model / 随机森林模型

**EN**  
Random forest is a non-parametric method for classification and regression. It combines multiple decision trees, averages their predictions in regression problems, and is suitable for complex datasets because it can capture nonlinear relationships and resist noise, missing data, and overfitting.

**中文**  
随机森林是一种可用于分类和回归的非参数方法。它组合多棵决策树，并在回归问题中对各树预测结果取平均。由于能够捕捉非线性关系，并且对噪声、缺失数据和过拟合具有较强鲁棒性，随机森林适合处理复杂数据集。

**Formula / 公式**  
$$
Y=\frac{1}{K}\sum_{k=1}^{K}f_k(x),\quad
MAE=\frac{1}{Q}\sum_{q=1}^{Q}|y_q-\hat y_q|,\quad
MSE=\frac{1}{Q}\sum_{q=1}^{Q}(y_q-\hat y_q)^2.
$$

**EN**  
The paper applies random forest to examine the relationship between each risk-spillover network’s TCI and a series of explanatory variables. The dataset is split into 80% training and 20% testing, and grid search is used to tune hyperparameters such as the number of trees, maximum tree depth, and number of features used for splitting.

**中文**  
本文使用随机森林考察各风险溢出网络的 TCI 与一系列解释变量之间的关系。数据集被划分为 80% 训练集和 20% 测试集，并通过网格搜索调节超参数，如决策树数量、最大树深度和用于分裂的特征数量。

---

## 4 Data description / 数据说明

### 4.1 Data sources / 数据来源

**EN**  
The study focuses on wheat, maize, soybean, and rice. It obtains daily closing prices of continuous futures contracts for wheat, corn, soybean, and rough rice traded on CBOT from Wind, and daily price indices for wheat, maize, soybean, and rice from the International Grains Council. CBOT futures prices serve as global agricultural pricing benchmarks, while IGC indices reflect spot export quotations from major producers. The sample period runs from January 3, 2000, to December 29, 2023.

**中文**  
本文聚焦小麦、玉米、大豆和稻米四种主粮。研究从 Wind 获取 CBOT 交易的小麦、玉米、大豆和糙米期货连续合约日收盘价，并从国际谷物理事会获取小麦、玉米、大豆和稻米的日价格指数。CBOT 期货价格可视为全球农产品定价基准，而 IGC 指数反映主要生产国现货出口报价。样本期为 2000 年 1 月 3 日至 2023 年 12 月 29 日。

**EN**  
Twelve explanatory variables are selected: ARMI, FPI, EPI, BDI, GPR, EPU, CPU, GND, PROD, IMP, CONS, and ES. They cover price-driven factors, external shock factors, and core supply-demand indicators. BDI and GPR are daily; ARMI, FPI, EPI, EPU, CPU, and GND are monthly; and PROD, IMP, CONS, and ES are annual. Forward filling is used for data alignment.

**中文**  
本文选择 12 个解释变量：ARMI、FPI、EPI、BDI、GPR、EPU、CPU、GND、PROD、IMP、CONS 和 ES。这些变量覆盖价格驱动因素、外部冲击因素和核心供需指标。其中 BDI 和 GPR 为日度数据；ARMI、FPI、EPI、EPU、CPU 和 GND 为月度数据；PROD、IMP、CONS 和 ES 为年度数据。本文使用向前填充进行数据对齐。

### 4.2 Statistical description / 统计描述

**EN**  
Figures 1 and 2 show the evolution of prices and returns for the four staples. Futures and spot prices generally move together and exhibit statistically significant positive correlations. All four staples display notable volatility during the global food crises of 2006-2008, 2010-2012, and the period since 2020. Futures returns fluctuate more than spot returns, and all return series show volatility clustering.

**中文**  
图 1 和图 2 展示了四种主粮价格和收益率的演变。期货与现货价格总体走势一致，并具有统计显著的正相关关系。四种主粮在 2006—2008 年、2010—2012 年以及 2020 年以来的全球粮食危机期间均出现明显波动。期货收益率波动大于现货收益率，所有收益率序列都表现出波动聚集特征。

**EN**  
Table 1 reports descriptive statistics. Futures returns have larger maxima, smaller minima, and higher standard deviations than corresponding spot returns, implying stronger volatility in futures markets. The return distributions are asymmetric and fat-tailed. Jarque-Bera and ADF statistics are significant at the 1% level, indicating non-normality and stationarity.

**中文**  
表 1 报告描述性统计。期货收益率相较对应现货收益率具有更大的最大值、更小的最小值和更高的标准差，说明期货市场波动性更强。收益率分布存在非对称性和厚尾特征。Jarque-Bera 检验和 ADF 检验统计量均在 1% 水平上显著，说明序列不服从正态分布且为平稳序列。

---

## 5 Empirical analysis / 实证分析

### 5.1 Decomposition of grain return series / 粮食收益率序列分解

**EN**  
The ICEEMDAN method decomposes futures and spot return series for the four staple crops. The results for wheat futures are shown in Figure 3, and the other series are shown in Appendix A. IMFs are ordered from high to low frequency, followed by the residue. The series are usually decomposed into 10 or 11 IMFs.

**中文**  
本文使用 ICEEMDAN 方法分解四种主粮的期货和现货收益率序列。小麦期货结果见图 3，其他序列结果见附录 A。IMF 按照频率从高到低排列，最后为残差项。收益率序列通常被分解为 10 个或 11 个 IMF。

**EN**  
For each decomposed mode, the paper computes the mean period, Spearman correlation with the original series, and variance contribution. The results show that IMF mean periods increase gradually, while correlation and importance generally decrease with IMF order. IMF1 contributes the most to volatility, whereas the residue contributes very little.

**中文**  
对于每个分解模态，本文计算平均周期、与原始序列的 Spearman 相关系数以及方差贡献。结果显示，IMF 平均周期逐渐增加，而相关性和重要性通常随 IMF 阶数上升而下降。IMF1 对波动贡献最大，残差项贡献很小。

### 5.2 Reconstruction of grain return series / 粮食收益率序列重构

**EN**  
Using GMM-RLN, the decomposed IMFs are reconstructed into short-term, medium-term, and long-term components. IMF1 and IMF2 are grouped as short-term components; IMF3, IMF4, and IMF5 are grouped as medium-term components; IMF6 and the remaining longer IMFs are grouped as long-term components.

**中文**  
使用 GMM-RLN 方法后，分解得到的 IMF 被重构为短期、中期和长期成分。IMF1 与 IMF2 被划分为短期成分；IMF3、IMF4 和 IMF5 被划分为中期成分；IMF6 及其余更长期 IMF 被划分为长期成分。

**EN**  
Short-term components have an average period ceiling of about five working days, medium-term components about 44 working days, and long-term components up to about 3,021 working days. Short-term components fluctuate the most, followed by medium-term components, while long-term components fluctuate the least. Futures components are generally more volatile than spot components.

**中文**  
短期成分平均周期上限约为 5 个工作日，中期成分约为 44 个工作日，长期成分最长约为 3021 个工作日。短期成分波动最大，其次为中期成分，长期成分波动最小。期货成分通常比现货成分波动更强。

**EN**  
The reconstructed components show violent fluctuations during major crisis periods, including the 2006-2008 food crisis, the 2008 global financial crisis, the 2010-2012 food crisis, and the post-2020 food crisis triggered by COVID-19, extreme weather, and regional conflicts.

**中文**  
重构成分在若干重大危机期间出现剧烈波动，包括 2006—2008 年粮食危机、2008 年全球金融危机、2010—2012 年粮食危机，以及 2020 年后由新冠疫情、极端天气和地区冲突触发的粮食危机。

### 5.3 Static analysis of risk spillovers / 风险溢出的静态分析

**EN**  
After reconstructing all components, the paper uses the $R^{2}$ decomposed connectedness approach to calculate full-sample risk connectedness. Figure 5 reveals two major spillover patterns. First, stronger spillovers occur among same-timescale components across different grains. Second, significant spillovers also occur among different-timescale components within the same grain.

**中文**  
重构所有成分后，本文使用 $R^{2}$ 分解连通性方法计算全样本风险连通性。图 5 揭示了两类主要溢出模式。第一，不同粮食品种相同时间尺度成分之间存在更强溢出。第二，同一粮食品种不同时间尺度成分之间也存在显著溢出。

**EN**  
Table 4 shows that the TCI values for same-timescale components are large, indicating significant cross-grain spillovers. Soybean contributes most to short-term spillovers, followed by maize and wheat. Rice contributes little, which is related to its lower internationalization, limited futures trading volume, low market liquidity, and stable production-consumption structure.

**中文**  
表 4 显示，相同时间尺度成分的 TCI 值较高，说明跨粮食品种风险溢出显著。大豆对短期溢出贡献最大，其后为玉米和小麦。稻米贡献较小，这与其国际化程度较低、期货交易量有限、市场流动性较低以及生产消费结构较稳定有关。

**EN**  
Table 5 shows static spillovers across different timescales within each grain. The soybean market has the highest TCI, followed by wheat, maize, and rice. For wheat, maize, and soybean, short-term components contribute most to spillovers; for rice, long-term components contribute the most, although overall spillovers remain low.

**中文**  
表 5 展示了每种粮食品种内部不同时间尺度成分之间的静态溢出。大豆市场 TCI 最高，其后为小麦、玉米和稻米。对于小麦、玉米和大豆，短期成分对溢出的贡献最大；对于稻米，长期成分贡献最大，但整体溢出水平仍较低。

### 5.4 Dynamic analysis of risk spillovers / 风险溢出的动态分析

**EN**  
The dynamic analysis uses a one-year rolling window. Dynamic average TCIs are higher than static TCIs, suggesting that risk spillovers are more pronounced dynamically. Long-term components show especially high dynamic connectedness, possibly because long-term risk spillovers last longer within rolling windows.

**中文**  
动态分析采用一年滚动窗口。动态平均 TCI 高于静态 TCI，说明动态情形下风险溢出更为明显。长期成分的动态连通性尤其高，可能是因为长期风险溢出在滚动窗口内持续时间更长。

**EN**  
Across short-, medium-, and long-term components, soybean is the main risk transmitter and receiver in global staple crop markets, followed by maize and wheat, while rice has the weakest effect. In the long-term component network, soybean and maize act as net risk transmitters, while rice futures and spot act as net risk receivers.

**中文**  
综合短期、中期和长期成分来看，大豆是全球主粮市场中最主要的风险输出者和接收者，其后为玉米和小麦，稻米作用最弱。在长期成分网络中，大豆和玉米是风险净输出者，而稻米期货和现货是风险净接收者。

**EN**  
The dynamic TCI series show elevated spillovers during major crises, including the 2006 global food crisis, the 2008 global financial crisis, the 2012 global food crisis, and the food crisis since 2020. In recent years, medium- and long-term spillovers have shown a clear upward trend.

**中文**  
动态 TCI 序列显示，在重大危机期间风险溢出显著上升，包括 2006 年全球粮食危机、2008 年全球金融危机、2012 年全球粮食危机以及 2020 年以来的粮食危机。近年来，中期和长期溢出呈明显上升趋势。

**EN**  
Net risk spillover networks show that maize futures and wheat futures are the main risk transmitters among short-term components. The largest spillover paths are from wheat futures to wheat spot and from maize futures to maize spot, confirming substantial transmission from agricultural futures markets to corresponding spot markets.

**中文**  
净风险溢出网络显示，玉米期货和小麦期货是短期成分中的主要风险输出者。最大溢出路径分别是小麦期货到小麦现货、玉米期货到玉米现货，说明农产品期货市场向对应现货市场存在显著风险传导。

**EN**  
For cross-timescale spillovers, short-term components dominate internal risk transmission in soybean, maize, and wheat markets, while long-term components dominate in the rice market. Net spillover networks further show that the rice market has a distinct transmission pattern compared with the other three staple crops.

**中文**  
对于跨时间尺度溢出，短期成分主导大豆、玉米和小麦市场内部的风险传导，而长期成分主导稻米市场内部传导。净溢出网络进一步表明，稻米市场的传导模式与其他三类主粮市场不同。

### 5.5 Factors influencing risk spillovers / 风险溢出的影响因素

**EN**  
After identifying significant cross-grain and cross-timescale spillovers, the paper explores their drivers using random forest regression. Twelve explanatory variables are selected: ARMI, FPI, EPI, BDI, GPR, EPU, CPU, GND, PROD, IMP, CONS, and ES. These variables cover supply, demand, production, transportation, and external uncertainties.

**中文**  
在识别出显著跨粮食品种和跨时间尺度溢出后，本文使用随机森林回归探究其驱动因素。选取的十二个解释变量包括 ARMI、FPI、EPI、BDI、GPR、EPU、CPU、GND、PROD、IMP、CONS 和 ES，覆盖供给、需求、生产、运输和外部不确定性等方面。

**EN**  
The random forest model fits the training and test data well. The small MAE and MSE values indicate that the selected variables effectively explain variation in TCI. These drivers can therefore serve as potential early-warning indicators for systemic risks in the global food system.

**中文**  
随机森林模型在训练集和测试集上均拟合良好。较小的 MAE 和 MSE 说明所选变量能够有效解释 TCI 的变化。因此，这些驱动因素可作为全球粮食系统系统性风险的潜在早期预警指标。

**EN**  
For short-term components, ARMI and FPI are the two most important explanatory variables. ARMI reflects upstream agricultural input costs, while FPI reflects global food price dynamics and consumer-side market pressure. Together, they capture market dynamics from production and consumption price dimensions.

**中文**  
对于短期成分，ARMI 和 FPI 是最重要的两个解释变量。ARMI 反映上游农业投入成本，FPI 反映全球食品价格动态和消费端市场压力。两者共同从生产端和消费端价格维度刻画市场动态。

**EN**  
For medium-term components, ES and CONS also become important. ES reflects supply security and reserve capacity, while CONS represents actual grain usage and market demand. Thus, medium-term spillovers are driven by both price dynamics and supply-demand quantities.

**中文**  
对于中期成分，ES 和 CONS 也变得重要。ES 反映供给安全和储备能力，CONS 表示实际粮食使用量和市场需求。因此，中期溢出同时受到价格动态和供需数量因素驱动。

**EN**  
For long-term components, EPU, BDI, EPI, ARMI, and CPU play important roles. This indicates that long-term spillovers are shaped by a broader set of factors, including economic policy uncertainty, climate policy uncertainty, energy prices, production costs, and transportation costs.

**中文**  
对于长期成分，EPU、BDI、EPI、ARMI 和 CPU 发挥重要作用。这说明长期溢出由更广泛的因素塑造，包括经济政策不确定性、气候政策不确定性、能源价格、生产成本和运输成本。

**EN**  
For cross-timescale spillovers within each grain market, FPI, ARMI, and EPI consistently show high importance. ES strongly affects spillovers within wheat, maize, and soybean markets, but has limited impact on rice because rice production and consumption are regionally concentrated and many major producers intervene to stabilize domestic supply and prices.

**中文**  
对于各粮食品种市场内部的跨时间尺度溢出，FPI、ARMI 和 EPI 始终具有较高重要性。ES 显著影响小麦、玉米和大豆市场内部溢出，但对稻米影响有限，因为稻米生产和消费具有区域集中性，且许多主要生产国会采取政策干预以稳定国内供应和价格。

**EN**  
BDI is particularly important for wheat and rice spillovers. Wheat and rice are often transported as bulk commodities, and their supply chains are less flexible. By contrast, maize and soybean have more flexible transportation modes, storage infrastructure, and end-use substitution possibilities, making them less sensitive to spot transportation cost changes.

**中文**  
BDI 对小麦和稻米溢出尤其重要。小麦和稻米通常以散货形式运输，供应链灵活性较低。相比之下，玉米和大豆具有更灵活的运输方式、储藏基础设施和终端用途替代可能性，因此对现货运输成本变化的敏感性较低。

### 5.6 Robustness checks / 稳健性检验

**EN**  
The paper checks robustness by changing the rolling window length from 252 trading days to 200 and 300 trading days. The resulting TCIs show only minor numerical differences and highly consistent trends, suggesting that the dynamic spillover results are not sensitive to window-length choice.

**中文**  
本文通过将滚动窗口长度从 252 个交易日改为 200 个和 300 个交易日进行稳健性检验。得到的 TCI 仅存在较小数值差异，整体趋势高度一致，说明动态溢出结果对窗口长度选择并不敏感。

**EN**  
The random forest results are also checked by changing the train-test split from 80/20 to 70/30 and reselecting parameters through grid search. The evaluation metrics and factor-importance patterns remain broadly consistent, confirming the robustness of the random forest findings.

**中文**  
随机森林结果也通过将训练集/测试集划分由 80/20 改为 70/30，并重新通过网格搜索选择参数进行检验。评价指标和因素重要性模式基本一致，进一步确认随机森林分析结论稳健。

---

## 6 Conclusions / 结论

**EN**  
Multiple unfavorable factors, including cost disturbances, supply-demand imbalances, and external shocks, are posing escalating threats to global food security. To clarify risk spillovers in international staple food markets, this study adopts a dual perspective across grains and across timescales, and further examines how these spillovers are shaped by price-driven factors, external uncertainties, and core supply-demand indicators.

**中文**  
成本扰动、供需失衡和外部冲击等多重不利因素正对全球粮食安全构成不断升级的威胁。为阐明国际主粮市场中的风险溢出，本文采用跨粮食品种和跨时间尺度的双重视角，并进一步考察价格驱动因素、外部不确定性和核心供需指标如何塑造这些溢出。

**EN**  
The decomposition-reconstruction results show that intrinsic modes correspond to short-, medium-, and long-term scales, and that shorter timescale components are more volatile. Futures components are generally more volatile than spot components. The similarity of mode groupings across the four grains reflects common features of international staple food markets.

**中文**  
分解—重构结果显示，本征模态对应短期、中期和长期尺度，且时间尺度越短的成分波动性越强。期货成分通常比现货成分更为波动。四种粮食模态分组的相似性反映了国际主粮市场的共性。

**EN**  
The $R^{2}$ decomposed connectedness approach identifies two main spillover patterns: across grains at the same timescale and across timescales within the same grain. Static and dynamic analyses confirm significant risk transmission in global food markets. Soybean, maize, and wheat are important transmitters and receivers in cross-grain spillovers, while rice has much weaker spillovers due to lower internationalization and higher self-sufficiency among major consumers.

**中文**  
$R^{2}$ 分解连通性方法识别出两类主要溢出模式：相同时间尺度下的跨粮食品种溢出，以及同一粮食品种内部的跨时间尺度溢出。静态和动态分析均确认全球粮食市场存在显著风险传导。在跨粮食品种溢出中，大豆、玉米和小麦是重要输出者和接收者，而稻米由于国际化程度较低、主要消费国自给率较高，溢出效应较弱。

**EN**  
Random forest analysis shows that risk spillovers are significantly influenced by price drivers, external uncertainties, and supply-demand indicators. ARMI and FPI are central to short-term spillovers; ES and CONS are important for medium-term spillovers; and long-term spillovers are affected by a broader set of factors including EPU, CPU, BDI, EPI, and ARMI.

**中文**  
随机森林分析表明，风险溢出受到价格驱动因素、外部不确定性和供需指标的显著影响。ARMI 和 FPI 对短期溢出最为关键；ES 和 CONS 对中期溢出很重要；长期溢出则受到更广泛因素影响，包括 EPU、CPU、BDI、EPI 和 ARMI。

**EN**  
The study suggests that policymakers and market participants should monitor multidimensional risk transmission across grains and timescales, improve early-warning systems for food market risk, and adopt context-specific strategies to mitigate excessive food price volatility and cascading effects on food security.

**中文**  
本文建议政策制定者和市场参与者关注跨粮食品种和跨时间尺度的多维风险传导，完善食品市场风险早期预警系统，并采取因地制宜的策略，以缓解过度粮价波动及其对粮食安全的级联影响。

---

## Acknowledgment / 致谢

**EN**  
This work was supported by the National Natural Science Foundation of China, the China Scholarship Council, the Fundamental Research Funds for the Central Universities, and related central-university development programs.

**中文**  
本研究得到国家自然科学基金、中国国家留学基金委、中央高校基本科研业务费及相关中央高校发展项目支持。

## Data availability / 数据可得性

**EN**  
The price data are obtained from Wind and the International Grains Council, while influencing-factor data come from sources including the Policy Uncertainty website, EM-DAT, the IMF, and FAOSTAT.

**中文**  
价格数据来自 Wind 和国际谷物理事会，影响因素数据来自政策不确定性网站、EM-DAT、IMF 和 FAOSTAT 等来源。

## Appendix A / 附录 A

**EN**  
Appendix A contains decomposition results for wheat spot, maize futures, maize spot, soybean futures, soybean spot, rice futures, and rice spot returns.

**中文**  
附录 A 包含小麦现货、玉米期货、玉米现货、大豆期货、大豆现货、稻米期货和稻米现货收益率的分解结果。
