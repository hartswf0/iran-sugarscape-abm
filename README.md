# Iranian Sugar Economy Simulation — v2++

## Overview
This project implements a mobile-friendly, single-file HTML/CSS/JS simulation of the Iranian sugar economy, inspired by the Sugarscape agent-based model. It integrates historically grounded variables—tariffs, subsidies, sanctions, climate impact—with real-time price, trade, and inequality metrics. The model emphasizes **transparency of assumptions**, **user-editable equations**, and **exportable data** for reproducible analysis.

## Historical Scope
The simulation is calibrated to reflect major phases of Iran’s sugar trade and policy (19th–20th century), including:
- **Global price shocks** and maritime trade dependencies.
- **Colonial-era tariffs** and domestic industry protectionism.
- **Subsidy regimes** under Pahlavi modernization.
- **Sanctions effects** on shipping, finance, and imports.

## Key Features
1. **Responsive UI**
   - Works on mobile and desktop; two-row metrics header prevents clipping.
   - Metric dashboard: `Price`, `Imports`, `Domestic Output`, `Revenue`, `Inequality Index`.
2. **Explicit Mathematics**
   - All governing equations are visible, annotated, and user-editable in the **ƒx** panel.
   - Variables (`k`, `targetPrice`, `priceCap`, etc.) display live values and historical context.
3. **Breadcrumb Logging**
   - All equation edits timestamped and listed for reproducibility.
4. **Real Data Export**
   - CSV download of per-tick simulation output (`t`, policy variables, market variables, inequality).
5. **Scenario Fidelity**
   - Parameter ranges grounded in historical research; defaults match plausible archival estimates.

## Usage
- **Run:** Open `index.html` in any modern browser.
- **Edit Assumptions:** Click **ƒx** → modify variables/equations → changes apply immediately.
- **Export Data:** Click **⤓** to download results for further analysis in R/Python.
- **Inspect Logic:** View source; core model in `simulate()` function.

## Mathematical Model
Price and supply/demand dynamics follow:
price_next = price + k * (demand - supply) - tariffImpact + subsidyImpact - sanctionsFriction
where:
- `k` = price elasticity coefficient (editable)
- `tariffImpact` = tariffRate × price
- `subsidyImpact` = subsidyRate × domesticOutput
- `sanctionsFriction` = multiplier for reduced import capacity

All constants and functions are editable in the **ƒx** panel.

## Academic Relevance
This simulation is designed as a **transparent, manipulable historical model**—suitable for teaching economic history, computational social science, and agent-based modelling. Its explicit math layer allows it to function as both a pedagogical tool and a sandbox for hypothesis testing.

#PROMPT: {Create a mobile-optimized, single-file HTML/CSS/JS agent-based simulation inspired by the Sugarscape model, accurately modeling Iranian sugar history. The simulation must blend rigorous historical, spatial, and economic dynamics with authentic Iranian geometric aesthetics, ensuring cultural, temporal, and regional fidelity. The output should be lightweight, performant, visually distinct with Persian art motifs, and maintain clear negative constraints preventing anachronisms and homogenization. This prompt serves as the orienting core directive for all subsequent development instructions. how could this be used to model sugar history in iran

# Modeling Sugar History in Iran with Sugarscape Agent-Based Models

The Sugarscape agent-based model framework presents a compelling approach for understanding and simulating Iran's complex sugar history, which spans over 1,500 years from ancient Sassanian innovations to modern industrial development. By adapting the classic Sugarscape paradigm, researchers could create sophisticated models that capture the dynamic interplay of political, economic, and social factors that shaped Iran's sugar economy.

## **Historical Context for Model Development**

Iran's sugar history provides rich empirical data for agent-based modeling, beginning with the Sassanian invention of sugar refining around 460 CE and continuing through distinct phases of import dependency, monopolistic control, and industrial development[1][2][3]. The historical trajectory reveals several critical periods suitable for ABM analysis:

