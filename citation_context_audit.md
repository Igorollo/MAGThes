# Citation-Context Audit

Audit date: 2026-04-26  
Scope: `chapters/introduction.tex`, `chapters/conclusions.tex`, `chapters/chapter_1.tex`, `chapters/chapter_2.tex`, `chapters/chapter_3/chapter_3_methodology.tex`, `chapters/chapter_4/chapter_4_results.tex`, `chapters/chapter_5/chapter_5_interpretation.tex`  
Mode: citation-context audit only. Thesis chapter files were not edited.

## Method and Classification

I reviewed each `\cite{...}` instance in sentence and paragraph context, using `references.bib`, `references_audit.md`, chapter text, subagent chapter scans, and targeted checks against primary or official source pages where needed.

Classification labels:

- **Correct**: the source supports the local claim and is chapter-appropriate.
- **Weak but acceptable**: the source is directionally relevant, but the wording should be softened or paired with a better source.
- **Incorrect or misleading**: the cited source does not support the claim as written, or the wording materially overstates the source.
- **Uncertain/manual review**: source support could not be confirmed without checking full paper text, implementation details, or exact data extraction records.

## Chapter-Level Audit

### Introduction

No external citations appear in `chapters/introduction.tex`.

| Line | Claim / passage | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|
| 4-9 | Broad background claims about cryptocurrencies, decentralization, speculative trading, social-media attention, and smaller markets reacting more strongly to organized signals. | **Weak but acceptable** as introductory framing, since later chapters cite the relevant literature. If the thesis style expects citations even in the introduction, these claims need light support. | Minor | Either leave as overview, or add a compact citation cluster to Chapter 1 sources such as `kamps2018pump`, `li2021cryptocurrency`, `amihud2002illiquidity`. |

### Chapter 1: Literature and Theory

Well-supported uses:

- `allen1992stock` at line 10 is appropriate for theoretical stock-price manipulation, though "broadcast signals" is slightly broader than the classic model.
- `gandal2018price`, `kamps2018pump`, and `victor2019cryptocurrency` at line 18 are well matched to crypto manipulation and pump-and-dump detection/quantification.
- `vanbommel2003rumors` and `sabherwal2011internet` at line 31 are well matched to rumors/message-board influence without fundamental news.
- `rubin1974estimating` and `angrist2009mostly` at line 56 are appropriate for potential outcomes and observational causal comparison.
- `dhawan2023new` at line 22 is strong for open participation despite poor expected returns; Oxford's abstract states that participants join despite negative expected returns and that overconfidence/gambling preferences help explain this behavior.

Problematic or weak uses:

