# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 664 ms: 1.49x slower                                  |
| docutils       | 4.01 sec                                                     | 4.86 sec: 1.21x slower                                |
| html5lib       | 92.6 ms                                                      | 157 ms: 1.69x slower                                  |
| tornado_http   | 251 ms                                                       | 320 ms: 1.27x slower                                  |
| Geometric mean | (ref)                                                        | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| async_tree_io           | 1.39 sec                                                     | 1.22 sec: 1.14x faster                                |
| async_tree_cpu_io_mixed | 889 ms                                                       | 945 ms: 1.06x slower                                  |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.27 sec: 1.18x slower                                |
| asyncio_tcp             | 948 ms                                                       | 1.12 sec: 1.19x slower                                |
| async_generators        | 567 ms                                                       | 724 ms: 1.28x slower                                  |
| coroutines              | 30.9 ms                                                      | 45.6 ms: 1.48x slower                                 |
| Geometric mean          | (ref)                                                        | 1.06x slower                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 200 ms: 1.73x slower                                  |
| nbody          | 119 ms                                                       | 283 ms: 2.38x slower                                  |
| Geometric mean | (ref)                                                        | 1.59x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 301 ms: 1.07x slower                                  |
| regex_compile  | 182 ms                                                       | 292 ms: 1.60x slower                                  |
| Geometric mean | (ref)                                                        | 1.16x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 42.9 us: 1.10x faster                                 |
| xml_etree_parse      | 231 ms                                                       | 213 ms: 1.09x faster                                  |
| xml_etree_iterparse  | 177 ms                                                       | 164 ms: 1.08x faster                                  |
| pickle_list          | 6.86 us                                                      | 6.45 us: 1.06x faster                                 |
| pickle               | 15.1 us                                                      | 14.3 us: 1.06x faster                                 |
| unpickle_list        | 6.68 us                                                      | 7.21 us: 1.08x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 158 ms: 1.29x slower                                  |
| json_loads           | 34.3 us                                                      | 45.2 us: 1.32x slower                                 |
| json_dumps           | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                 |
| xml_etree_process    | 85.9 ms                                                      | 124 ms: 1.44x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.14 sec: 1.49x slower                                |
| pickle_pure_python   | 416 us                                                       | 760 us: 1.83x slower                                  |
| unpickle_pure_python | 290 us                                                       | 540 us: 1.86x slower                                  |
| Geometric mean       | (ref)                                                        | 1.20x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.5 ms: 1.32x slower                                 |
| python_startup_no_site | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 122 ms: 1.69x slower                                  |
| genshi_text     | 31.7 ms                                                      | 55.7 ms: 1.76x slower                                 |
| django_template | 44.3 ms                                                      | 84.5 ms: 1.91x slower                                 |
| mako            | 15.9 ms                                                      | 31.9 ms: 2.00x slower                                 |
| Geometric mean  | (ref)                                                        | 1.84x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool            | 18.7 ms                                                      | 13.3 ms: 1.40x faster                                 |
| create_gc_cycles         | 2.41 ms                                                      | 1.82 ms: 1.32x faster                                 |
| gc_traversal             | 5.70 ms                                                      | 4.60 ms: 1.24x faster                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| async_tree_io            | 1.39 sec                                                     | 1.22 sec: 1.14x faster                                |
| pickle_dict              | 47.2 us                                                      | 42.9 us: 1.10x faster                                 |
| xml_etree_parse          | 231 ms                                                       | 213 ms: 1.09x faster                                  |
| xml_etree_iterparse      | 177 ms                                                       | 164 ms: 1.08x faster                                  |
| pickle_list              | 6.86 us                                                      | 6.45 us: 1.06x faster                                 |
| pickle                   | 15.1 us                                                      | 14.3 us: 1.06x faster                                 |
| sqlite_synth             | 3.99 us                                                      | 4.23 us: 1.06x slower                                 |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 945 ms: 1.06x slower                                  |
| regex_dna                | 282 ms                                                       | 301 ms: 1.07x slower                                  |
| unpickle_list            | 6.68 us                                                      | 7.21 us: 1.08x slower                                 |
| pathlib                  | 29.9 ms                                                      | 32.6 ms: 1.09x slower                                 |
| telco                    | 12.2 ms                                                      | 13.4 ms: 1.10x slower                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.27 sec: 1.18x slower                                |
| asyncio_tcp              | 948 ms                                                       | 1.12 sec: 1.19x slower                                |
| deepcopy                 | 498 us                                                       | 594 us: 1.19x slower                                  |
| docutils                 | 4.01 sec                                                     | 4.86 sec: 1.21x slower                                |
| pylint                   | 470 ms                                                       | 582 ms: 1.24x slower                                  |
| tornado_http             | 251 ms                                                       | 320 ms: 1.27x slower                                  |
| async_generators         | 567 ms                                                       | 724 ms: 1.28x slower                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.70 ms: 1.29x slower                                 |
| xml_etree_generate       | 122 ms                                                       | 158 ms: 1.29x slower                                  |
| scimark_fft              | 473 ms                                                       | 617 ms: 1.30x slower                                  |
| python_startup           | 22.4 ms                                                      | 29.5 ms: 1.32x slower                                 |
| json_loads               | 34.3 us                                                      | 45.2 us: 1.32x slower                                 |
| json                     | 6.51 ms                                                      | 8.61 ms: 1.32x slower                                 |
| meteor_contest           | 150 ms                                                       | 199 ms: 1.32x slower                                  |
| json_dumps               | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                 |
| mdp                      | 3.80 sec                                                     | 5.10 sec: 1.34x slower                                |
| nqueens                  | 112 ms                                                       | 152 ms: 1.36x slower                                  |
| python_startup_no_site   | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                 |
| generators               | 40.0 ms                                                      | 54.9 ms: 1.37x slower                                 |
| pycparser                | 1.57 sec                                                     | 2.16 sec: 1.38x slower                                |
| deepcopy_memo            | 50.1 us                                                      | 69.7 us: 1.39x slower                                 |
| bench_thread_pool        | 2.89 ms                                                      | 4.01 ms: 1.39x slower                                 |
| coverage                 | 107 ms                                                       | 151 ms: 1.41x slower                                  |
| deepcopy_reduce          | 4.10 us                                                      | 5.85 us: 1.43x slower                                 |
| fannkuch                 | 547 ms                                                       | 783 ms: 1.43x slower                                  |
| xml_etree_process        | 85.9 ms                                                      | 124 ms: 1.44x slower                                  |
| sympy_integrate          | 30.2 ms                                                      | 43.9 ms: 1.45x slower                                 |
| coroutines               | 30.9 ms                                                      | 45.6 ms: 1.48x slower                                 |
| tomli_loads              | 2.78 sec                                                     | 4.14 sec: 1.49x slower                                |
| dulwich_log              | 93.7 ms                                                      | 140 ms: 1.49x slower                                  |
| 2to3                     | 445 ms                                                       | 664 ms: 1.49x slower                                  |
| typing_runtime_protocols | 226 us                                                       | 342 us: 1.51x slower                                  |
| crypto_pyaes             | 100 ms                                                       | 157 ms: 1.57x slower                                  |
| spectral_norm            | 157 ms                                                       | 247 ms: 1.58x slower                                  |
| thrift                   | 1.10 ms                                                      | 1.75 ms: 1.59x slower                                 |
| regex_compile            | 182 ms                                                       | 292 ms: 1.60x slower                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.1 sec: 1.61x slower                                |
| sqlglot_normalize        | 140 ms                                                       | 230 ms: 1.65x slower                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 124 ms: 1.66x slower                                  |
| genshi_xml               | 72.1 ms                                                      | 122 ms: 1.69x slower                                  |
| html5lib                 | 92.6 ms                                                      | 157 ms: 1.69x slower                                  |
| pyflate                  | 664 ms                                                       | 1.13 sec: 1.71x slower                                |
| richards                 | 65.5 ms                                                      | 112 ms: 1.71x slower                                  |
| comprehensions           | 22.2 us                                                      | 38.3 us: 1.72x slower                                 |
| float                    | 116 ms                                                       | 200 ms: 1.73x slower                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.71 sec: 1.74x slower                                |
| genshi_text              | 31.7 ms                                                      | 55.7 ms: 1.76x slower                                 |
| logging_simple           | 8.56 us                                                      | 15.2 us: 1.78x slower                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 163 ms: 1.80x slower                                  |
| logging_format           | 9.24 us                                                      | 16.6 us: 1.80x slower                                 |
| sympy_str                | 379 ms                                                       | 685 ms: 1.81x slower                                  |
| richards_super           | 73.2 ms                                                      | 133 ms: 1.81x slower                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.55 sec: 1.83x slower                                |
| pickle_pure_python       | 416 us                                                       | 760 us: 1.83x slower                                  |
| unpickle_pure_python     | 290 us                                                       | 540 us: 1.86x slower                                  |
| logging_silent           | 130 ns                                                       | 246 ns: 1.89x slower                                  |
| scimark_sor              | 179 ms                                                       | 341 ms: 1.91x slower                                  |
| django_template          | 44.3 ms                                                      | 84.5 ms: 1.91x slower                                 |
| mako                     | 15.9 ms                                                      | 31.9 ms: 2.00x slower                                 |
| hexiom                   | 8.11 ms                                                      | 16.7 ms: 2.06x slower                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.58 ms: 2.09x slower                                 |
| chaos                    | 83.6 ms                                                      | 175 ms: 2.09x slower                                  |
| sympy_expand             | 601 ms                                                       | 1.27 sec: 2.11x slower                                |
| scimark_lu               | 146 ms                                                       | 314 ms: 2.14x slower                                  |
| go                       | 191 ms                                                       | 411 ms: 2.15x slower                                  |
| sympy_sum                | 210 ms                                                       | 476 ms: 2.26x slower                                  |
| sqlglot_parse            | 1.76 ms                                                      | 3.99 ms: 2.27x slower                                 |
| raytrace                 | 344 ms                                                       | 807 ms: 2.34x slower                                  |
| nbody                    | 119 ms                                                       | 283 ms: 2.38x slower                                  |
| deltablue                | 4.44 ms                                                      | 11.4 ms: 2.57x slower                                 |
| unpack_sequence          | 74.3 ns                                                      | 200 ns: 2.69x slower                                  |
| Geometric mean           | (ref)                                                        | 1.41x slower                                          |

Benchmark hidden because not significant (10): pidigits, async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, regex_effbot, regex_v8, unpickle, async_tree_memoization, async_tree_none
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x