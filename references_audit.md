# references.bib audit

Audit date: 2026-04-25  
File audited: `references.bib`  
Scope: report-only audit; `references.bib` was not edited.

## Summary

- The file contains 43 entries, not 42.
- No duplicate BibTeX keys were found.
- No clearly hallucinated reference was found.
- Strong confirmed corrections are needed for `econml`, `barabasi1999emergence`, `gandal2018price`, `liu2021risks`, `lightgbm2017`, `optuna2019`, `sabherwal2011internet`, and `vanderweele2017sensitivity`.
- Several live/software/documentation references exist but are weakly specified because they are not pinned to a version or stable release: `ccxt2023`, `telethon2023`, and `coinmarketcap2024api`.
- `arms1994volume` remains partly ambiguous: the 1994 Equis edition exists in bookseller/ISBN metadata, but stronger library evidence was found for the original 1983 Dow Jones-Irwin edition.
- Citation keys `li2021cryptocurrency` and `alexander2020critical` have stale years relative to their metadata, but that is a key-naming issue, not necessarily a bibliography metadata error.

## Full Entry Audit

| Key | Status | Evidence | Discrepancies and recommendation | Type / confidence |
|---|---|---|---|---|
| `rubin1974estimating` | Confirmed | [Crossref](https://api.crossref.org/works/10.1037%2Fh0037350), [ETS](https://www.ets.org/research/policy_research_reports/publications/article/1974/hrbx.html) | Metadata matches: Journal of Educational Psychology 66(5), 688--701, 1974, DOI `10.1037/h0037350`. | `@article` correct / high |
| `breiman2001random` | Confirmed | [Springer DOI](https://doi.org/10.1023/A:1010933404324), [CiNii/Crossref mirror](https://cir.nii.ac.jp/crid/1360574092892023168) | Metadata matches. DOI case differs across sources only; DOI is case-insensitive. | `@article` correct / high |
| `econml` | Confirmed with correction | [Microsoft Research](https://www.microsoft.com/en-us/research/project/econml/), [GitHub citation lines](https://github.com/py-why/EconML) | Current entry is too generic. Official project citation gives named authors, fuller title, GitHub URL, `year = {2019}`, and `note = {Version 0.x}`. | `@misc` acceptable; `@software` would be better only if the thesis BibTeX style supports it / high |
| `obrien2007` | Confirmed | [CiNii/Crossref](https://cir.nii.ac.jp/crid/1362544418759401600?lang=en), [DOI](https://doi.org/10.1007/s11135-006-9018-6) | Metadata matches: Quality & Quantity 41(5), 673--690, 2007. | `@article` correct / high |
| `angrist2009mostly` | Confirmed | [Ingram Academic](https://www.ingramacademic.com/9780691120355/mostly-harmless-econometrics), [MIT Press Bookstore](https://mitpressbookstore.mit.edu/book/9780691120355), [Springer review](https://link.springer.com/article/10.1007/s00362-009-0284-y) | Core metadata matches. Strong evidence supports ISBN `9780691120355` and Princeton University Press, 2009; ISBN could be added but absence is not an error. | `@book` correct / high |
| `conneau2020xlmroberta` | Confirmed | [ACL Anthology](https://aclanthology.org/2020.acl-main.747/), [DOI](https://doi.org/10.18653/v1/2020.acl-main.747) | Metadata matches. Optional additions: `month = jul`, `url`, editors. | `@inproceedings` correct / high |
| `ccxt2023` | Partially verified | [GitHub](https://github.com/ccxt/ccxt), [PyPI](https://pypi.org/project/ccxt/) | Source exists and title is supported. Entry is not version-pinned; `year = {2023}` is not tied to a specific release or access-time source. Consider citing a pinned version/release. | `@misc` acceptable; versioned software citation preferable / medium |
| `barabasi1999emergence` | Confirmed with correction | [PubMed](https://pubmed.ncbi.nlm.nih.gov/10521342/), [Crossref DOI](https://doi.org/10.1126/science.286.5439.509), [CEU metadata](https://research.ceu.edu/en/publications/emergence-of-scaling-in-random-networks/) | Entry is missing volume `286`, issue `5439`, pages `509--512`, and DOI `10.1126/science.286.5439.509`. | `@article` correct / high |
| `li2021cryptocurrency` | Confirmed | [Cambridge Core](https://www.cambridge.org/core/journals/journal-of-financial-and-quantitative-analysis/article/cryptocurrency-pumpanddump-schemes/97149DCD519BAF838F269F98DC76D682), [Crossref DOI](https://doi.org/10.1017/S0022109025000201) | Metadata matches final 2025 publication. The key name is stale (`2021`) but the fields are correct. | `@article` correct / high |
| `chernozhukov2018double` | Confirmed | [Oxford Academic](https://academic.oup.com/ectj/article-abstract/21/1/C1/5056401), [NBER working-paper page](https://www.nber.org/papers/w23564), [DOI](https://doi.org/10.1111/ectj.12097) | Metadata matches: Econometrics Journal 21(1), C1--C68, 2018. | `@article` correct / high |
| `athey2019generalized` | Confirmed | [Stanford GSB](https://www.gsb.stanford.edu/faculty-research/publications/generalized-random-forests), [DOI](https://doi.org/10.1214/18-AOS1709) | Metadata matches; Crossref may omit pages, but publisher/institutional metadata supports 1148--1178. | `@article` correct / high |
| `abadie2010synthetic` | Confirmed | [Taylor & Francis](https://www.tandfonline.com/doi/abs/10.1198/jasa.2009.ap08746), [Harvard Kennedy School](https://www.hks.harvard.edu/publications/synthetic-control-methods-comparative-case-studies-estimating-effect-californias-0), [RePEc](https://ideas.repec.org/a/bes/jnlasa/v105i490y2010p493-505.html) | Metadata matches: JASA 105(490), 493--505, 2010. | `@article` correct / high |
| `amihud2002illiquidity` | Confirmed | [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S1386418101000246), [DOI](https://doi.org/10.1016/S1386-4181(01)00024-6) | Metadata matches. | `@article` correct / high |
| `kamps2018pump` | Confirmed with caveat | [Springer](https://link.springer.com/article/10.1186/s40163-018-0093-5), [DOI](https://doi.org/10.1186/s40163-018-0093-5) | Source uses article number 18. `pages = {18}` is acceptable in many BibTeX styles, though an `eid`/article-number field would be more precise if supported. | `@article` correct / high |
| `telethon2023` | Partially verified | [GitHub archive](https://github.com/lonamiwebs/telethon), [PyPI](https://pypi.org/project/Telethon/) | Title and author are supported. GitHub repository is now archived and points to Codeberg; the entry is not version-pinned, and `year = {2023}` is not tied to a specific release. | `@misc` acceptable; versioned software citation preferable / medium |
| `coinmarketcap2024api` | Uncertain metadata | [Current docs](https://coinmarketcap.com/api/documentation/), [old v1 URL](https://coinmarketcap.com/api/documentation/v1/) | Source exists, but `/v1/` redirects to current docs. I found no strong evidence for `year = {2024}`. Keep as live documentation or update to current canonical URL/access date if citing current page state. | `@misc` appropriate / medium |
| `gemini2025pro` | Confirmed | [Google Cloud docs](https://cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/2-5-pro), [Google Cloud docs mirror](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/2-5-pro) | Model page exists; release date is 2025. Metadata is adequate for a documentation/model page. | `@misc` appropriate / high |
| `victor2019cryptocurrency` | Confirmed | [DOI](https://doi.org/10.1109/ICDMW.2019.00045), [DBLP](https://dblp.org/rec/conf/icdm/VictorH19), [EurekaMag metadata](https://eurekamag.com/research/102/824/102824695.php) | Metadata matches: ICDMW 2019, pages 244--251, IEEE. | `@inproceedings` correct / high |
| `xu2019anatomy` | Confirmed | [USENIX](https://www.usenix.org/conference/usenixsecurity19/presentation/xu-jiahua), [DBLP](https://dblp.org/rec/conf/uss/XuL19), [EPFL record](https://infoscience.epfl.ch/handle/20.500.14299/166389) | Metadata matches. Optional: add `month = aug` and `isbn = {978-1-939133-06-9}` from USENIX. | `@inproceedings` correct / high |
| `gandal2018price` | Confirmed with correction | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0304393217301666), [Tel Aviv University record](https://cris.tau.ac.il/en/publications/price-manipulation-in-the-bitcoin-ecosystem), [RePEc](https://ideas.repec.org/a/eee/moneco/v95y2018icp86-96.html) | Entry is missing volume `95`, pages `86--96`, and DOI `10.1016/j.jmoneco.2017.12.004`. | `@article` correct / high |
| `abadie2021synthetic` | Confirmed | [AEA](https://www.aeaweb.org/articles?id=10.1257/jel.20191450), [DOI](https://doi.org/10.1257/jel.20191450) | Metadata matches: Journal of Economic Literature 59(2), 391--425, 2021. | `@article` correct / high |
| `liu2021risks` | Confirmed with correction | [Oxford Academic](https://academic.oup.com/rfs/article/34/6/2689/5912024), [NBER](https://www.nber.org/papers/w24877), [DOI](https://doi.org/10.1093/rfs/hhaa113) | Author should be `Aleh Tsyvinski`, not `Oleg Tsyvinski`; missing volume `34`, issue `6`, pages `2689--2727`, and DOI `10.1093/rfs/hhaa113`. | `@article` correct / high |
| `barndorff2002estimating` | Confirmed | [DOI](https://doi.org/10.1002/jae.691), [RePEc](https://ideas.repec.org/a/jae/japmet/v17y2002i5p457-477.html) | Metadata matches. | `@article` correct / high |
| `lamorgia2020pump` | Confirmed | [DOI](https://doi.org/10.1109/ICCCN49398.2020.9209660), [DBLP](https://dblp.org/rec/conf/icccn/MorgiaMSS20), [secondary citation](https://www.ijraset.com/research-paper/analysing-cryptocurrency-pump-and-dump-scams) | Metadata matches: ICCCN 2020, pages 1--9, IEEE. | `@inproceedings` correct / high |
| `alexander2020critical` | Confirmed with key caveat | [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3382828), [DOI](https://doi.org/10.2139/ssrn.3382828) | Metadata supports `year = {2019}` and `SSRN Electronic Journal`; key says 2020. No metadata correction required unless key hygiene matters. | `@article` acceptable for SSRN Electronic Journal / high |
| `lamorgia2023doge` | Confirmed | [DOI](https://doi.org/10.1145/3561300), [DBLP](https://dblp.org/rec/journals/toit/MorgiaMSS23), [Sapienza record](https://iris.uniroma1.it/handle/11573/1673225) | Core metadata matches. Crossref gives pages 1--28; ACM/DBLP-style article pagination supports local `11:1--11:28`. | `@article` correct / high |
| `makarov2020trading` | Confirmed | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0304405X19301746), [DOI](https://doi.org/10.1016/j.jfineco.2019.07.001) | Metadata matches. | `@article` correct / high |
| `roll1984simple` | Confirmed | [DOI](https://doi.org/10.1111/j.1540-6261.1984.tb03897.x), [CiNii/Crossref](https://cir.nii.ac.jp/crid/1363670319131044480) | Metadata matches. Sentence-case title is stylistically acceptable. | `@article` correct / high |
| `arms1994volume` | Unresolved/partial | [NLA 1983 catalog](https://catalogue.nla.gov.au/catalog/828793), [Google Books 1983](https://books.google.com/books/about/Volume_cycles_in_the_stock_market.html?id=BXvQAAAAIAAJ), [AbeBooks 1994 ISBN page](https://www.abebooks.com/9781885439000/Volume-Cycles-Stock-Market-Timing-1885439008/plp) | Strong library evidence confirms a 1983 Dow Jones-Irwin edition with subtitle and ISBN `9780870944055`; 1994 Equis edition with ISBN `9781885439000` is supported mainly by bookseller metadata. Do not silently change without deciding which edition was used. | `@book` correct / medium-low |
| `parkinson1980extreme` | Confirmed | [DOI](https://doi.org/10.1086/296071), [RePEc](https://ideas.repec.org/a/ucp/jnlbus/v53y1980i1p61-65.html) | Metadata matches. Crossref may truncate page field to `61`; RePEc and citation sources support `61--65`. | `@article` correct / high |
| `vanderweele2017sensitivity` | Confirmed with minor correction | [DOI](https://doi.org/10.7326/M16-2607), [Harvard DASH](https://dash.harvard.edu/entities/publication/73120378-fbd5-6bd4-e053-0100007fdf3b), [EPA HERO](https://hero.epa.gov/hero/index.cfm/reference/details/reference_id/5381254) | Metadata matches. Official title styling uses `E-Value`; local title has `{E}-value`. Correcting title capitalization is strongly supported but minor. | `@article` correct / high |
| `xgboost2016` | Confirmed | [DOI](https://doi.org/10.1145/2939672.2939785), [DBLP](https://dblp.org/rec/conf/kdd/ChenG16), [ACM/CoLab metadata](https://colab.ws/articles/10.1145%2F2939672.2939785) | Metadata matches. Optional: add `series = {KDD '16}` and URL. | `@inproceedings` correct / high |
| `lightgbm2017` | Confirmed with correction | [NeurIPS page](https://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree), [NeurIPS metadata](https://papers.nips.cc/paper_files/paper/2017/file/6449f44a102fde848669bdd9eb6b76fa-Metadata.json) | Entry lacks pages, publisher, URL, and editors. Official NeurIPS metadata gives pages `3146--3154` and publisher `Curran Associates, Inc.`. | `@inproceedings` correct / high |
| `optuna2019` | Confirmed with minor correction | [DOI](https://doi.org/10.1145/3292500.3330701), [DBLP](https://dblp.org/rec/conf/kdd/AkibaSYOK19), [ACM/Crossref metadata](https://api.crossref.org/works/10.1145%2F3292500.3330701) | Booktitle should use `Knowledge Discovery \& Data Mining`; local uses `and`. Title capitalization `Next-generation` is supported by ACM/Crossref. | `@inproceedings` correct / high |
| `allen1992stock` | Confirmed | [Oxford Academic](https://academic.oup.com/rfs/article-abstract/5/3/503/1576822), [DOI](https://doi.org/10.1093/rfs/5.3.503) | Metadata matches. Title case differs only. | `@article` correct / high |
| `aggarwal2006stock` | Confirmed | [DOI](https://doi.org/10.1086/503652), [CoLab metadata](https://colab.ws/articles/10.1086/503652) | Local pages `1915--1953` match Crossref/UChicago; some RePEc-like sources report `1915--1954`, likely a secondary-source discrepancy. | `@article` correct / high |
| `khwaja2005unchecked` | Confirmed | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0304405X0500053X), [Princeton](https://collaborate.princeton.edu/en/publications/unchecked-intermediaries-price-manipulation-in-an-emerging-stock-), [Harvard Kennedy School](https://www.hks.harvard.edu/publications/unchecked-intermediaries-price-manipulation-emerging-stock-market) | Metadata matches. | `@article` correct / high |
| `vanbommel2003rumors` | Confirmed with name-case caveat | [DOI](https://doi.org/10.1111/1540-6261.00575), [RePEc](https://ideas.repec.org/a/bla/jfinan/v58y2003i4p1499-1520.html), [Zendy metadata](https://zendy.io/title/10.1111/1540-6261.00575) | Metadata matches. Sources vary between `Van Bommel` and `van Bommel`; keep current unless style policy requires surname-particle normalization. | `@article` correct / high metadata, medium name casing |
| `sabherwal2011internet` | Confirmed with correction | [RePEc](https://ideas.repec.org/a/bla/jbfnac/v38y2011i9-10p1209-1237.html), [DOI](https://doi.org/10.1111/j.1468-5957.2011.02258.x), [ResearchGate metadata](https://www.researchgate.net/publication/228280351_Do_Internet_Stock_Message_Boards_Influence_Trading_Evidence_from_Heavily_Discussed_Stocks_with_No_Fundamental_News) | Official title capitalizes `Internet`; preserve with `{Internet}` in BibTeX. | `@article` correct / high |
| `mirtaheri2021identifying` | Confirmed | [DOI](https://doi.org/10.1109/TCSS.2021.3059286), [DBLP](https://dblp.org/rec/journals/tcss/MirtaheriAMSG21), [Scinapse metadata](https://www.scinapse.io/papers/3134685772) | Metadata matches. `Ver Steeg, Greg` is a safe BibTeX surname form. | `@article` correct / high |
| `dhawan2023new` | Confirmed with year note | [Oxford Academic](https://academic.oup.com/rof/article/27/3/935/6655707), [DOI](https://doi.org/10.1093/rof/rfac051) | Issue citation is 2023, volume 27(3), pages 935--975; online publication was 2022-08-04. Local `year = {2023}` is defensible for final issue citation. | `@article` correct / high |
| `hu2023sequence` | Confirmed with article-number caveat | [DOI](https://doi.org/10.1145/3588686), [DBLP](https://dblp.uni-trier.de/rec/journals/pacmmod/HuZLHL23.html), [NUS project page](https://www.aidf.nus.edu.sg/research/research-projects/ai-data-driven-insights/) | Crossref gives pages `1--19`; DBLP gives ACM-style `6:1--6:19`. Local `1--19` is acceptable, but `articleno = {6}` or `pages = {6:1--6:19}` would be more ACM-style. | `@article` correct / high core metadata |
| `fu2025perseus` | Confirmed | [arXiv](https://arxiv.org/abs/2503.01686), [DOI](https://doi.org/10.48550/arXiv.2503.01686), [RePEc](https://ideas.repec.org/p/arx/papers/2503.01686.html) | Metadata matches. `primaryClass = {cs.CY}` is correct; arXiv also lists secondary classes `cs.LG` and `q-fin.TR`. | `@misc` arXiv preprint appropriate / high |

## Duplicate and Conflict Check

- Duplicate keys: none found.
- Duplicate works under different keys: none found.
- Related but distinct entries:
  - `lamorgia2020pump` and `lamorgia2023doge` share authors and topic but are distinct conference and journal works.
  - `li2021cryptocurrency`, `victor2019cryptocurrency`, and `xu2019anatomy` have similar pump-and-dump titles but are distinct works.
  - `abadie2010synthetic` and `abadie2021synthetic` are distinct synthetic-control publications.
- Conflicting metadata:
  - `li2021cryptocurrency`: key year conflicts with final publication year 2025.
  - `alexander2020critical`: key year conflicts with SSRN date/year 2019.
  - `aggarwal2006stock`: some secondary sources show final page 1954, but DOI/Crossref/UChicago-supported metadata supports 1953; current entry is likely correct.
  - `vanbommel2003rumors`: name-particle casing varies across sources; current form is acceptable.
  - `arms1994volume`: exact edition remains uncertain; see unresolved section.

## Corrected BibTeX Entries

Only entries with strong evidence are included here. These are suggested replacements or targeted corrections; no file changes were made.

```bibtex
@misc{econml,
  author       = {Battocchi, Keith and Dillon, Eleanor and Hei, Maggie and Lewis, Greg and Oka, Paul and Oprescu, Miruna and Syrgkanis, Vasilis},
  title        = {{EconML}: {A Python Package for ML-Based Heterogeneous Treatment Effects Estimation}},
  howpublished = {\url{https://github.com/py-why/EconML}},
  note         = {Version 0.x},
  year         = {2019}
}
```

```bibtex
@article{barabasi1999emergence,
  title     = {{Emergence of Scaling in Random Networks}},
  author    = {Barab{\'a}si, Albert-L{\'a}szl{\'o} and Albert, R{\'e}ka},
  journal   = {Science},
  year      = {1999},
  volume    = {286},
  number    = {5439},
  pages     = {509--512},
  doi       = {10.1126/science.286.5439.509},
  publisher = {American Association for the Advancement of Science}
}
```

```bibtex
@article{gandal2018price,
  title     = {{Price Manipulation in the Bitcoin Ecosystem}},
  author    = {Gandal, Neil and Hamrick, JT and Moore, Tyler and Oberman, Tali},
  journal   = {Journal of Monetary Economics},
  year      = {2018},
  volume    = {95},
  pages     = {86--96},
  doi       = {10.1016/j.jmoneco.2017.12.004},
  publisher = {Elsevier}
}
```

```bibtex
@article{liu2021risks,
  title     = {{Risks and Returns of Cryptocurrency}},
  author    = {Liu, Yukun and Tsyvinski, Aleh},
  journal   = {The Review of Financial Studies},
  year      = {2021},
  volume    = {34},
  number    = {6},
  pages     = {2689--2727},
  doi       = {10.1093/rfs/hhaa113},
  publisher = {Oxford University Press}
}
```

```bibtex
@inproceedings{lightgbm2017,
  title     = {{LightGBM}: A Highly Efficient Gradient Boosting Decision Tree},
  author    = {Ke, Guolin and Meng, Qi and Finley, Thomas and Wang, Taifeng and Chen, Wei and Ma, Weidong and Ye, Qiwei and Liu, Tie-Yan},
  booktitle = {Advances in Neural Information Processing Systems},
  editor    = {Guyon, I. and von Luxburg, U. and Bengio, S. and Wallach, H. and Fergus, R. and Vishwanathan, S. and Garnett, R.},
  volume    = {30},
  pages     = {3146--3154},
  publisher = {Curran Associates, Inc.},
  year      = {2017},
  url       = {https://proceedings.neurips.cc/paper_files/paper/2017/hash/6449f44a102fde848669bdd9eb6b76fa-Abstract.html}
}
```

```bibtex
@inproceedings{optuna2019,
  title     = {{Optuna}: A Next-generation Hyperparameter Optimization Framework},
  author    = {Akiba, Takuya and Sano, Shotaro and Yanase, Toshihiko and Ohta, Takeru and Koyama, Masanori},
  booktitle = {Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery \& Data Mining},
  series    = {KDD '19},
  year      = {2019},
  month     = jul,
  pages     = {2623--2631},
  publisher = {ACM},
  doi       = {10.1145/3292500.3330701},
  url       = {https://dl.acm.org/doi/10.1145/3292500.3330701}
}
```

```bibtex
@article{sabherwal2011internet,
  title   = {Do {Internet} stock message boards influence trading? Evidence from heavily discussed stocks with no fundamental news},
  author  = {Sabherwal, Sanjiv and Sarkar, Salil K. and Zhang, Ying},
  journal = {Journal of Business Finance \& Accounting},
  year    = {2011},
  volume  = {38},
  number  = {9--10},
  pages   = {1209--1237},
  doi     = {10.1111/j.1468-5957.2011.02258.x}
}
```

```bibtex
@article{vanderweele2017sensitivity,
  title   = {Sensitivity Analysis in Observational Research: Introducing the {E}-Value},
  author  = {VanderWeele, Tyler J. and Ding, Peng},
  journal = {Annals of Internal Medicine},
  year    = {2017},
  volume  = {167},
  number  = {4},
  pages   = {268--274},
  doi     = {10.7326/M16-2607}
}
```

## Unresolved or Ambiguous Cases

- `ccxt2023`: source exists, but the citation is not versioned. The current repository and PyPI metadata have moved far beyond 2023, so the exact cited state cannot be confirmed from the entry alone.
- `telethon2023`: source exists, but the GitHub repository is currently archived and moved to Codeberg. The entry is not pinned to a version or release date, so the exact cited state cannot be confirmed from the entry alone.
- `coinmarketcap2024api`: the documentation exists, but the `/v1/` URL redirects to the current docs. I found no strong evidence for 2024 as the bibliographic year.
- `arms1994volume`: the 1994 Equis edition appears to exist with ISBN `9781885439000`, but high-authority library metadata was stronger for the 1983 Dow Jones-Irwin edition. The correct fix depends on which edition the thesis used.
- `hu2023sequence`: core metadata is confirmed, but ACM-style article numbering differs by source (`1--19` in Crossref, `6:1--6:19` in DBLP). This is a style/fielding issue rather than an existence problem.
- `kamps2018pump`: source uses article number 18; keeping `pages = {18}` is common, but an article-number field would be more semantically precise if the bibliography style supports it.