| Line | Claim / passage | Cited source | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|---|
| 12 | Traditional market manipulation findings are "highly relevant" to crypto because crypto has limited regulation, uneven information distribution, and weaker investor protection. | `aggarwal2006stock`, `khwaja2005unchecked` | **Weak but acceptable.** These sources support traditional/emerging-market manipulation analogies, but they do not directly establish crypto-market regulation or investor-protection conditions. | Minor | Phrase as analogy: "These findings provide an analogy for cryptocurrency markets..." or add a crypto-specific market-structure/regulation source. |
| 14 | Fragmented exchanges create price discrepancies; digital assets have extreme volatility and inconsistent volume. | `makarov2020trading`, `liu2021risks` | **Correct/weak split.** `makarov2020trading` is strong for exchange fragmentation/arbitrage. `liu2021risks` supports crypto risk/return and volatility more than "inconsistent trading volume" specifically. | Minor | Keep `makarov2020trading`; soften the volume clause or pair with pump/detection literature that discusses low-liquidity targets. |
| 24 | Market capitalization "serves as a reliable proxy" for resistance to organized demand. | `amihud2002illiquidity` | **Weak but acceptable.** Amihud supports illiquidity/price impact, not market capitalization as a reliable proxy. The source is conceptually relevant but the wording overclaims. | Substantial because market-cap stratification is central | Change "reliable proxy" to "rough proxy" or "practical proxy"; optionally add a source directly connecting market cap/liquidity in crypto pump targeting. |
| 37 | Messaging platforms such as Telegram, Discord and similar channels are important venues; content/delivery are integral. | `li2021cryptocurrency`, `lamorgia2023doge`, plus `mirtaheri2021identifying`, `xu2019anatomy` | **Mostly correct, partly weak.** `lamorgia2023doge` strongly supports Telegram/Discord coordination; `xu2019anatomy` supports Telegram; `li2021cryptocurrency` supports pump market effects but is less direct for Telegram platform centrality. The "content and delivery" inference is plausible but should remain interpretive. | Minor | Keep, but avoid implying all cited sources directly theorize message delivery. |
| 46 | Existing research focuses on detecting pump schemes or predicting target coin. | `kamps2018pump`, `victor2019cryptocurrency`, `lamorgia2020pump`, `hu2023sequence`, `fu2025perseus` | **Incorrect for `fu2025perseus`.** PERSEUS is about tracing/identifying masterminds behind schemes, not target-coin prediction. | Moderate | Remove `fu2025perseus` from this detection/target-prediction list or move it to a separate clause about actor/mastermind tracing. |
| 58 | Xu and Livshits report that price usually reaches peak within a few minutes. | `xu2019anatomy` | **Weak but acceptable.** The paper supports very fast dynamics and a case peak within seconds; it is less clear that "usually" is an aggregate finding. | Minor | Change "usually reaches" to "can reach" or "often reaches in the studied examples." |
| 60 | Li et al. support the 10-minute window; thesis measures return at the 10-minute mark. | `li2021cryptocurrency` | **Weak but acceptable with nuance.** Li et al. support a 600-second/10-minute event horizon and maximum return within 10 minutes, but not necessarily a fixed return exactly at minute 10. | Substantial | Say Li et al. support using a 10-minute post-announcement horizon; the fixed 10-minute checkpoint is this thesis's comparability choice. |
| 64 | A 10-minute window "helps isolate the effect" of the signal. | `li2021cryptocurrency`, `lamorgia2023doge`, `kamps2018pump` | **Overstated.** These sources support fast pump dynamics and reversals, but a short window alone does not isolate causal effects. `lamorgia2023doge` is also weaker for a fixed 10-minute standard-pump outcome. | Moderate | Replace "helps isolate" with "reduces exposure to later unrelated market movements." |
| 75 | Organizers use forceful and urgent wording to minimize hesitation. | No citation | **Uncited claim.** Plausible from pump literature, but not backed at the hypothesis-formation point. | Minor/moderate | Add `xu2019anatomy`, `kamps2018pump`, or `lamorgia2023doge`, or frame as a thesis-specific operational premise. |
| 81 | H2 logic is "well-supported" by manipulation and illiquidity literature. | `amihud2002illiquidity`, `dhawan2023new` | **Weak but acceptable.** Amihud supports price impact from illiquidity; Dhawan supports crypto manipulation and participation, with stronger emphasis on illiquidity than market cap. They do not directly establish urgency-effect heterogeneity by market cap. | Moderate | Change "well-supported" to "motivated by" or "consistent with." |

### Chapter 2: Data Description and Exploratory Analysis

Well-supported uses:

- `telethon2023` at line 11 is appropriate for Telegram extraction via Telethon, with the usual caveat that the software citation is not version-pinned.
- `kamps2018pump` and `li2021cryptocurrency` at line 11 are appropriate for using prior pump-and-dump literature to seed channel discovery.
- `ccxt2023` at line 93 is appropriate for OHLCV extraction via CCXT; the CCXT manual documents unified OHLCV fetching, including 1-minute timeframes.
- `amihud2002illiquidity` at line 191, `roll1984simple` at line 207, and `parkinson1980extreme` at line 228 are strong matches for the corresponding market-microstructure measures.

Problematic or weak uses:

| Line | Claim / passage | Cited source | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|---|
| 9 | Telegram is one of the main platforms for coordinating crypto pump-and-dumps. | `li2021cryptocurrency` | **Weak but acceptable.** Li et al. support crypto P&D effects, but `kamps2018pump`, `xu2019anatomy`, or `lamorgia2023doge` more directly support Telegram/Discord platform use. | Minor | Add or replace with `kamps2018pump` / `xu2019anatomy` / `lamorgia2023doge`. |
| 49 | Gemini is effective because it enables accurate, context-aware classification without a large labeled dataset. | `gemini2025pro` | **Weak / potentially misleading.** Google documentation supports model identity and general reasoning capability, not task-specific classification accuracy on pump signals. | Substantial if treated as validation evidence | Soften to "used for initial annotation because of its general reasoning and long-context capabilities"; keep actual accuracy claims tied to internal validation results. |
| 49 | XLM-R is multilingual, open-source, cost-free, and efficient on local GPU hardware. | `conneau2020xlmroberta` | **Correct/weak split.** ACL source supports multilingual/cross-lingual performance. It is weaker for "cost-free" and local GPU efficiency. | Minor | Keep citation for architecture/performance; support deployment/cost claims with software/model documentation or reword as implementation choices. |
| 88 | Gemini verified each candidate `T_0`; validation confirmed/corrected 97.9%. | `gemini2025pro` | **Weak for validation.** The citation supports the model used, not correctness of the thesis's validation procedure. | Moderate | Tie the 97.9% statement to internal validation/procedure, not to Google documentation. |
| 114 | BTC/ETH/BNB/USDT quote-currency background, including BNB fee discounts as quote asset. | No citation | **Incorrect/unsupported in part.** BTC/ETH and USDT claims are plausible but uncited. BNB fee discounts come from using BNB to pay fees, not from BNB being a quote asset. | Substantial | Correct BNB wording and cite Binance/Tether or exchange documentation, or keep this as a narrower dataset explanation. |
| 116 | Broader market shift toward stablecoin-denominated trading and organizer motive to realize dollar-equivalent gains. | Figure only, no external citation | **Weak/unsupported.** The figure supports sample composition, not a general market-wide shift or organizer motive. | Substantial | Limit to the thesis sample, or add stablecoin/market-structure literature. |
| 130 | CoinMarketCap historical metadata snapshots on Sunday preceding each event. | `coinmarketcap2024api` | **Weak / uncertain.** CMC docs support historical market data and metadata endpoints, but not clearly historical project metadata snapshots via API. | Moderate | Clarify whether data came from API historical quotes, website snapshots, or stored local snapshots; cite the exact endpoint/source. |
| 169 | Pump organizers rely on urgency and FOMO cues. | `lamorgia2023doge` | **Weak but acceptable.** La Morgia supports Telegram/Discord coordination, FOMO/shilling, and fast operations; it is weaker for this thesis's exact uppercase-ratio "Urgency Index" construct. | Minor | State that prior work documents FOMO/shilling and rapid coordination, while uppercase ratio is this thesis's proxy. |
| 184 | Volume z-score detects potential insider front-running. | `lamorgia2020pump` | **Weak.** La Morgia supports early access/hierarchy and price-volume spikes, but not the exact `T_0-1` z-score as front-running detection. | Moderate | Reword to "captures abnormal pre-announcement volume that may be consistent with early activity." |
| 205 | Elevated pre-pump run-up "strongly suggests" insider accumulation or information leakage. | `lamorgia2020pump` | **Overstated.** A run-up may be consistent with leakage/early accumulation but does not establish it. `li2021cryptocurrency` is better support for pre-announcement run-ups and wealth transfer. | Substantial | Change to "may be consistent with"; consider adding `li2021cryptocurrency`. |
| 221 | Close Location Value formula. | `arms1994volume` | **Incorrect or weak.** CLV is usually tied to Chaikin accumulation/distribution; Arms is more closely associated with Ease of Movement. The prior bibliography audit also found the Arms edition ambiguous. | Moderate | Replace or supplement with a direct CLV / accumulation-distribution source. |
| 303 | DOCK/RLC/TRB/RVN project descriptions and token purposes. | No citation | **Uncited factual background.** The descriptions are broadly correct but need official project documentation if retained. | Substantial | Add official project docs/whitepapers or reduce to neutral "sample tokens" wording without detailed functional claims. |

