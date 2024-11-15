# Results vs. 3.13.0rc2

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 656 ms: 1.47x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.56 sec: 1.14x slower                                                 |
| html5lib       | 92.6 ms                                                      | 135 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 948 ms                                                       | 1.05 sec: 1.11x slower                                                 |
| asyncio_tcp_ssl  | 2.77 sec                                                     | 3.33 sec: 1.20x slower                                                 |
| async_generators | 567 ms                                                       | 713 ms: 1.26x slower                                                   |
| coroutines       | 30.9 ms                                                      | 39.9 ms: 1.29x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 190 ms: 1.64x slower                                                   |
| nbody          | 119 ms                                                       | 250 ms: 2.11x slower                                                   |
| Geometric mean | (ref)                                                        | 1.50x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 295 ms: 1.05x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 38.8 ms: 1.18x slower                                                  |
| regex_compile  | 182 ms                                                       | 290 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 157 ms: 1.12x faster                                                   |
| pickle_dict          | 47.2 us                                                      | 43.2 us: 1.09x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 217 ms: 1.06x faster                                                   |
| pickle               | 15.1 us                                                      | 16.0 us: 1.06x slower                                                  |
| json_loads           | 34.3 us                                                      | 39.3 us: 1.15x slower                                                  |
| unpickle             | 20.5 us                                                      | 23.7 us: 1.15x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.71 us: 1.15x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 157 ms: 1.28x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 19.3 ms: 1.36x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.11 sec: 1.48x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 129 ms: 1.51x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 761 us: 1.83x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 539 us: 1.86x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 111 ms: 1.54x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 53.0 ms: 1.68x slower                                                  |
| django_template | 44.3 ms                                                      | 81.0 ms: 1.83x slower                                                  |
| mako            | 15.9 ms                                                      | 30.9 ms: 1.94x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.74x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 3.97 ms: 1.44x faster                                                  |
| create_gc_cycles         | 2.41 ms                                                      | 1.85 ms: 1.30x faster                                                  |
| xml_etree_iterparse      | 177 ms                                                       | 157 ms: 1.12x faster                                                   |
| pickle_dict              | 47.2 us                                                      | 43.2 us: 1.09x faster                                                  |
| xml_etree_parse          | 231 ms                                                       | 217 ms: 1.06x faster                                                   |
| regex_dna                | 282 ms                                                       | 295 ms: 1.05x slower                                                   |
| pickle                   | 15.1 us                                                      | 16.0 us: 1.06x slower                                                  |
| pathlib                  | 29.9 ms                                                      | 32.1 ms: 1.07x slower                                                  |
| sqlite_synth             | 3.99 us                                                      | 4.37 us: 1.09x slower                                                  |
| asyncio_tcp              | 948 ms                                                       | 1.05 sec: 1.11x slower                                                 |
| json                     | 6.51 ms                                                      | 7.26 ms: 1.11x slower                                                  |
| telco                    | 12.2 ms                                                      | 13.8 ms: 1.13x slower                                                  |
| docutils                 | 4.01 sec                                                     | 4.56 sec: 1.14x slower                                                 |
| json_loads               | 34.3 us                                                      | 39.3 us: 1.15x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 7.79 ms: 1.15x slower                                                  |
| unpickle                 | 20.5 us                                                      | 23.7 us: 1.15x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 7.71 us: 1.15x slower                                                  |
| deepcopy                 | 498 us                                                       | 582 us: 1.17x slower                                                   |
| regex_v8                 | 32.8 ms                                                      | 38.8 ms: 1.18x slower                                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.33 sec: 1.20x slower                                                 |
| bench_thread_pool        | 2.89 ms                                                      | 3.53 ms: 1.22x slower                                                  |
| scimark_fft              | 473 ms                                                       | 590 ms: 1.25x slower                                                   |
| async_generators         | 567 ms                                                       | 713 ms: 1.26x slower                                                   |
| meteor_contest           | 150 ms                                                       | 190 ms: 1.27x slower                                                   |
| mdp                      | 3.80 sec                                                     | 4.86 sec: 1.28x slower                                                 |
| xml_etree_generate       | 122 ms                                                       | 157 ms: 1.28x slower                                                   |
| coroutines               | 30.9 ms                                                      | 39.9 ms: 1.29x slower                                                  |
| pylint                   | 470 ms                                                       | 616 ms: 1.31x slower                                                   |
| deepcopy_memo            | 50.1 us                                                      | 66.7 us: 1.33x slower                                                  |
| nqueens                  | 112 ms                                                       | 149 ms: 1.33x slower                                                   |
| deepcopy_reduce          | 4.10 us                                                      | 5.53 us: 1.35x slower                                                  |
| pycparser                | 1.57 sec                                                     | 2.13 sec: 1.35x slower                                                 |
| python_startup_no_site   | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                                  |
| json_dumps               | 14.1 ms                                                      | 19.3 ms: 1.36x slower                                                  |
| fannkuch                 | 547 ms                                                       | 748 ms: 1.37x slower                                                   |
| python_startup           | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                  |
| coverage                 | 107 ms                                                       | 150 ms: 1.40x slower                                                   |
| dulwich_log              | 93.7 ms                                                      | 133 ms: 1.41x slower                                                   |
| spectral_norm            | 157 ms                                                       | 222 ms: 1.42x slower                                                   |
| generators               | 40.0 ms                                                      | 56.7 ms: 1.42x slower                                                  |
| html5lib                 | 92.6 ms                                                      | 135 ms: 1.46x slower                                                   |
| bpe_tokeniser            | 6.28 sec                                                     | 9.21 sec: 1.46x slower                                                 |
| 2to3                     | 445 ms                                                       | 656 ms: 1.47x slower                                                   |
| tomli_loads              | 2.78 sec                                                     | 4.11 sec: 1.48x slower                                                 |
| sympy_integrate          | 30.2 ms                                                      | 44.8 ms: 1.48x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 149 ms: 1.48x slower                                                   |
| xml_etree_process        | 85.9 ms                                                      | 129 ms: 1.51x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 214 ms: 1.53x slower                                                   |
| genshi_xml               | 72.1 ms                                                      | 111 ms: 1.54x slower                                                   |
| sqlglot_optimize         | 74.7 ms                                                      | 115 ms: 1.55x slower                                                   |
| typing_runtime_protocols | 226 us                                                       | 351 us: 1.55x slower                                                   |
| thrift                   | 1.10 ms                                                      | 1.72 ms: 1.57x slower                                                  |
| pyflate                  | 664 ms                                                       | 1.04 sec: 1.57x slower                                                 |
| regex_compile            | 182 ms                                                       | 290 ms: 1.59x slower                                                   |
| float                    | 116 ms                                                       | 190 ms: 1.64x slower                                                   |
| scimark_monte_carlo      | 90.6 ms                                                      | 150 ms: 1.66x slower                                                   |
| pprint_safe_repr         | 987 ms                                                       | 1.65 sec: 1.67x slower                                                 |
| genshi_text              | 31.7 ms                                                      | 53.0 ms: 1.68x slower                                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.34 sec: 1.72x slower                                                 |
| comprehensions           | 22.2 us                                                      | 38.5 us: 1.73x slower                                                  |
| richards_super           | 73.2 ms                                                      | 127 ms: 1.74x slower                                                   |
| logging_simple           | 8.56 us                                                      | 15.0 us: 1.75x slower                                                  |
| richards                 | 65.5 ms                                                      | 115 ms: 1.76x slower                                                   |
| sympy_str                | 379 ms                                                       | 688 ms: 1.81x slower                                                   |
| pickle_pure_python       | 416 us                                                       | 761 us: 1.83x slower                                                   |
| django_template          | 44.3 ms                                                      | 81.0 ms: 1.83x slower                                                  |
| scimark_sor              | 179 ms                                                       | 327 ms: 1.83x slower                                                   |
| go                       | 191 ms                                                       | 353 ms: 1.84x slower                                                   |
| unpickle_pure_python     | 290 us                                                       | 539 us: 1.86x slower                                                   |
| chaos                    | 83.6 ms                                                      | 156 ms: 1.87x slower                                                   |
| mako                     | 15.9 ms                                                      | 30.9 ms: 1.94x slower                                                  |
| hexiom                   | 8.11 ms                                                      | 15.8 ms: 1.95x slower                                                  |
| logging_silent           | 130 ns                                                       | 255 ns: 1.96x slower                                                   |
| logging_format           | 9.24 us                                                      | 18.3 us: 1.97x slower                                                  |
| scimark_lu               | 146 ms                                                       | 290 ms: 1.98x slower                                                   |
| sqlglot_parse            | 1.76 ms                                                      | 3.68 ms: 2.10x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.26 sec: 2.10x slower                                                 |
| nbody                    | 119 ms                                                       | 250 ms: 2.11x slower                                                   |
| sympy_sum                | 210 ms                                                       | 457 ms: 2.18x slower                                                   |
| sqlglot_transpile        | 2.20 ms                                                      | 4.89 ms: 2.23x slower                                                  |
| raytrace                 | 344 ms                                                       | 776 ms: 2.25x slower                                                   |
| deltablue                | 4.44 ms                                                      | 11.6 ms: 2.60x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 197 ns: 2.66x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 59.4 ms: 3.18x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.45x slower                                                           |

Benchmark hidden because not significant (4): pidigits, pickle_list, asyncio_websockets, regex_effbot
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.41x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.19x