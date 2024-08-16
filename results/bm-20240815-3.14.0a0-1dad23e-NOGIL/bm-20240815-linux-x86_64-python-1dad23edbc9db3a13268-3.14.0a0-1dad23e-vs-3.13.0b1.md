# Results vs. 3.13.0b1

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 687 ms: 1.56x slower                                                  |
| docutils       | 3.94 sec                                                              | 5.35 sec: 1.36x slower                                                |
| html5lib       | 92.0 ms                                                               | 147 ms: 1.60x slower                                                  |
| tornado_http   | 253 ms                                                                | 350 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.14 sec: 1.26x faster                                                |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.09x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 490 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 836 ms: 1.05x faster                                                  |
| asyncio_websockets         | 728 ms                                                                | 781 ms: 1.07x slower                                                  |
| asyncio_tcp                | 972 ms                                                                | 1.16 sec: 1.19x slower                                                |
| async_tree_none            | 523 ms                                                                | 626 ms: 1.20x slower                                                  |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.47 sec: 1.23x slower                                                |
| async_generators           | 588 ms                                                                | 731 ms: 1.24x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 42.9 ms: 1.46x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.06x slower                                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                | 195 ms: 1.69x slower                                                  |
| nbody          | 126 ms                                                                | 307 ms: 2.44x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.59x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 300 ms: 1.06x slower                                                  |
| regex_effbot   | 4.63 ms                                                               | 5.00 ms: 1.08x slower                                                 |
| regex_compile  | 189 ms                                                                | 310 ms: 1.63x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.17x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.72 us: 1.11x faster                                                 |
| pickle_dict          | 46.5 us                                                               | 42.2 us: 1.10x faster                                                 |
| pickle               | 15.2 us                                                               | 13.8 us: 1.10x faster                                                 |
| xml_etree_parse      | 216 ms                                                                | 229 ms: 1.06x slower                                                  |
| xml_etree_iterparse  | 163 ms                                                                | 176 ms: 1.08x slower                                                  |
| unpickle_list        | 6.78 us                                                               | 7.89 us: 1.16x slower                                                 |
| json_loads           | 37.9 us                                                               | 44.8 us: 1.18x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 167 ms: 1.39x slower                                                  |
| tomli_loads          | 2.84 sec                                                              | 4.23 sec: 1.49x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 130 ms: 1.58x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 783 us: 1.83x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 578 us: 2.03x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 20.9 ms: 1.31x slower                                                 |
| python_startup         | 23.5 ms                                                               | 30.8 ms: 1.31x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.31x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 124 ms: 1.73x slower                                                  |
| genshi_text     | 31.6 ms                                                               | 55.2 ms: 1.75x slower                                                 |
| mako            | 16.7 ms                                                               | 31.5 ms: 1.89x slower                                                 |
| django_template | 46.1 ms                                                               | 87.7 ms: 1.90x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.82x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 13.7 ms: 16.73x faster                                                |
| create_gc_cycles           | 2.49 ms                                                               | 1.87 ms: 1.33x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.14 sec: 1.26x faster                                                |
| gc_traversal               | 5.80 ms                                                               | 5.05 ms: 1.15x faster                                                 |
| pickle_list                | 7.48 us                                                               | 6.72 us: 1.11x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 42.2 us: 1.10x faster                                                 |
| pickle                     | 15.2 us                                                               | 13.8 us: 1.10x faster                                                 |
| async_tree_io              | 1.39 sec                                                              | 1.28 sec: 1.09x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 490 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 836 ms: 1.05x faster                                                  |
| regex_dna                  | 284 ms                                                                | 300 ms: 1.06x slower                                                  |
| xml_etree_parse            | 216 ms                                                                | 229 ms: 1.06x slower                                                  |
| asyncio_websockets         | 728 ms                                                                | 781 ms: 1.07x slower                                                  |
| regex_effbot               | 4.63 ms                                                               | 5.00 ms: 1.08x slower                                                 |
| xml_etree_iterparse        | 163 ms                                                                | 176 ms: 1.08x slower                                                  |
| sqlite_synth               | 3.94 us                                                               | 4.29 us: 1.09x slower                                                 |
| unpickle_list              | 6.78 us                                                               | 7.89 us: 1.16x slower                                                 |
| pathlib                    | 31.8 ms                                                               | 37.4 ms: 1.18x slower                                                 |
| json_loads                 | 37.9 us                                                               | 44.8 us: 1.18x slower                                                 |
| asyncio_tcp                | 972 ms                                                                | 1.16 sec: 1.19x slower                                                |
| async_tree_none            | 523 ms                                                                | 626 ms: 1.20x slower                                                  |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.47 sec: 1.23x slower                                                |
| async_generators           | 588 ms                                                                | 731 ms: 1.24x slower                                                  |
| deepcopy                   | 498 us                                                                | 626 us: 1.26x slower                                                  |
| json                       | 6.79 ms                                                               | 8.59 ms: 1.26x slower                                                 |
| meteor_contest             | 156 ms                                                                | 202 ms: 1.29x slower                                                  |
| pylint                     | 466 ms                                                                | 606 ms: 1.30x slower                                                  |
| pycparser                  | 1.71 sec                                                              | 2.23 sec: 1.30x slower                                                |
| mdp                        | 4.01 sec                                                              | 5.24 sec: 1.31x slower                                                |
| python_startup_no_site     | 16.0 ms                                                               | 20.9 ms: 1.31x slower                                                 |
| python_startup             | 23.5 ms                                                               | 30.8 ms: 1.31x slower                                                 |
| coverage                   | 121 ms                                                                | 159 ms: 1.32x slower                                                  |
| docutils                   | 3.94 sec                                                              | 5.35 sec: 1.36x slower                                                |
| json_dumps                 | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                                 |
| tornado_http               | 253 ms                                                                | 350 ms: 1.38x slower                                                  |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 9.49 ms: 1.39x slower                                                 |
| xml_etree_generate         | 120 ms                                                                | 167 ms: 1.39x slower                                                  |
| scimark_fft                | 469 ms                                                                | 657 ms: 1.40x slower                                                  |
| generators                 | 40.7 ms                                                               | 58.2 ms: 1.43x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 42.9 ms: 1.46x slower                                                 |
| tomli_loads                | 2.84 sec                                                              | 4.23 sec: 1.49x slower                                                |
| nqueens                    | 108 ms                                                                | 164 ms: 1.51x slower                                                  |
| deepcopy_memo              | 50.9 us                                                               | 77.4 us: 1.52x slower                                                 |
| fannkuch                   | 535 ms                                                                | 814 ms: 1.52x slower                                                  |
| thrift                     | 1.09 ms                                                               | 1.66 ms: 1.53x slower                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 6.61 us: 1.54x slower                                                 |
| typing_runtime_protocols   | 222 us                                                                | 342 us: 1.54x slower                                                  |
| richards                   | 68.8 ms                                                               | 107 ms: 1.55x slower                                                  |
| 2to3                       | 441 ms                                                                | 687 ms: 1.56x slower                                                  |
| sqlglot_normalize          | 150 ms                                                                | 235 ms: 1.56x slower                                                  |
| sqlglot_optimize           | 77.9 ms                                                               | 122 ms: 1.57x slower                                                  |
| pyflate                    | 710 ms                                                                | 1.12 sec: 1.58x slower                                                |
| xml_etree_process          | 82.2 ms                                                               | 130 ms: 1.58x slower                                                  |
| sympy_integrate            | 28.7 ms                                                               | 45.4 ms: 1.58x slower                                                 |
| crypto_pyaes               | 102 ms                                                                | 161 ms: 1.58x slower                                                  |
| html5lib                   | 92.0 ms                                                               | 147 ms: 1.60x slower                                                  |
| logging_simple             | 9.16 us                                                               | 14.9 us: 1.63x slower                                                 |
| regex_compile              | 189 ms                                                                | 310 ms: 1.63x slower                                                  |
| bpe_tokeniser              | 6.53 sec                                                              | 10.7 sec: 1.63x slower                                                |
| spectral_norm              | 151 ms                                                                | 247 ms: 1.64x slower                                                  |
| float                      | 115 ms                                                                | 195 ms: 1.69x slower                                                  |
| genshi_xml                 | 71.9 ms                                                               | 124 ms: 1.73x slower                                                  |
| comprehensions             | 22.6 us                                                               | 39.2 us: 1.73x slower                                                 |
| genshi_text                | 31.6 ms                                                               | 55.2 ms: 1.75x slower                                                 |
| bench_thread_pool          | 3.01 ms                                                               | 5.33 ms: 1.77x slower                                                 |
| pprint_pformat             | 2.04 sec                                                              | 3.62 sec: 1.78x slower                                                |
| scimark_monte_carlo        | 89.0 ms                                                               | 161 ms: 1.81x slower                                                  |
| pprint_safe_repr           | 991 ms                                                                | 1.80 sec: 1.81x slower                                                |
| richards_super             | 73.5 ms                                                               | 133 ms: 1.82x slower                                                  |
| pickle_pure_python         | 428 us                                                                | 783 us: 1.83x slower                                                  |
| logging_format             | 9.36 us                                                               | 17.3 us: 1.84x slower                                                 |
| sympy_str                  | 376 ms                                                                | 697 ms: 1.85x slower                                                  |
| mako                       | 16.7 ms                                                               | 31.5 ms: 1.89x slower                                                 |
| django_template            | 46.1 ms                                                               | 87.7 ms: 1.90x slower                                                 |
| logging_silent             | 137 ns                                                                | 266 ns: 1.95x slower                                                  |
| sqlglot_parse              | 1.92 ms                                                               | 3.77 ms: 1.96x slower                                                 |
| sympy_expand               | 638 ms                                                                | 1.26 sec: 1.97x slower                                                |
| hexiom                     | 8.42 ms                                                               | 16.9 ms: 2.01x slower                                                 |
| scimark_sor                | 176 ms                                                                | 355 ms: 2.01x slower                                                  |
| unpickle_pure_python       | 285 us                                                                | 578 us: 2.03x slower                                                  |
| sympy_sum                  | 226 ms                                                                | 462 ms: 2.04x slower                                                  |
| sqlglot_transpile          | 2.24 ms                                                               | 4.65 ms: 2.07x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 319 ms: 2.13x slower                                                  |
| chaos                      | 81.5 ms                                                               | 177 ms: 2.18x slower                                                  |
| raytrace                   | 351 ms                                                                | 789 ms: 2.25x slower                                                  |
| go                         | 193 ms                                                                | 440 ms: 2.28x slower                                                  |
| nbody                      | 126 ms                                                                | 307 ms: 2.44x slower                                                  |
| deltablue                  | 4.55 ms                                                               | 11.8 ms: 2.60x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 212 ns: 3.89x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.39x slower                                                          |

Benchmark hidden because not significant (7): bench_mp_pool, async_tree_memoization_tg, pidigits, regex_v8, async_tree_memoization, async_tree_cpu_io_mixed, unpickle
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x