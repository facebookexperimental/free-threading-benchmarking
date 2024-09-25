# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.47x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 698 ms: 1.57x slower                                  |
| docutils       | 4.01 sec                                                     | 5.02 sec: 1.25x slower                                |
| html5lib       | 92.6 ms                                                      | 149 ms: 1.61x slower                                  |
| tornado_http   | 251 ms                                                       | 429 ms: 1.71x slower                                  |
| Geometric mean | (ref)                                                        | 1.52x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.19 sec: 1.18x faster                                |
| asyncio_websockets      | 766 ms                                                       | 795 ms: 1.04x slower                                  |
| async_tree_memoization  | 709 ms                                                       | 759 ms: 1.07x slower                                  |
| async_tree_none         | 572 ms                                                       | 614 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed | 889 ms                                                       | 974 ms: 1.10x slower                                  |
| asyncio_tcp             | 948 ms                                                       | 1.12 sec: 1.18x slower                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.41 sec: 1.23x slower                                |
| async_generators        | 567 ms                                                       | 763 ms: 1.35x slower                                  |
| coroutines              | 30.9 ms                                                      | 43.6 ms: 1.41x slower                                 |
| Geometric mean          | (ref)                                                        | 1.08x slower                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 251 ms                                                       | 275 ms: 1.09x slower                                  |
| float          | 116 ms                                                       | 191 ms: 1.64x slower                                  |
| nbody          | 119 ms                                                       | 317 ms: 2.67x slower                                  |
| Geometric mean | (ref)                                                        | 1.69x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 297 ms: 1.05x slower                                  |
| regex_v8       | 32.8 ms                                                      | 36.7 ms: 1.12x slower                                 |
| regex_compile  | 182 ms                                                       | 303 ms: 1.66x slower                                  |
| Geometric mean | (ref)                                                        | 1.19x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle             | 20.5 us                                                      | 23.1 us: 1.13x slower                                 |
| unpickle_list        | 6.68 us                                                      | 7.97 us: 1.19x slower                                 |
| json_dumps           | 14.1 ms                                                      | 17.9 ms: 1.27x slower                                 |
| json_loads           | 34.3 us                                                      | 48.4 us: 1.41x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 180 ms: 1.47x slower                                  |
| xml_etree_process    | 85.9 ms                                                      | 133 ms: 1.55x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.36 sec: 1.57x slower                                |
| unpickle_pure_python | 290 us                                                       | 574 us: 1.98x slower                                  |
| pickle_pure_python   | 416 us                                                       | 910 us: 2.18x slower                                  |
| Geometric mean       | (ref)                                                        | 1.30x slower                                          |

