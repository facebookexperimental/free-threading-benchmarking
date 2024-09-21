# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 626 ms: 1.41x slower                                  |
| docutils       | 4.01 sec                                                     | 4.76 sec: 1.19x slower                                |
| html5lib       | 92.6 ms                                                      | 141 ms: 1.52x slower                                  |
| tornado_http   | 251 ms                                                       | 352 ms: 1.40x slower                                  |
| Geometric mean | (ref)                                                        | 1.37x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                |
| async_tree_io           | 1.39 sec                                                     | 1.31 sec: 1.06x faster                                |
| asyncio_websockets      | 766 ms                                                       | 738 ms: 1.04x faster                                  |
| async_tree_memoization  | 709 ms                                                       | 748 ms: 1.05x slower                                  |
| async_tree_cpu_io_mixed | 889 ms                                                       | 980 ms: 1.10x slower                                  |
| asyncio_tcp             | 948 ms                                                       | 1.09 sec: 1.15x slower                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.27 sec: 1.18x slower                                |
| async_generators        | 567 ms                                                       | 712 ms: 1.25x slower                                  |
| coroutines              | 30.9 ms                                                      | 45.1 ms: 1.46x slower                                 |
| Geometric mean          | (ref)                                                        | 1.05x slower                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 201 ms: 1.73x slower                                  |
| nbody          | 119 ms                                                       | 312 ms: 2.63x slower                                  |
| Geometric mean | (ref)                                                        | 1.64x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                 |
| regex_compile  | 182 ms                                                       | 290 ms: 1.59x slower                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 43.5 us: 1.09x faster                                 |
| pickle_list          | 6.86 us                                                      | 6.36 us: 1.08x faster                                 |
| unpickle             | 20.5 us                                                      | 22.7 us: 1.11x slower                                 |
| unpickle_list        | 6.68 us                                                      | 7.59 us: 1.14x slower                                 |
| json_loads           | 34.3 us                                                      | 42.8 us: 1.25x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 157 ms: 1.28x slower                                  |
| json_dumps           | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                 |
| xml_etree_process    | 85.9 ms                                                      | 121 ms: 1.41x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.35 sec: 1.56x slower                                |
| unpickle_pure_python | 290 us                                                       | 547 us: 1.88x slower                                  |
| pickle_pure_python   | 416 us                                                       | 804 us: 1.93x slower                                  |
| Geometric mean       | (ref)                                                        | 1.23x slower                                          |