**Traditional Period (460-1600 CE)**: Early sugar refining technology, trade route dependencies, and regional production centers could be modeled as agents interacting in a network where technological knowledge, trade relationships, and resource availability determine outcomes[1][4][5].

**Import-Dependent Era (1600-1930)**: The complex web of international sugar trade - from Indian dominance to Dutch Java sugar, then French and Russian competition - presents an ideal scenario for multi-agent modeling of trade networks, pricing mechanisms, and political influence on market access[1][2][6].

**Monopoly and State Control Period (1925-1979)**: The Pahlavi era's state monopolies on sugar imports and exports, combined with taxation policies to fund infrastructure projects like the Trans-Iranian Railway, offer a clear case study for modeling government intervention in commodity markets[7][8][9][10][11].

**Modern Industrial Development (1932-present)**: The establishment of domestic sugar beet and sugarcane industries, private-public partnerships, and contemporary challenges with subsidies and price controls provide data for modeling industrial policy effectiveness[1][3][12][13][14].

## **Agent Types and Behavioral Rules**

A Sugarscape model of Iranian sugar history could incorporate multiple agent types, each with distinct behavioral rules based on historical evidence:

**Producer Agents**: Representing sugar beet farmers, sugarcane cultivators, and industrial refineries with attributes including production capacity, technological efficiency, geographic location, and responsiveness to government policies. Historical data shows significant variation in productivity - from 14.45 tons/hectare in Yasooj to 45.38 tons/hectare in Khuzestan - which could inform agent heterogeneity[15][16][17].

**Government Agents**: Modeling state behavior in taxation, monopoly creation, subsidy allocation, and industrial policy. The historical record of sugar monopolies (1927-1932), state-owned companies, and contemporary import controls provides clear behavioral patterns[7][8][14][10].

**Trader/Merchant Agents**: Representing bazaar merchants, international trading companies (Dutch East India Company, British traders), and modern importers. Their behavior would be driven by profit maximization, relationship networks, and regulatory compliance, with historical examples showing adaptation to changing trade routes and political conditions[1][2][6].

**Consumer Agents**: Modeling household demand, industrial users (confectionery, beverage industries), and institutional consumers with varying price sensitivities and substitution behaviors. Per capita consumption data (25-30 kg annually in recent decades) provides calibration parameters[1][18].

## **Environment and Resource Dynamics**

The model environment would represent Iran's geographic and economic landscape with cells containing different attributes:

**Agricultural Zones**: Sugar beet regions (Kermanshah, Fars, Isfahan, Azerbaijan) and sugarcane areas (Khuzestan) with varying soil quality, water availability, and climate conditions affecting productivity[1][18][15][16].

**Transportation Networks**: Historical trade routes (Silk Road connections, Persian Gulf ports) and modern infrastructure (Trans-Iranian Railway, road networks) that influence distribution costs and market access[2][8][9].

**Political Boundaries**: Reflecting changing sovereignty, international sanctions, and trade agreements that affect market access and pricing. The model could simulate how political events (wars, revolutions, sanctions) disrupt supply chains and force adaptation[3][12].

## **Dynamic Scenarios and Policy Analysis**

The agent-based model could simulate various historical scenarios and evaluate counterfactual policy options:

**Monopoly Impact Analysis**: Modeling how the Pahlavi sugar monopolies (1927-1932) affected market efficiency, price stability, and revenue generation compared to competitive markets[7][10][11].

**Industrial Development Pathways**: Analyzing the timing and effectiveness of domestic sugar industry development, comparing the successful post-1932 development with earlier failed attempts in the 1860s[1][3].

**Import Substitution Effects**: Examining how domestic production growth affected import dependency, trade balance, and food security, particularly during periods of international conflict or sanctions[1][19][14].

**Subsidy and Taxation Policy**: Modeling the complex effects of sugar subsidies alongside sugar taxes on beverages, analyzing unintended consequences and policy effectiveness[13][20][21].

## **Advanced Model Features**

Modern ABM implementations could incorporate sophisticated features:

**Adaptive Learning**: Agents could learn from market conditions, adjusting production decisions, trading strategies, or consumption patterns based on experience and information availability[22][23].