Benchmark hidden because not significant (5): pickle_dict, pickle_list, xml_etree_iterparse, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 31.2 ms: 1.39x slower                                 |
| python_startup_no_site | 15.3 ms                                                      | 22.7 ms: 1.48x slower                                 |
| Geometric mean         | (ref)                                                        | 1.44x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 118 ms: 1.64x slower                                  |
| django_template | 44.3 ms                                                      | 80.8 ms: 1.82x slower                                 |
| genshi_text     | 31.7 ms                                                      | 59.2 ms: 1.87x slower                                 |
| mako            | 15.9 ms                                                      | 30.6 ms: 1.92x slower                                 |
| Geometric mean  | (ref)                                                        | 1.81x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.95 ms: 1.24x faster                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.19 sec: 1.18x faster                                |
| gc_traversal             | 5.70 ms                                                      | 5.18 ms: 1.10x faster                                 |
| asyncio_websockets       | 766 ms                                                       | 795 ms: 1.04x slower                                  |
| regex_dna                | 282 ms                                                       | 297 ms: 1.05x slower                                  |
| async_tree_memoization   | 709 ms                                                       | 759 ms: 1.07x slower                                  |
| async_tree_none          | 572 ms                                                       | 614 ms: 1.07x slower                                  |
| sqlite_synth             | 3.99 us                                                      | 4.35 us: 1.09x slower                                 |
| pidigits                 | 251 ms                                                       | 275 ms: 1.09x slower                                  |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 974 ms: 1.10x slower                                  |
| regex_v8                 | 32.8 ms                                                      | 36.7 ms: 1.12x slower                                 |
| unpickle                 | 20.5 us                                                      | 23.1 us: 1.13x slower                                 |
| telco                    | 12.2 ms                                                      | 14.1 ms: 1.16x slower                                 |
| asyncio_tcp              | 948 ms                                                       | 1.12 sec: 1.18x slower                                |
| unpickle_list            | 6.68 us                                                      | 7.97 us: 1.19x slower                                 |
| deepcopy                 | 498 us                                                       | 596 us: 1.20x slower                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.41 sec: 1.23x slower                                |
| pylint                   | 470 ms                                                       | 586 ms: 1.25x slower                                  |
| docutils                 | 4.01 sec                                                     | 5.02 sec: 1.25x slower                                |
| pathlib                  | 29.9 ms                                                      | 37.5 ms: 1.25x slower                                 |
| json_dumps               | 14.1 ms                                                      | 17.9 ms: 1.27x slower                                 |
| generators               | 40.0 ms                                                      | 53.0 ms: 1.33x slower                                 |
| async_generators         | 567 ms                                                       | 763 ms: 1.35x slower                                  |
| json                     | 6.51 ms                                                      | 8.77 ms: 1.35x slower                                 |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.11 ms: 1.35x slower                                 |
| meteor_contest           | 150 ms                                                       | 203 ms: 1.35x slower                                  |
| scimark_fft              | 473 ms                                                       | 642 ms: 1.36x slower                                  |
| deepcopy_reduce          | 4.10 us                                                      | 5.58 us: 1.36x slower                                 |
| mdp                      | 3.80 sec                                                     | 5.29 sec: 1.39x slower                                |
| python_startup           | 22.4 ms                                                      | 31.2 ms: 1.39x slower                                 |
| pycparser                | 1.57 sec                                                     | 2.21 sec: 1.41x slower                                |
| coroutines               | 30.9 ms                                                      | 43.6 ms: 1.41x slower                                 |
| json_loads               | 34.3 us                                                      | 48.4 us: 1.41x slower                                 |
| deepcopy_memo            | 50.1 us                                                      | 70.9 us: 1.42x slower                                 |
| coverage                 | 107 ms                                                       | 152 ms: 1.42x slower                                  |
| fannkuch                 | 547 ms                                                       | 786 ms: 1.44x slower                                  |
| xml_etree_generate       | 122 ms                                                       | 180 ms: 1.47x slower                                  |
| python_startup_no_site   | 15.3 ms                                                      | 22.7 ms: 1.48x slower                                 |
| crypto_pyaes             | 100 ms                                                       | 150 ms: 1.50x slower                                  |
| thrift                   | 1.10 ms                                                      | 1.70 ms: 1.54x slower                                 |
| xml_etree_process        | 85.9 ms                                                      | 133 ms: 1.55x slower                                  |
| spectral_norm            | 157 ms                                                       | 245 ms: 1.56x slower                                  |
| 2to3                     | 445 ms                                                       | 698 ms: 1.57x slower                                  |
| tomli_loads              | 2.78 sec                                                     | 4.36 sec: 1.57x slower                                |
| nqueens                  | 112 ms                                                       | 175 ms: 1.57x slower                                  |
| typing_runtime_protocols | 226 us                                                       | 355 us: 1.57x slower                                  |
| sympy_integrate          | 30.2 ms                                                      | 48.4 ms: 1.60x slower                                 |
| html5lib                 | 92.6 ms                                                      | 149 ms: 1.61x slower                                  |
| bench_thread_pool        | 2.89 ms                                                      | 4.67 ms: 1.62x slower                                 |
| genshi_xml               | 72.1 ms                                                      | 118 ms: 1.64x slower                                  |
| richards                 | 65.5 ms                                                      | 107 ms: 1.64x slower                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.3 sec: 1.64x slower                                |
| float                    | 116 ms                                                       | 191 ms: 1.64x slower                                  |
| regex_compile            | 182 ms                                                       | 303 ms: 1.66x slower                                  |
| pyflate                  | 664 ms                                                       | 1.13 sec: 1.71x slower                                |
| tornado_http             | 251 ms                                                       | 429 ms: 1.71x slower                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 128 ms: 1.71x slower                                  |
| sqlglot_normalize        | 140 ms                                                       | 240 ms: 1.72x slower                                  |
| logging_simple           | 8.56 us                                                      | 14.9 us: 1.74x slower                                 |
| comprehensions           | 22.2 us                                                      | 39.5 us: 1.77x slower                                 |
| pprint_safe_repr         | 987 ms                                                       | 1.77 sec: 1.79x slower                                |
| django_template          | 44.3 ms                                                      | 80.8 ms: 1.82x slower                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.57 sec: 1.84x slower                                |
| richards_super           | 73.2 ms                                                      | 137 ms: 1.87x slower                                  |
| genshi_text              | 31.7 ms                                                      | 59.2 ms: 1.87x slower                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 170 ms: 1.88x slower                                  |
| mako                     | 15.9 ms                                                      | 30.6 ms: 1.92x slower                                 |
| sympy_str                | 379 ms                                                       | 730 ms: 1.93x slower                                  |
| logging_format           | 9.24 us                                                      | 17.9 us: 1.93x slower                                 |
| unpickle_pure_python     | 290 us                                                       | 574 us: 1.98x slower                                  |
| scimark_sor              | 179 ms                                                       | 354 ms: 1.98x slower                                  |
| hexiom                   | 8.11 ms                                                      | 16.3 ms: 2.01x slower                                 |
| logging_silent           | 130 ns                                                       | 267 ns: 2.05x slower                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.53 ms: 2.06x slower                                 |
| chaos                    | 83.6 ms                                                      | 175 ms: 2.10x slower                                  |
| sqlglot_parse            | 1.76 ms                                                      | 3.81 ms: 2.17x slower                                 |
| sympy_expand             | 601 ms                                                       | 1.31 sec: 2.18x slower                                |
| pickle_pure_python       | 416 us                                                       | 910 us: 2.18x slower                                  |
| scimark_lu               | 146 ms                                                       | 330 ms: 2.26x slower                                  |
| go                       | 191 ms                                                       | 452 ms: 2.36x slower                                  |
| raytrace                 | 344 ms                                                       | 816 ms: 2.37x slower                                  |
| sympy_sum                | 210 ms                                                       | 509 ms: 2.42x slower                                  |
| deltablue                | 4.44 ms                                                      | 11.3 ms: 2.54x slower                                 |
| unpack_sequence          | 74.3 ns                                                      | 191 ns: 2.57x slower                                  |
| nbody                    | 119 ms                                                       | 317 ms: 2.67x slower                                  |
| Geometric mean           | (ref)                                                        | 1.47x slower                                          |

Benchmark hidden because not significant (11): bench_mp_pool, async_tree_memoization_tg, async_tree_io, pickle_dict, pickle_list, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, regex_effbot, async_tree_none_tg, xml_etree_parse, pickle
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.15x