### Chapter 3: Methodology

Well-supported uses:

- `rubin1974estimating` at line 8 is correct for potential outcomes/counterfactual treatment logic.
- `chernozhukov2018double` at line 73 is correct for DML, nuisance models, residualization, orthogonality, and cross-fitting, as long as inference claims stay conditional.
- `breiman2001random`, `econml`, and `chernozhukov2018double` at line 119 are appropriate for Random Forests, EconML `LinearDML`, and the DML framework.
- `athey2019generalized` at line 163 is appropriate for generalized/causal forests and treatment-effect heterogeneity.
- `xgboost2016`, `lightgbm2017`, `breiman2001random`, and `optuna2019` at line 186 are correct for model/tool provenance.

Problematic or weak uses:

| Line | Claim / passage | Cited source | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|---|
| 61 | Synthetic-control CAR rejected because fits were too weak. | `abadie2010synthetic` | **Weak but acceptable.** Abadie 2010 supports the original SCM method. Abadie 2021 is a better fit for feasibility, data requirements, and poor-fit concerns. | Minor/moderate | Cite `abadie2021synthetic` alongside or instead when discussing feasibility/fit diagnostics. |
| 117 | Cross-fitting avoids finite-sample bias and prevents overfitting. | No citation at sentence; relies on DML section | **Overstated.** DML literature supports reducing overfitting/regularization bias under conditions, not eliminating finite-sample bias. | Minor/moderate | Reword to "mitigate overfitting and regularization bias." |
| 119 | All calculations follow the exact influence functions in Chernozhukov et al. | `chernozhukov2018double` | **Weak/uncertain.** The framework is correct, but "exact influence functions" should be verified against the EconML implementation and thesis code. | Moderate | Change to "follow the DML orthogonalization and inference framework." |
| 130 | VIF values below 5 indicate limited multicollinearity concerns. | `obrien2007` | **Weak / mismatched.** O'Brien is a caution against rigid VIF rules of thumb, not support for a hard threshold. The observed VIFs below 1.2 are still reassuring. | Moderate | Say VIFs are very low and cite O'Brien as cautioning that thresholds are contextual. |
| 132 | E-values quantify robustness and help assess model stability. | `vanderweele2017sensitivity` | **Correct for unmeasured confounding, weak for "model stability."** VanderWeele and Ding define E-values for robustness to unmeasured confounding on a risk-ratio scale. They do not assess general model stability. | Substantial | Limit wording to sensitivity to unmeasured confounding; remove "model stability." |
| 132 / Ch. 4 table | E-values for continuous DML log-return coefficients. | `vanderweele2017sensitivity` | **Uncertain/manual review.** E-values can be extended via conversions, but the thesis must document how continuous coefficients were converted or approximated. | Substantial | Add calculation/provenance for the effect-scale conversion, or soften/remove the E-value interpretation. |
| 139 | Bootstrap inference is "more reliable"; variance across 500 runs constructs CIs. | `econml` cited earlier but not here | **Weak.** EconML supports `BootstrapInference`, but default CI construction may use pivot/percentile/bootstrap methods, not simply variance across runs. | Minor/moderate | Cite `econml` here and describe bootstrap CIs generically unless the exact bootstrap type was normal. |
| 144 | Highly liquid markets naturally resist simple manipulation. | No citation | **Weak/uncited.** Plausible and supported elsewhere in the thesis, but this methodological design choice should point back to liquidity/manipulation literature. | Minor | Cite `amihud2002illiquidity`, `kamps2018pump`, `dhawan2023new`, or phrase as design motivation. |
| 167 | Smaller nuisance models keep the system efficient "without losing accuracy" and "pinpoint" vulnerability. | No citation | **Overstated.** This is an implementation assertion, not established by citation. | Minor | Reword to "reduce computation while preserving the intended model specification" and "estimate how..." |

### Chapter 4: Results

Problematic or weak uses:

| Line | Claim / passage | Cited source | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|---|
| 10 | VIF below 5 common threshold. | `obrien2007` | **Weak / mismatched.** Same issue as Chapter 3: O'Brien cautions against rigid thresholds. | Moderate | Reword: "VIFs are very low; following O'Brien's caution against rigid thresholds, these values do not indicate material collinearity." |
| 115 / 133 / 136 | E-values for significant effects and table interpretation. | `vanderweele2017sensitivity` | **Correct for method label; uncertain for application.** The E-value citation is appropriate for sensitivity to unmeasured confounding, but continuous log-return coefficient conversion needs documentation. | Substantial | Document the conversion/assumptions or soften the robustness claim. |
| 163 | "Highly meaningful predictive information" and "overwhelming majority." | No external citation | **Overstated result wording.** Not a citation mismatch, but too strong for a model-performance paragraph. | Minor | Use "useful predictive information" and "high recall." |
| 188 | Precision at 0.90 "ensuring that almost 9 in 10 signals execute successfully." | No external citation | **Misleading wording.** Precision means predicted positives are positive-return events in held-out data, not that trades execute successfully or are profitable. | Substantial | "Almost 9 in 10 predicted positives are positive 10-minute-return events in the held-out set." |
| 190 | Feature importance "drives" success; variables "confirm" that price must be easy to move. | No external citation | **Misleading causal language.** This conflicts with Chapter 5's correct warning that feature importance is predictive, not causal. | Substantial | Replace "driven by" with "the model relies on"; replace "confirming" with "consistent with." |

### Chapter 5: Interpretation

Well-supported or cautious uses:

- `amihud2002illiquidity` at line 16 is a good conceptual citation for thin-market price impact, provided the claim remains about liquidity/price impact rather than Telegram-specific coordination.
- Lines 20, 27, 29, 36, and 40 generally distinguish causality, prediction, and limitations carefully.

Problematic or weak uses:

| Line | Claim / passage | Cited source | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|---|
| 16 | Coordinated buying pressure matters more in thinner markets. | `amihud2002illiquidity` | **Correct but narrow.** Amihud supports illiquidity/price impact, not Telegram coordination specifically. | Minor | Keep citation, or pair with pump-specific literature if the sentence is meant to cover crypto pump mechanics. |
| 36 | Small-cap E-value is moderately robust to unmeasured confounding. | Implied `vanderweele2017sensitivity` from Ch. 4 | **Uncertain/manual review.** The interpretation depends on whether the continuous-outcome E-value calculation is valid and documented. | Substantial | Add calculation detail in methodology/results, or soften to "under the reported E-value calculation." |

### Conclusions

No external citations appear in `chapters/conclusions.tex`.

| Line | Claim / passage | Assessment | Severity | Minimal correction |
|---:|---|---|---|---|
| 30-32 | Prior work has shown pump-and-dump schemes can be found in market and messaging data. | **Weak but acceptable** as a recap if the conclusion is summarizing Chapter 1. | Minor | Add "as reviewed in Chapter 1" or cite `kamps2018pump`, `victor2019cryptocurrency`, `xu2019anatomy`, `li2021cryptocurrency`. |
| 4 / 10 / 54 | Urgency as short-lived coordination trigger; pump messages as coordination tools. | **Acceptable thesis interpretation** if framed as the thesis's finding, not as a literature fact. | Minor | Keep conditional framing; avoid adding unsupported general claims. |

## Most Important Cross-Thesis Problems

1. **E-values are the highest-risk methodological issue.** `vanderweele2017sensitivity` supports E-values for unmeasured confounding, but the thesis reports E-values for continuous DML log-return coefficients. The calculation needs explicit conversion/provenance or weaker interpretation.
2. **O'Brien is used backward as threshold support.** `obrien2007` cautions against rigid VIF rules; the thesis should not present it as endorsing a fixed threshold of 5.
3. **The 10-minute outcome window is partly supported but overstated.** `li2021cryptocurrency` supports a 600-second event horizon and maximum-return construction, not automatically the thesis's fixed return at exactly minute 10.
4. **Prediction results sometimes use causal or trading-execution language.** Chapter 4 should avoid "drive," "confirm," and "execute successfully" when discussing feature importance and precision.
5. **Chapter 2 contains several data/context claims that need source tightening.** Quote-currency background, BNB fee-discount wording, CoinMarketCap historical metadata, CLV support, and project descriptions are the main issues.
6. **Market cap as a liquidity proxy should be softened.** `amihud2002illiquidity` supports illiquidity and price impact, not market capitalization as a reliable proxy.

