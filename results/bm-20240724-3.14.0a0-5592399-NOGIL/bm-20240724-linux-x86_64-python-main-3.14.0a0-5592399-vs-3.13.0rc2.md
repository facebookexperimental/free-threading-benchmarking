# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 662 ms: 1.49x slower                                  |
| docutils       | 4.01 sec                                                     | 4.97 sec: 1.24x slower                                |
| html5lib       | 92.6 ms                                                      | 137 ms: 1.48x slower                                  |
| tornado_http   | 251 ms                                                       | 339 ms: 1.35x slower                                  |
| Geometric mean | (ref)                                                        | 1.38x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| async_tree_io           | 1.39 sec                                                     | 1.27 sec: 1.09x faster                                |
| async_tree_memoization  | 709 ms                                                       | 759 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed | 889 ms                                                       | 959 ms: 1.08x slower                                  |
| asyncio_tcp             | 948 ms                                                       | 1.08 sec: 1.14x slower                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.42 sec: 1.23x slower                                |
| async_generators        | 567 ms                                                       | 721 ms: 1.27x slower                                  |
| coroutines              | 30.9 ms                                                      | 41.7 ms: 1.35x slower                                 |
| Geometric mean          | (ref)                                                        | 1.06x slower                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 211 ms: 1.82x slower                                  |
| nbody          | 119 ms                                                       | 278 ms: 2.34x slower                                  |
| Geometric mean | (ref)                                                        | 1.60x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 37.6 ms: 1.15x slower                                 |
| regex_compile  | 182 ms                                                       | 307 ms: 1.69x slower                                  |
| Geometric mean | (ref)                                                        | 1.19x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 208 ms: 1.11x faster                                  |
| pickle               | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| unpickle             | 20.5 us                                                      | 22.0 us: 1.07x slower                                 |
| unpickle_list        | 6.68 us                                                      | 7.97 us: 1.19x slower                                 |
| json_loads           | 34.3 us                                                      | 45.6 us: 1.33x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 164 ms: 1.34x slower                                  |
| json_dumps           | 14.1 ms                                                      | 19.0 ms: 1.34x slower                                 |
| xml_etree_process    | 85.9 ms                                                      | 127 ms: 1.48x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.32 sec: 1.55x slower                                |
| unpickle_pure_python | 290 us                                                       | 547 us: 1.88x slower                                  |
| pickle_pure_python   | 416 us                                                       | 801 us: 1.92x slower                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.3 ms: 1.26x slower                                 |
| python_startup         | 22.4 ms                                                      | 29.1 ms: 1.30x slower                                 |
| Geometric mean         | (ref)                                                        | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 53.7 ms: 1.70x slower                                 |
| genshi_xml      | 72.1 ms                                                      | 125 ms: 1.74x slower                                  |
| django_template | 44.3 ms                                                      | 86.4 ms: 1.95x slower                                 |
| mako            | 15.9 ms                                                      | 31.1 ms: 1.95x slower                                 |
| Geometric mean  | (ref)                                                        | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool            | 18.7 ms                                                      | 14.4 ms: 1.29x faster                                 |
| gc_traversal             | 5.70 ms                                                      | 4.51 ms: 1.27x faster                                 |
| create_gc_cycles         | 2.41 ms                                                      | 1.93 ms: 1.25x faster                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| xml_etree_parse          | 231 ms                                                       | 208 ms: 1.11x faster                                  |
| async_tree_io            | 1.39 sec                                                     | 1.27 sec: 1.09x faster                                |
| pickle                   | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| async_tree_memoization   | 709 ms                                                       | 759 ms: 1.07x slower                                  |
| unpickle                 | 20.5 us                                                      | 22.0 us: 1.07x slower                                 |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 959 ms: 1.08x slower                                  |
| sqlite_synth             | 3.99 us                                                      | 4.39 us: 1.10x slower                                 |
| deepcopy                 | 498 us                                                       | 556 us: 1.12x slower                                  |
| asyncio_tcp              | 948 ms                                                       | 1.08 sec: 1.14x slower                                |
| telco                    | 12.2 ms                                                      | 13.8 ms: 1.14x slower                                 |
| pathlib                  | 29.9 ms                                                      | 34.2 ms: 1.14x slower                                 |
| regex_v8                 | 32.8 ms                                                      | 37.6 ms: 1.15x slower                                 |
| unpickle_list            | 6.68 us                                                      | 7.97 us: 1.19x slower                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.42 sec: 1.23x slower                                |
| docutils                 | 4.01 sec                                                     | 4.97 sec: 1.24x slower                                |
| json                     | 6.51 ms                                                      | 8.11 ms: 1.25x slower                                 |
| pylint                   | 470 ms                                                       | 592 ms: 1.26x slower                                  |
| python_startup_no_site   | 15.3 ms                                                      | 19.3 ms: 1.26x slower                                 |
| async_generators         | 567 ms                                                       | 721 ms: 1.27x slower                                  |
| python_startup           | 22.4 ms                                                      | 29.1 ms: 1.30x slower                                 |
| scimark_fft              | 473 ms                                                       | 616 ms: 1.30x slower                                  |
| mdp                      | 3.80 sec                                                     | 4.96 sec: 1.30x slower                                |
| meteor_contest           | 150 ms                                                       | 198 ms: 1.32x slower                                  |
| json_loads               | 34.3 us                                                      | 45.6 us: 1.33x slower                                 |
| generators               | 40.0 ms                                                      | 53.4 ms: 1.33x slower                                 |
| xml_etree_generate       | 122 ms                                                       | 164 ms: 1.34x slower                                  |
| json_dumps               | 14.1 ms                                                      | 19.0 ms: 1.34x slower                                 |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.09 ms: 1.35x slower                                 |
| tornado_http             | 251 ms                                                       | 339 ms: 1.35x slower                                  |
| coroutines               | 30.9 ms                                                      | 41.7 ms: 1.35x slower                                 |
| coverage                 | 107 ms                                                       | 148 ms: 1.37x slower                                  |
| deepcopy_memo            | 50.1 us                                                      | 70.5 us: 1.41x slower                                 |
| pycparser                | 1.57 sec                                                     | 2.25 sec: 1.43x slower                                |
| dulwich_log              | 93.7 ms                                                      | 134 ms: 1.43x slower                                  |
| nqueens                  | 112 ms                                                       | 161 ms: 1.44x slower                                  |
| fannkuch                 | 547 ms                                                       | 792 ms: 1.45x slower                                  |
| sympy_integrate          | 30.2 ms                                                      | 44.1 ms: 1.46x slower                                 |
| xml_etree_process        | 85.9 ms                                                      | 127 ms: 1.48x slower                                  |
| bench_thread_pool        | 2.89 ms                                                      | 4.26 ms: 1.48x slower                                 |
| html5lib                 | 92.6 ms                                                      | 137 ms: 1.48x slower                                  |
| 2to3                     | 445 ms                                                       | 662 ms: 1.49x slower                                  |
| crypto_pyaes             | 100 ms                                                       | 152 ms: 1.52x slower                                  |
| tomli_loads              | 2.78 sec                                                     | 4.32 sec: 1.55x slower                                |
| deepcopy_reduce          | 4.10 us                                                      | 6.40 us: 1.56x slower                                 |
| typing_runtime_protocols | 226 us                                                       | 354 us: 1.57x slower                                  |
| spectral_norm            | 157 ms                                                       | 246 ms: 1.57x slower                                  |
| thrift                   | 1.10 ms                                                      | 1.74 ms: 1.59x slower                                 |
| sqlglot_normalize        | 140 ms                                                       | 227 ms: 1.62x slower                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.2 sec: 1.63x slower                                |
| richards                 | 65.5 ms                                                      | 107 ms: 1.63x slower                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 123 ms: 1.64x slower                                  |
| pyflate                  | 664 ms                                                       | 1.12 sec: 1.68x slower                                |
| regex_compile            | 182 ms                                                       | 307 ms: 1.69x slower                                  |
| genshi_text              | 31.7 ms                                                      | 53.7 ms: 1.70x slower                                 |
| genshi_xml               | 72.1 ms                                                      | 125 ms: 1.74x slower                                  |
| richards_super           | 73.2 ms                                                      | 127 ms: 1.74x slower                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.75 sec: 1.77x slower                                |
| sympy_str                | 379 ms                                                       | 679 ms: 1.79x slower                                  |
| comprehensions           | 22.2 us                                                      | 39.9 us: 1.79x slower                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.52 sec: 1.81x slower                                |
| scimark_monte_carlo      | 90.6 ms                                                      | 164 ms: 1.81x slower                                  |
| float                    | 116 ms                                                       | 211 ms: 1.82x slower                                  |
| unpickle_pure_python     | 290 us                                                       | 547 us: 1.88x slower                                  |
| pickle_pure_python       | 416 us                                                       | 801 us: 1.92x slower                                  |
| logging_simple           | 8.56 us                                                      | 16.5 us: 1.93x slower                                 |
| logging_format           | 9.24 us                                                      | 17.9 us: 1.93x slower                                 |
| django_template          | 44.3 ms                                                      | 86.4 ms: 1.95x slower                                 |
| mako                     | 15.9 ms                                                      | 31.1 ms: 1.95x slower                                 |
| scimark_sor              | 179 ms                                                       | 353 ms: 1.98x slower                                  |
| hexiom                   | 8.11 ms                                                      | 16.1 ms: 1.99x slower                                 |
| logging_silent           | 130 ns                                                       | 266 ns: 2.05x slower                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.52 ms: 2.06x slower                                 |
| chaos                    | 83.6 ms                                                      | 176 ms: 2.10x slower                                  |
| sympy_expand             | 601 ms                                                       | 1.26 sec: 2.10x slower                                |
| scimark_lu               | 146 ms                                                       | 315 ms: 2.15x slower                                  |
| go                       | 191 ms                                                       | 420 ms: 2.20x slower                                  |
| sqlglot_parse            | 1.76 ms                                                      | 4.03 ms: 2.29x slower                                 |
| sympy_sum                | 210 ms                                                       | 483 ms: 2.30x slower                                  |
| raytrace                 | 344 ms                                                       | 803 ms: 2.33x slower                                  |
| nbody                    | 119 ms                                                       | 278 ms: 2.34x slower                                  |
| unpack_sequence          | 74.3 ns                                                      | 194 ns: 2.61x slower                                  |
| deltablue                | 4.44 ms                                                      | 11.8 ms: 2.65x slower                                 |
| Geometric mean           | (ref)                                                        | 1.42x slower                                          |

Benchmark hidden because not significant (11): xml_etree_iterparse, pidigits, pickle_dict, async_tree_memoization_tg, pickle_list, async_tree_cpu_io_mixed_tg, asyncio_websockets, regex_effbot, regex_dna, async_tree_none_tg, async_tree_none
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x