**Network Effects**: Modeling how merchant networks, political connections, and technological knowledge transfer influence market outcomes and industrial development[2][24].

**Multi-Scale Dynamics**: Connecting household-level consumption decisions to national policy outcomes, similar to how individual farmer decisions aggregate to national production levels[24][25].

**Uncertainty and Risk**: Incorporating climate variability, political instability, and international market volatility that characterized Iran's sugar history[3][12][23].

## **Validation and Calibration**

The rich historical data on Iranian sugar production, imports, prices, and consumption provides extensive opportunities for model validation[1][16][17][26]. Key metrics for calibration include:

- Production volumes and geographic distribution over time
- Import quantities and source countries
- Price movements and market volatility
- Government revenue from sugar-related taxes and monopolies
- Industrial development patterns and capacity utilization

## **Research Applications and Insights**

Such a model could address important research questions about economic development, state capacity, and policy effectiveness:

**Industrial Policy Evaluation**: Understanding why some government interventions (post-1932 sugar industry development) succeeded while others (1860s attempts) failed[1][3].

**Trade Network Resilience**: Analyzing how Iran's sugar supply networks adapted to changing geopolitical conditions and trade disruptions[2][6].

**Market Institution Evolution**: Tracing the transformation from traditional bazaar-based trading to modern industrial and financial institutions[7][10].

**Policy Unintended Consequences**: Examining how sugar subsidies, import monopolies, and taxation policies created distortions and rent-seeking behavior[13][14][21].

By combining the Sugarscape framework's proven ability to model complex adaptive systems with Iran's rich sugar history, researchers could create powerful tools for understanding economic development, policy effectiveness, and market evolution in developing economies. The model would not only illuminate Iran's specific experience but provide insights applicable to other countries undergoing similar transitions from traditional to modern economic systems.