## Especially Well-Used Citations

- `rubin1974estimating` and `angrist2009mostly` for potential outcomes and observational causal comparison.
- `chernozhukov2018double` for DML orthogonalization, nuisance models, and cross-fitting.
- `athey2019generalized` for Causal Forest / heterogeneous-treatment-effect estimation.
- `breiman2001random`, `xgboost2016`, `lightgbm2017`, and `optuna2019` for algorithm/tool provenance.
- `amihud2002illiquidity`, `roll1984simple`, and `parkinson1980extreme` for the corresponding liquidity/spread/volatility measures.
- `kamps2018pump`, `victor2019cryptocurrency`, `xu2019anatomy`, `li2021cryptocurrency`, and `lamorgia2023doge` for the general existence, detection, platform context, and fast dynamics of crypto pump-and-dump schemes, with the specific caveats listed above.
- `dhawan2023new` for open participation despite negative expected returns and gambling/overconfidence mechanisms.
- `ccxt2023`, `telethon2023`, and `gemini2025pro` for identifying software/model tools used, though all should avoid implying task-specific validity without internal validation.

## Uncertain / Manual Review Needed

- **E-value implementation:** verify the formula and scale conversion for continuous DML log-return coefficients.
- **CLV citation:** verify whether `arms1994volume` actually supports the Close Location Value formula; current evidence suggests it should be replaced or supplemented.
- **CoinMarketCap extraction:** verify whether historical market capitalization and metadata came from API historical endpoints, website snapshots, or stored local snapshots.
- **Lamorgia front-running/run-up support:** verify whether `lamorgia2020pump` directly discusses one-minute pre-announcement volume/run-up as insider or front-running evidence.
- **Gemini validation:** ensure the 97.9% T0 validation result is presented as internal validation, not as something supported by Google model documentation.
- **Project descriptions:** if DOCK/RLC/TRB/RVN descriptions remain, add official project documentation or neutralize the wording.

## Source Links Used for Targeted Context Checks

- Kamps and Kleinberg, 2018: https://link.springer.com/article/10.1186/s40163-018-0093-5
- Li, Shin, and Wang, 2025: https://www.cambridge.org/core/journals/journal-of-financial-and-quantitative-analysis/article/cryptocurrency-pumpanddump-schemes/97149DCD519BAF838F269F98DC76D682
- Xu and Livshits, 2019: https://www.usenix.org/conference/usenixsecurity19/presentation/xu-jiahua
- La Morgia et al., 2023: https://iris.uniroma1.it/handle/11573/1673225
- Dhawan and Putnins, 2023: https://academic.oup.com/rof/article/27/3/935/6655707
- Fu et al., 2025: https://arxiv.org/abs/2503.01686
- Chernozhukov et al., 2018: https://academic.oup.com/ectj/article/21/1/C1/5056401
- EconML DML documentation: https://www.pywhy.org/EconML/spec/estimation/dml.html
- VanderWeele and Ding, 2017: https://dash.harvard.edu/entities/publication/73120378-fbd5-6bd4-e053-0100007fdf3b
- O'Brien, 2007: https://doi.org/10.1007/s11135-006-9018-6
- Abadie, 2021: https://www.aeaweb.org/articles?id=10.1257/jel.20191450
- CCXT manual: https://github.com/ccxt/ccxt/wiki/Manual
- CoinMarketCap API documentation: https://coinmarketcap.com/api/documentation/v1/
- Google Gemini 2.5 Pro documentation: https://docs.cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/2-5-pro
- XLM-R ACL Anthology page: https://aclanthology.org/2020.acl-main.747/
- Roll, 1984 metadata/abstract: https://cir.nii.ac.jp/crid/1363670319131044480
- Generalized Random Forests Stanford page: https://www.gsb.stanford.edu/faculty-research/publications/generalized-random-forests
