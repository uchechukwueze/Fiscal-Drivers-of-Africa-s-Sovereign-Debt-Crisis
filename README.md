# Fiscal Drivers of-Africa's Sovereign Debt Crisis

This repository presents an analysis of a global fiscal dataset highlighting a critical macro-fiscal trend: emerging economies such as Nigeria, Egypt, and South Africa are experiencing widening fiscal deficits as expenditure growth consistently outpaces revenue mobilization. 

Using historical data, the analysis identifies the key drivers of fiscal instability, detects anomaly periods associated with major economic shocks, and projects a continued deepening of Nigeria’s 
fiscal deficit through 2027 under a business-as-usual scenario, absent meaningful structural reforms.

<img width="1536" height="1024" alt="Theme" src="https://github.com/user-attachments/assets/7c14c7a2-d198-4784-b5ad-05f2b866f5de" />

## Table of Contents
- [Abstract](#abstract)
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [Data Wrangling](#data-wrangling)
- [Analysis of Africa Fiscal Indicators](#analysis-of-africa-fiscal-indicators)
- [Nigeria as Case Study](#nigeria-as-case-study)
- [Correlation Analysis: Fiscal Indicators](#correlation-analysis-fiscal-indicators)
- [Trend Analysis](#trend-analysis)
- [Anomaly Detection and Prediction](#anomaly-detection-and-prediction)
- [Policy Simulation: Can We Close This Fiscal Gap by 2030?](#policy-simulation-can-we-close-this-fiscal-gap-by-2030)
- [Conclusion](#conclusion)
- [Recommendation](#recommendation)


### Abstract

In this project, I analyzed the fiscal and macroeconomic performance of many African economies using data compiled from various Central Banks and Statistical agencies of respective countries. In this project, I worked, cleaned, and explored 23,784 rows of records with 9 columns, including fiscal variables such as Budget Balance, Capital and Health Expenditure, GDP, Inflation, Unemployment, Government Debt, and Population metrics.
I applied AI-driven anomaly detection and predictive modelling to find insights, uncover instability risks, and forecast economic trends through 2028. I found that the growth of the African economies in 2025 is 3.9%. From the data, the average growth rate of the 14 economies in the dataset between 2000 and 2023 ranges from 8.54 of Ethiopia to 2.32% of South Africa. Unemployment, food inflation, and deficit remain major issues facing African countries.
I narrowed this study down to Nigeria. I found that between 2024 and 2025 alone, debt service rose by 73%, from ₦8.27tn to ₦14.32tn, highlighting the country's growing debt burden. Debt service currently accounts for 26.04% of the 2025 budget, up from 8.85% in 2009. Similarly, the debt service-to-GDP ratio has increased from 0.64% in 2009 to 4.07% in 2025. Meanwhile, the FG's budget deficit has continued to increase, reaching ₦13.08tn in the 2025 budget. However, as a percentage of the total budget, the deficit has declined to 23.79%. Since 2020, the budget deficit as a percentage of GDP has consistently exceeded the 3% threshold set by the Fiscal Responsibility Act. In the 2025 budget, the deficit stands at 3.72% of GDP.
My anomaly detection flagged the 2023 and 2025 budget deficits as unusually high. My model forecasted that fiscal deficits would continue to widen into 2026 to over ₦20.35tn, and to ₦18.61 and ₦16.86tn in 2027 and 2028, respectively. My policy simulation based on three case scenarios suggests that to tame fiscal crisis, the Nigerian government should embrace fiscal prudence by finding a way to boost revenue and cut the cost of governance.

### Problem Statement
Fiscal crises remain a major challenge confronting economies worldwide, with particularly severe consequences for developing economies in Africa. Despite the availability of extensive macroeconomic and fiscal data, weak integration and limited analytical use of these indicators often hinder the effectiveness of policy responses.
The aim of the project, is to used AI, data science, and analytical modelling to transform fragmented macroeconomic and fiscal indicators — such as Budget Balance, Capital and Health Expenditure, GDP, Inflation, Unemployment, Government Debt, and Population metrics — into meaningful intelligence that can strengthen governance, support inclusive growth, and drive evidence-based policy choices across many developing economies — including Nigeria and other African countries.
Also, I connect these datasets to measurable development outcomes and generate solutions that directly advance the Sustainable Development Goals (SDGs), such as linking health expenditure, population data, and real GDP to health system performance.

### Data Wrangling, Preprocess
To ensure robust and reliable insights, a rigorous data processing pipeline was implemented:
Data Cleaning: A total of 23,784 observations were carefully examined. Mixed data types in the Amount column were resolved by removing commas, parsing numeric values, and converting the Time variable into a standardized datetime format.
Unit Standardization: Significant heterogeneity existed across measurement units (Millions vs. Billions). All financial variables were therefore standardized to Millions of local currency, ensuring internal consistency within each country.
Currency Handling: Given country-specific currencies (e.g., EGP, NGN, ZAR, etc), cross-country aggregation was avoided to prevent misleading comparisons. Analysis instead emphasized within-country dynamics and normalized indicators such as fiscal deficits as a percentage of GDP.
Aggregation: High-frequency monthly flow variables, including budget deficits and revenues, were aggregated into annual totals to ensure alignment with yearly macroeconomic indicators such as GDP.

#### Tech Stack

I used Python for this project, using the libraries below.

Pandas: Data Cleaning and Manipulation

Numpy: Numeric/Data computation

seaborn: Visual display

Matplotlib: Visuliaztion

Sciklearn: Prediction and Forecast


<img width="3158" height="2091" alt="1" src="https://github.com/user-attachments/assets/53e1d2aa-53be-4bed-b961-dc366806922d" />

Economic growth rate measures the pace at which an economy expands over time. According to World Bank projections, African economies are expected to grow by 4.3 percent in 2026-2027. However, historical data from 2000 to 2024 reveal substantial cross-country variation. Over this period, average growth rates ranged from as high as 8.54 percent in Ethiopia to as low as 2.32 percent in South Africa, highlighting the uneven growth performance across the continent.


<img width="2515" height="1575" alt="2" src="https://github.com/user-attachments/assets/a7ab455c-8992-436b-801d-d077f56b3da3" />

This shows largely that unemployment is a serious challenge facing African economies, with Botswana facing a whopping 26%, followed closely by South Africa experiencing 25.7% rate of unemployment. Kenya has a margin of 6%. Unemployment is a killer of the economy, as productive resources that should be channeled into productive use lie idle.


<img width="3115" height="1629" alt="3" src="https://github.com/user-attachments/assets/9716f758-b56e-4a25-a94a-c4550ff91c62" />

Fiscal deficit is the heart of this project; the economy cannot survive without finance. Finance and Health are among the two most important parameters that affect all, whether you like it or not. The fiscal crisis facing African countries is proof that finance plays a key role in economic growth and development. Without finance government cannot run, salaries and wages of workers won't be paid, consumption drops, investment fails as well, and the economy collapses. Our data shows that the average deficit as a share of GDP for Egypt stood at -13.5% of Egypt's GDP, and Senegal witnessed -1.8% of deficit as a share of GDP. Deficit is a serious concern as it's one of the main reasons the economy goes bad into debt. When the measure cannot keep up with expenses.

### Nigeria as a Case Study
Let me begin this section with correlation analysis. How are these macroeconomic variables related to each other


<img width="2364" height="2036" alt="4" src="https://github.com/user-attachments/assets/0a55b43c-109b-48f1-8605-4f3759105c0b" />

From the correction above, there is a very strong correlation between revenue, expenditure, GDP, and inflation, among others. These fiscal indicators are very necessary for the welfare and growth of any economy. It is vital to know that correlation does not imply causation; there could be other unforeseen factors that may, in one way or another, drive or affect these parameters, factors like institutional quality in a country, among others.

### Trend Analysis of Nigeria Fiscal Indicators
I did some feature engineering by calculating various parameters like debt service % of GDP, deficit % of GDP, debt services % of total government expenditure, among others. This will offer us a better view of the performance of these fiscal indicators.
Let's decode the pattern.



<img width="3005" height="1574" alt="8" src="https://github.com/user-attachments/assets/2357a20d-378d-4f08-8618-1b892218f738" />

<img width="2992" height="1574" alt="7" src="https://github.com/user-attachments/assets/347640ef-dcd0-4aa4-a900-51827fee3b5b" />

<img width="2982" height="1574" alt="6" src="https://github.com/user-attachments/assets/b123568f-eef8-4a14-b174-aba96d4f096c" />

<img width="3016" height="1574" alt="5" src="https://github.com/user-attachments/assets/881d5eb8-82a3-4f39-a02a-34da45c39bde" />

<img width="2958" height="1575" alt="9" src="https://github.com/user-attachments/assets/8539d985-d99c-4e1a-beed-c11d894d6a61" />


The pattern is very clear: the budget deficit has widened over time, and this calls for urgent fiscal prudence. When revenue does not meet almost half of the expenditure, it shows there is something fundamentally wrong with the revenue projection of the government.

The Federal Government’s (FG) debt service obligations have expanded markedly, reflecting a deepening fiscal strain. The most pronounced surge occurred between 2024 and 2025, when debt service costs rose by an estimated 73 percent, increasing from ₦8.27 trillion to ₦14.32 trillion. This sharp escalation underscores Nigeria’s growing debt burden and the rising pressure on public finances.

Debt service now absorbs a substantial share of government spending. In the 2025 budget, it accounts for 26.04 percent of total expenditure, a significant increase from 8.85 percent in 2009. A similar pattern is evident relative to economic output: the debt service-to-GDP ratio has climbed from 0.64 percent in 2009 to 4.07 percent in 2025, highlighting the expanding fiscal cost of debt amid modest growth in national income.

At the same time, the FG’s budget deficit has continued to widen in nominal terms, reaching ₦13.08 trillion in the 2025 budget (the most pronounced outlier occurred between 2023 and 2025. This was detected by the AI-driven anomaly I deployed, showing far more unusual behavior. However, the deficit between 2024 and 2025 has moderated, declining to 23.79 percent, suggesting some improvement in expenditure coverage despite rising financing needs.

Nonetheless, fiscal risks remain elevated. Since 2020, the budget deficit as a share of GDP has consistently exceeded the 3 percent ceiling prescribed by the Fiscal Responsibility Act. In 2025, the deficit stands at 3.72 percent of GDP, reinforcing concerns about fiscal sustainability and the urgency of structural reforms to restore macro-fiscal balance.

### The misery Index


<img width="3135" height="1575" alt="10" src="https://github.com/user-attachments/assets/d8ff982b-84c3-4d5c-ae3f-21e58923df8d" />

The MIS Index, constructed as the sum of food inflation and the unemployment rate, provides a simple measure of macroeconomic distress faced by households.

Food inflation captures pressures on the cost of basic consumption, while unemployment reflects labor market weakness and income insecurity.

When combined, the index highlights periods in which rising prices and limited job opportunities simultaneously erode purchasing power and living standards.

In the context of fiscal crisis analysis, a rising food inflation–unemployment index signals heightened socio-economic stress that can intensify fiscal pressures through increased social spending needs, reduced revenue mobilization, and broader macroeconomic instability.

### How does fiscal distress affect Sustainable Development Goals?


<img width="2948" height="1575" alt="11" src="https://github.com/user-attachments/assets/2383ce25-2a28-4d44-9c8e-ccc2e5ab72ec" />


Mounting fiscal pressures have compelled the government to reallocate scarce public resources in ways that weaken long-term human capital development. As fiscal space narrows, spending priorities have increasingly shifted away from social investment toward security-related outlays.

This shift is evident in the growing dominance of state security over human security. Recent budget figures indicate that defense spending (approximately ₦743 billion) now far exceeds health expenditure (around ₦468 billion).

Such an imbalance risks undermining progress toward SDG 3 (Good Health and Well-being), as reduced investment in health constrains service delivery, worsens health outcomes, and weakens the foundations of inclusive growth.

### AI-driven Anomaly Detection and Prediction

<img width="3006" height="1581" alt="13" src="https://github.com/user-attachments/assets/25eb53bb-6283-4f7c-bb79-46981b044436" />

<img width="3016" height="1629" alt="12" src="https://github.com/user-attachments/assets/f5a7db07-8b9e-443d-ba30-90bcefd34385" />


A linear trend forecasting model was employed to project Nigeria’s fiscal outlook. The results suggest that the fiscal deficit will peak at ₦20.35 trillion in 2026, before moderating to ₦18.61 trillion in 2027 and ₦16.86 trillion in 2028. 

Overall, the model indicates an average annual widening of approximately ₦1.75 trillion, reflecting sustained fiscal pressures.


### Policy Simulation 
Can we close this fiscal gap by 2030?


<img width="3006" height="1629" alt="14" src="https://github.com/user-attachments/assets/5b6a633e-51c8-4719-8d60-55eb4164b53d" />

Fiscal matter is of policy importance. I simulated a 3-case policy scenario, and the best option is for the government to adopt both boosting revenue and cutting the cost of governance. Both seem to be the optimal social planner choice.

### Conclusion
The analysis reveals a strong relationship between fiscal deficits and the availability of resources for human capital investment, underscoring the crowding-out effect. As debt servicing obligations expand, funds that should be allocated to critical sectors such as health and education are increasingly diverted toward financing public debt. This reallocation erodes fiscal space, weakens long-term human capital development, and constrains inclusive growth.

### Recommendation

Against this backdrop, the following policy recommendations are proposed.

-First, the government should pursue gradual expenditure rationalization by eliminating non-essential and inefficient spending. 

While an abrupt reduction in the cost of governance may be impractical, a phased approach—such as incremental cuts to administrative and operational expenditures—can steadily reduce fiscal leakages without disrupting public service delivery.

-Second, enhanced financial intelligence and prioritization, akin to credit rationing in financial markets, should guide public investment decisions. 

The government must rigorously assess which capital and social projects yield the highest economic and social returns, while postponing or discontinuing projects with limited impact. This targeted allocation of resources would improve spending efficiency and fiscal sustainability.

-Finally, expanding and diversifying revenue streams must take precedence over continued expenditure expansion. Nigeria’s heavy reliance on oil revenues exposes public finances to external shocks, particularly crude oil price volatility. 

Strengthening revenue mobilization from non-oil sectors—such as manufacturing, agriculture, and services—offers a more resilient and sustainable fiscal base, enhancing the government’s capacity to finance development priorities.
