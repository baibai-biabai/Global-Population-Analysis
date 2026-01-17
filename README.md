# 全球人口演变分析（1950-2023）

## 项目简介

本项目通过对全球人口数据（1950-2023年）的系统分析，揭示了全球人口演变的宏观趋势、区域差异及其核心驱动机制。研究综合运用了数据清洗、探索性数据分析（EDA）和可视化技术，从四个维度深入剖析了全球人口的发展特征：

1. **全球及地区层面的趋势与对比分析**
2. **关键国家/地区的深度案例研究**（特别聚焦中国与印度的人口交替）
3. **生育率的核心驱动作用分析**
4. **城市化水平与人口发展的关联分析**

## 数据来源

本研究基于Kaggle平台提供的"World Population Dataset"，https://www.kaggle.com/datasets/chandanchoudhury/world-population-dataset，整合了三个主要数据源：

1. **世界国家统计数据** (`world_country_stats.csv`) - 234×5
   - 国家、地区、土地面积、生育率、中位年龄
   
2. **2023年人口数据** (`world_population_by_country_2023.csv`) - 234×11
   - 总人口、年变化率、净变化、人口密度、净移民、生育率、中位年龄、城市人口比例等
   
3. **1950-2023时间序列数据** (`world_population_by_year_1950_2023.csv`) - 234×75
   - 1950-2023年逐年人口数量

## 文件结构
    DataAnalysisandVisualization/
    ├── Global Population Analysis.ipynb        # 主分析文件
    ├── world_data_unified_final.csv            # 统一数据集（包含区域、人口结构等）
    ├── world_population_timeseries_checked.csv # 时间序列数据（1950-2023）
    ├── global_population_analysis.csv          # 全球人口分析结果
    ├── regional_population_history.csv         # 各洲历史人口数据
    ├── fertility_analysis_detailed.csv         # 生育率详细分析
    ├── urbanization_analysis_detailed.csv      # 城市化详细分析
    ├── global_population_trend.png             # 全球人口增长趋势图
    ├── regional_population_analysis.png        # 各洲人口分析图
    ├── china_india_comparison.png              # 中印人口对比图
    ├── typical_countries_growth.png            # 典型国家增长趋势图
    ├── top_countries_ranking.png               # 人口大国排名图
    ├── fertility_analysis.png                  # 生育率分析图
    ├── urbanization_analysis_new.png           # 城市化分析图
    └── README.md                               # 本说明文件

## 主要发现

### 1. 全球人口增长趋势
- **总量增长**：全球人口从1950年的24.8亿增长到2023年的80.5亿，增长3.24倍
- **增速放缓**：年均复合增长率从1964年的峰值2.22%降至2023年的0.93%
- **里程碑**：人口在1961年、1975年、1988年、1999年、2011年和2023年分别突破30亿、40亿、50亿、60亿、70亿和80亿大关

### 2. 区域格局变化
- **亚洲主导**：2023年占全球人口的59.09%，但增速放缓
- **非洲崛起**：占比从1950年的9.2%上升至2023年的18.1%，增长潜力最大
- **欧洲萎缩**：占比从1950年的22.1%下降至2023年的9.2%

### 3. 中印人口交替
- **历史性转折**：印度在2023年以14.29亿人口超越中国（14.26亿）
- **结构差异**：印度人口更年轻（中位年龄28.0岁 vs 中国39.0岁），增长动力更强

### 4. 生育率核心作用
- **强相关关系**：生育率与中位年龄呈强负相关（r = -0.853），与增长率呈强正相关（r = 0.710）
- **两极分化**：51.3%的国家生育率低于人口更替水平（2.1），非洲国家生育率普遍高于4.0

### 5. 城市化关联
- **负相关关系**：城市化率与生育率呈负相关（r = -0.415），与中位年龄呈正相关（r = 0.412）
- **发展模式**：识别出"低城市化高增长型"到"高度城市化成熟型"四种典型发展模式


### 环境要求
- Python 3.9+
- Jupyter Notebook