Citations:
[1] SUGAR - Encyclopaedia Iranica https://www.iranicaonline.org/articles/sugar-cultivation/
[2] COMMERCE vi. In the Safavid and Qajar periods https://www.iranicaonline.org/articles/commerce-vi/
[3] The Rise and Fall of Haft-Tappeh Sugar Factory - IranWire https://iranwire.com/en/features/65658/
[4] History of Sugar https://www.sugar.org/sugar/history/
[5] Sugar & the Rise of the Plantation System https://www.worldhistory.org/article/1784/sugar--the-rise-of-the-plantation-system/
[6] [PDF] Sugar trade in the Eighteenth-Century Persian Gulf https://scholarlypublications.universiteitleiden.nl/access/item:2945280/view
[7] COMMERCE vii. In the Pahlavi and post-Pahlavi periods https://www.iranicaonline.org/articles/commerce-vii/
[8] ECONOMY ix. IN THE PAHLAVI PERIOD - Encyclopaedia Iranica https://www.iranicaonline.org/articles/economy-ix/
[9] A Brief History of 20th-Century Iran - Grey Art Museum https://greyartmuseum.nyu.edu/2015/12/a-brief-history-of-20th-century-iran/
[10] Reza Shah and the Pahlavi Order (1925–1941) - Iran - Erenow https://erenow.org/modern/iran-a-modern-history/9.php
[11] God, Shah, Nation: Reza Shah's Modernization of Iran https://thelionandthesun.org/958/god-shah-nation-reza-shahs-modernization-of-iran/
[12] Haft Tappeh Sugarcane Agro-Industry Co. - Wikipedia https://en.wikipedia.org/wiki/Haft_Tappeh_Sugarcane_Agro-Industry_Co.
[13] Why has the taxing policy on sugar sweetened beverages not ... https://pmc.ncbi.nlm.nih.gov/articles/PMC9939810/
[14] Iran in Crisis: Government Monopoly on Sugar Imports https://iranfocus.com/economy/33945-iran-in-crisis-government-monopoly-on-sugar-imports/
[15] [PDF] SUGAR BEET PRODUCTION IN IRAN, A STYUDY ON ... https://assbt.org/wp-content/uploads/2023/09/Vol32AgP603to607SugarbeetProductioninIranaStudyonProductionRestrictingFactors.pdf
[16] Iran Agricultural Production: Sugar Beet | Economic Indicators - CEIC https://www.ceicdata.com/en/iran/agricultural-production/agricultural-production-sugar-beet
[17] Iran Agricultural Production: Sugar Cane | Economic Indicators - CEIC https://www.ceicdata.com/en/iran/agricultural-production/agricultural-production-sugar-cane
[18] Agriculture - کشت و صنعت حکیم فارابی خوزستان https://hakimfarabi.co/en/about-us/agriculture/
[19] Agriculture in Iran - Wikipedia https://en.wikipedia.org/wiki/Agriculture_in_Iran
[20] Subsidies in Iran - Wikipedia https://en.wikipedia.org/wiki/Subsidies_in_Iran
[21] Economic barriers and gaps to reach the desirable consumption of ... https://pmc.ncbi.nlm.nih.gov/articles/PMC9885062/
[22] Agent-Based Modeling as a Tool for Trade and Development Theory https://www.jasss.org/16/2/1.html
[23] Agent-based models: understanding the economy from the bottom up https://www.bankofengland.co.uk/-/media/boe/files/quarterly-bulletin/2016/agent-based-models-understanding-the-economy-from-the-bottom-up.pdf?la=en&hash=66A41463EC6EBCDD4B040AA27A8DF7929387A5B6
[24] agent-based modeling for livestock systems: the mechanics of ... https://academic.oup.com/jas/article/doi/10.1093/jas/skad321/7441327
[25] [PDF] Using NetLogo to Build an Agent-Based Model for Teaching ... https://www.aetrjournal.org/UserFiles/file/AETR_2023_044RR%20Final.pdf
[26] Iran Imports of Sugars and sugar confectionery - Trading Economics https://tradingeconomics.com/iran/imports/sugars-sugar-confectionery
[27] History of the establishment of agro-industry in Iran - Azar tarvand https://azartarvand.com/history-of-the-establishment-of-agro-industry-in-iran/
[28] The oil boom and structural transformation in the sugar industry of Iran https://www.sciencedirect.com/science/article/abs/pii/074301679190004C
[29] [PDF] Sugar trade in the Eighteenth-Century Persian Gulf https://scholarlypublications.universiteitleiden.nl/access/item:2945277/view
[30] History of sugar - Wikipedia https://en.wikipedia.org/wiki/History_of_sugar
[31] Simulating Sugar Rush with Python: An Agent-Based Model with Mesa https://towardsai.net/p/l/simulating-sugar-rush-with-python-an-agent-based-model-with-mesa
[32] [PDF] Modeling Tariff Rate Quotas in a Global Context: The Case of Sugar ... https://www.card.iastate.edu/products/publications/pdf/03wp343.pdf
[33] [PDF] A Builder's Guide to Agent Based Financial Markets https://wiki.santafe.edu/images/2/25/Bldr.pdf
[34] Food and Agricultural Supply Chain (FASC) model https://inlsoftware.inl.gov/product/fasc-model
[35] Sugar Industry Process Modeling and the Role of Software in ... https://sugarsonline.com/sugar-industry-process-modeling-and-the-role-of-software-in-achieving-optimal-efficiency/
[36] Agent-based modeling in applied economics? : r/AskEconomics https://www.reddit.com/r/AskEconomics/comments/vt04as/agentbased_modeling_in_applied_economics/
[37] Essential Sugar Calculations: Costs, Yields, Margins - Vesper https://vespertool.com/knowledge-hub/sugar/types-of-data/calculations/
[38] Mohammad Reza Pahlavi - Wikipedia https://en.wikipedia.org/wiki/Mohammad_Reza_Pahlavi
[39] The constitutional revolution of 1905 in Tehran - Asfar https://asfar.org.uk/constitutional-revolution-1905-tehran-visible-manifestation-consequences-imperial-modernisation-qajar-iran-hellen-gheorghe/}