Benchmark hidden because not significant (3): pickle, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 30.9 ms: 1.38x slower                                 |
| python_startup_no_site | 15.3 ms                                                      | 21.2 ms: 1.38x slower                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 116 ms: 1.61x slower                                  |
| genshi_text     | 31.7 ms                                                      | 58.2 ms: 1.84x slower                                 |
| django_template | 44.3 ms                                                      | 83.8 ms: 1.89x slower                                 |
| mako            | 15.9 ms                                                      | 31.2 ms: 1.96x slower                                 |
| Geometric mean  | (ref)                                                        | 1.82x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.83 ms: 1.32x faster                                 |
| gc_traversal             | 5.70 ms                                                      | 4.51 ms: 1.26x faster                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.13 sec: 1.24x faster                                |
| pickle_dict              | 47.2 us                                                      | 43.5 us: 1.09x faster                                 |
| pickle_list              | 6.86 us                                                      | 6.36 us: 1.08x faster                                 |
| async_tree_io            | 1.39 sec                                                     | 1.31 sec: 1.06x faster                                |
| asyncio_websockets       | 766 ms                                                       | 738 ms: 1.04x faster                                  |
| sqlite_synth             | 3.99 us                                                      | 4.19 us: 1.05x slower                                 |
| async_tree_memoization   | 709 ms                                                       | 748 ms: 1.05x slower                                  |
| regex_v8                 | 32.8 ms                                                      | 36.1 ms: 1.10x slower                                 |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 980 ms: 1.10x slower                                  |
| unpickle                 | 20.5 us                                                      | 22.7 us: 1.11x slower                                 |
| unpickle_list            | 6.68 us                                                      | 7.59 us: 1.14x slower                                 |
| telco                    | 12.2 ms                                                      | 14.0 ms: 1.15x slower                                 |
| asyncio_tcp              | 948 ms                                                       | 1.09 sec: 1.15x slower                                |
| deepcopy                 | 498 us                                                       | 579 us: 1.16x slower                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.27 sec: 1.18x slower                                |
| docutils                 | 4.01 sec                                                     | 4.76 sec: 1.19x slower                                |
| json                     | 6.51 ms                                                      | 7.97 ms: 1.22x slower                                 |
| pathlib                  | 29.9 ms                                                      | 36.6 ms: 1.23x slower                                 |
| scimark_fft              | 473 ms                                                       | 587 ms: 1.24x slower                                  |
| meteor_contest           | 150 ms                                                       | 186 ms: 1.24x slower                                  |
| json_loads               | 34.3 us                                                      | 42.8 us: 1.25x slower                                 |
| async_generators         | 567 ms                                                       | 712 ms: 1.25x slower                                  |
| pylint                   | 470 ms                                                       | 593 ms: 1.26x slower                                  |
| xml_etree_generate       | 122 ms                                                       | 157 ms: 1.28x slower                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.77 ms: 1.30x slower                                 |
| json_dumps               | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                 |
| mdp                      | 3.80 sec                                                     | 5.11 sec: 1.35x slower                                |
| generators               | 40.0 ms                                                      | 54.8 ms: 1.37x slower                                 |
| coverage                 | 107 ms                                                       | 147 ms: 1.37x slower                                  |
| python_startup           | 22.4 ms                                                      | 30.9 ms: 1.38x slower                                 |
| dulwich_log              | 93.7 ms                                                      | 130 ms: 1.38x slower                                  |
| python_startup_no_site   | 15.3 ms                                                      | 21.2 ms: 1.38x slower                                 |
| tornado_http             | 251 ms                                                       | 352 ms: 1.40x slower                                  |
| fannkuch                 | 547 ms                                                       | 767 ms: 1.40x slower                                  |
| 2to3                     | 445 ms                                                       | 626 ms: 1.41x slower                                  |
| xml_etree_process        | 85.9 ms                                                      | 121 ms: 1.41x slower                                  |
| nqueens                  | 112 ms                                                       | 160 ms: 1.43x slower                                  |
| deepcopy_reduce          | 4.10 us                                                      | 5.88 us: 1.44x slower                                 |
| sympy_integrate          | 30.2 ms                                                      | 43.8 ms: 1.45x slower                                 |
| pycparser                | 1.57 sec                                                     | 2.28 sec: 1.45x slower                                |
| bench_thread_pool        | 2.89 ms                                                      | 4.19 ms: 1.45x slower                                 |
| coroutines               | 30.9 ms                                                      | 45.1 ms: 1.46x slower                                 |
| deepcopy_memo            | 50.1 us                                                      | 73.7 us: 1.47x slower                                 |
| thrift                   | 1.10 ms                                                      | 1.65 ms: 1.50x slower                                 |
| crypto_pyaes             | 100 ms                                                       | 151 ms: 1.51x slower                                  |
| html5lib                 | 92.6 ms                                                      | 141 ms: 1.52x slower                                  |
| tomli_loads              | 2.78 sec                                                     | 4.35 sec: 1.56x slower                                |
| regex_compile            | 182 ms                                                       | 290 ms: 1.59x slower                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 10.0 sec: 1.60x slower                                |
| richards                 | 65.5 ms                                                      | 105 ms: 1.60x slower                                  |
| genshi_xml               | 72.1 ms                                                      | 116 ms: 1.61x slower                                  |
| typing_runtime_protocols | 226 us                                                       | 364 us: 1.61x slower                                  |
| spectral_norm            | 157 ms                                                       | 254 ms: 1.62x slower                                  |
| pyflate                  | 664 ms                                                       | 1.08 sec: 1.62x slower                                |
| sqlglot_optimize         | 74.7 ms                                                      | 125 ms: 1.67x slower                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.69 sec: 1.71x slower                                |
| comprehensions           | 22.2 us                                                      | 38.4 us: 1.73x slower                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 157 ms: 1.73x slower                                  |
| logging_format           | 9.24 us                                                      | 16.0 us: 1.73x slower                                 |
| float                    | 116 ms                                                       | 201 ms: 1.73x slower                                  |
| logging_simple           | 8.56 us                                                      | 15.0 us: 1.75x slower                                 |
| sqlglot_normalize        | 140 ms                                                       | 245 ms: 1.75x slower                                  |
| sympy_str                | 379 ms                                                       | 672 ms: 1.77x slower                                  |
| richards_super           | 73.2 ms                                                      | 130 ms: 1.78x slower                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.52 sec: 1.81x slower                                |
| genshi_text              | 31.7 ms                                                      | 58.2 ms: 1.84x slower                                 |
| unpickle_pure_python     | 290 us                                                       | 547 us: 1.88x slower                                  |
| scimark_sor              | 179 ms                                                       | 337 ms: 1.88x slower                                  |
| django_template          | 44.3 ms                                                      | 83.8 ms: 1.89x slower                                 |
| pickle_pure_python       | 416 us                                                       | 804 us: 1.93x slower                                  |
| go                       | 191 ms                                                       | 369 ms: 1.93x slower                                  |
| mako                     | 15.9 ms                                                      | 31.2 ms: 1.96x slower                                 |
| hexiom                   | 8.11 ms                                                      | 16.0 ms: 1.97x slower                                 |
| sqlglot_parse            | 1.76 ms                                                      | 3.50 ms: 1.99x slower                                 |
| chaos                    | 83.6 ms                                                      | 168 ms: 2.01x slower                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.53 ms: 2.06x slower                                 |
| logging_silent           | 130 ns                                                       | 272 ns: 2.09x slower                                  |
| scimark_lu               | 146 ms                                                       | 309 ms: 2.11x slower                                  |
| sympy_sum                | 210 ms                                                       | 464 ms: 2.21x slower                                  |
| sympy_expand             | 601 ms                                                       | 1.36 sec: 2.26x slower                                |
| raytrace                 | 344 ms                                                       | 791 ms: 2.30x slower                                  |
| deltablue                | 4.44 ms                                                      | 10.9 ms: 2.45x slower                                 |
| unpack_sequence          | 74.3 ns                                                      | 187 ns: 2.52x slower                                  |
| nbody                    | 119 ms                                                       | 312 ms: 2.63x slower                                  |
| Geometric mean           | (ref)                                                        | 1.41x slower                                          |

Benchmark hidden because not significant (11): bench_mp_pool, regex_effbot, pidigits, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, pickle, xml_etree_iterparse, async_tree_none, regex_dna, xml_etree_parse
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x