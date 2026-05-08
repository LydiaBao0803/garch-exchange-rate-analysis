# Impact of Crude Oil Price Volatility on Major Currency Exchange Rates: A GARCH Model Empirical Study

## Overview
This project investigates how Brent crude oil price fluctuations affect the exchange rate volatility of nine major oil-linked currencies (USD/RUB, USD/NOK, USD/CAD, USD/SAR, USD/JPY, USD/CNY, USD/INR, USD/EUR, USD/BRL) using GARCH(1,1) models with oil price as an external regressor. The study combines time-series diagnostics, ARCH effect testing, and parameter estimation to quantify each currency's sensitivity to oil price shocks.

## Key Skills Demonstrated
- Time-series analysis: log-return computation, stationarity (ADF), and ARCH effect testing
- GARCH(1,1) model specification and fitting with external regressors (`rugarch`)
- Multi-currency comparative analysis and parameter extraction
- Rolling volatility computation and ACF/PACF diagnostic plots
- R Markdown reproducible reporting; LaTeX report typesetting

## Methods & Tools
- **Language**: R
- **Libraries**: `rugarch`, `FinTS`, `tseries`, `TTR`, `ggplot2`, `car`, `readr`
- **Techniques**: Log-return transformation, ADF stationarity test, Ljung-Box and ARCH-LM tests, GARCH(1,1) model with mean equation external regressor (Brent crude), standardized residual diagnostics

## Dataset
Daily log-return series for **9 USD exchange rate pairs** (RUB, NOK, CAD, SAR, JPY, CNY, INR, EUR, BRL) and **Brent crude oil prices**, stored in `log_return.csv` and `oildata.csv`. Data spans multiple years of daily observations.

## Results
- Estimated γ (gamma) coefficients quantify the marginal impact of oil price log-returns on each currency's conditional mean
- Oil-linked commodity currencies (RUB, NOK, CAD) showed stronger sensitivity to Brent crude fluctuations
- ARCH effects were successfully captured and eliminated in standardized residuals across all nine currency pairs
- Full results, coefficient table, and diagnostic plots compiled in `garch.pdf`

## File Structure
```
Final/
├── garch.Rmd             # Main R Markdown analysis script
├── garch.pdf             # Compiled full report
├── garch.html            # HTML version of report
├── garch.tex             # LaTeX source
├── log_return.csv        # Processed log-return data (currencies + oil)
├── oildata.csv           # Raw oil price data
└── data.ipynb            # Python EDA notebook (data preprocessing)
```

## How to Run
1. Open `garch.Rmd` in RStudio.
2. Ensure packages are installed: `install.packages(c("rugarch", "FinTS", "tseries", "TTR", "ggplot2", "car"))`
3. Update `data_path` to your local path for `log_return.csv`.
4. Knit to HTML or PDF.

---

# 原油价格波动对主要货币兑美元汇率影响的实证研究 — 基于 GARCH 模型

## 项目简介
本项目研究布伦特原油价格波动对九种主要货币兑美元汇率（USD/RUB、USD/NOK、USD/CAD、USD/SAR、USD/JPY、USD/CNY、USD/INR、USD/EUR、USD/BRL）波动性的影响，采用以原油价格为外生变量的 GARCH(1,1) 模型进行实证分析，结合时间序列诊断、ARCH 效应检验和参数估计，量化各货币对原油冲击的敏感性。

## 使用技术
- **语言**：R
- **主要库**：`rugarch`、`FinTS`、`tseries`、`TTR`、`ggplot2`、`car`
- **核心方法**：对数收益率计算、ADF 平稳性检验、ARCH-LM 效应检验、带外生变量的 GARCH(1,1) 均值方程、标准化残差诊断

## 数据集
九种 USD 汇率对（RUB、NOK、CAD、SAR、JPY、CNY、INR、EUR、BRL）与布伦特原油价格的日度对数收益率序列，存储于 `log_return.csv` 和 `oildata.csv`，涵盖多年日度数据。

## 主要结果
- 估计了各货币对原油价格的 γ 系数，量化原油价格对汇率条件均值的边际影响
- 大宗商品关联货币（RUB、NOK、CAD）对布伦特原油波动的敏感性更强
- 所有九对汇率的 GARCH 模型标准化残差中，ARCH 效应均得到有效消除
- 完整结果、系数表及诊断图表见 `garch.pdf`

## 文件说明
- `garch.Rmd`：主要 R Markdown 分析脚本
- `garch.pdf`：编译好的完整报告
- `log_return.csv`：已处理的对数收益率数据
- `oildata.csv`：原始原油价格数据
- `data.ipynb`：Python 数据预处理探索 notebook

## 运行方法
1. 在 RStudio 中打开 `garch.Rmd`
2. 安装依赖包：`install.packages(c("rugarch", "FinTS", "tseries", "TTR", "ggplot2", "car"))`
3. 将 `data_path` 更新为 `log_return.csv` 的本地路径
4. Knit 输出为 HTML 或 PDF
