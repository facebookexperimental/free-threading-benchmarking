# Results vs. 3.13.0b1

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 650 ms: 1.47x slower                                                  |
| docutils       | 3.94 sec                                                              | 4.88 sec: 1.24x slower                                                |
| html5lib       | 92.0 ms                                                               | 139 ms: 1.51x slower                                                  |
| tornado_http   | 253 ms                                                                | 349 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.40x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.16 sec: 1.23x faster                                                |
| async_tree_none_tg         | 526 ms                                                                | 485 ms: 1.08x faster                                                  |
| async_tree_memoization     | 775 ms                                                                | 721 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 817 ms: 1.07x faster                                                  |
| async_tree_io              | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                                |
| asyncio_websockets         | 728 ms                                                                | 753 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 944 ms: 1.05x slower                                                  |
| async_tree_none            | 523 ms                                                                | 588 ms: 1.12x slower                                                  |
| asyncio_tcp                | 972 ms                                                                | 1.12 sec: 1.15x slower                                                |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                                |
| async_generators           | 588 ms                                                                | 739 ms: 1.26x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 43.2 ms: 1.47x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                                          |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 243 ms: 1.05x faster                                                  |
| float          | 115 ms                                                                | 202 ms: 1.75x slower                                                  |
| nbody          | 126 ms                                                                | 288 ms: 2.29x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.56x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 294 ms: 1.04x slower                                                  |
| regex_compile  | 189 ms                                                                | 291 ms: 1.54x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.30 us: 1.19x faster                                                 |
| pickle_dict          | 46.5 us                                                               | 42.5 us: 1.09x faster                                                 |
| pickle               | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| xml_etree_parse      | 216 ms                                                                | 231 ms: 1.07x slower                                                  |
| json_loads           | 37.9 us                                                               | 42.7 us: 1.13x slower                                                 |
| unpickle_list        | 6.78 us                                                               | 8.14 us: 1.20x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 162 ms: 1.36x slower                                                  |
| json_dumps           | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                                 |
| tomli_loads          | 2.84 sec                                                              | 4.22 sec: 1.49x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 127 ms: 1.54x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 805 us: 1.88x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 609 us: 2.14x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                                          |

Benchmark hidden because not significant (2): unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 29.7 ms: 1.26x slower                                                 |
| python_startup_no_site | 16.0 ms                                                               | 20.6 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 116 ms: 1.61x slower                                                  |
| genshi_text     | 31.6 ms                                                               | 54.9 ms: 1.74x slower                                                 |
| django_template | 46.1 ms                                                               | 80.4 ms: 1.74x slower                                                 |
| mako            | 16.7 ms                                                               | 30.4 ms: 1.82x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 13.2 ms: 17.32x faster                                                |
| bench_mp_pool              | 19.7 ms                                                               | 13.4 ms: 1.46x faster                                                 |
| create_gc_cycles           | 2.49 ms                                                               | 1.94 ms: 1.28x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.16 sec: 1.23x faster                                                |
| gc_traversal               | 5.80 ms                                                               | 4.76 ms: 1.22x faster                                                 |
| pickle_list                | 7.48 us                                                               | 6.30 us: 1.19x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 42.5 us: 1.09x faster                                                 |
| async_tree_none_tg         | 526 ms                                                                | 485 ms: 1.08x faster                                                  |
| async_tree_memoization     | 775 ms                                                                | 721 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 817 ms: 1.07x faster                                                  |
| async_tree_io              | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                                |
| pidigits                   | 256 ms                                                                | 243 ms: 1.05x faster                                                  |
| pickle                     | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| asyncio_websockets         | 728 ms                                                                | 753 ms: 1.03x slower                                                  |
| regex_dna                  | 284 ms                                                                | 294 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 944 ms: 1.05x slower                                                  |
| xml_etree_parse            | 216 ms                                                                | 231 ms: 1.07x slower                                                  |
| pathlib                    | 31.8 ms                                                               | 34.8 ms: 1.09x slower                                                 |
| sqlite_synth               | 3.94 us                                                               | 4.35 us: 1.10x slower                                                 |
| async_tree_none            | 523 ms                                                                | 588 ms: 1.12x slower                                                  |
| json_loads                 | 37.9 us                                                               | 42.7 us: 1.13x slower                                                 |
| asyncio_tcp                | 972 ms                                                                | 1.12 sec: 1.15x slower                                                |
| json                       | 6.79 ms                                                               | 7.98 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.36 sec: 1.19x slower                                                |
| unpickle_list              | 6.78 us                                                               | 8.14 us: 1.20x slower                                                 |
| deepcopy                   | 498 us                                                                | 606 us: 1.22x slower                                                  |
| docutils                   | 3.94 sec                                                              | 4.88 sec: 1.24x slower                                                |
| coverage                   | 121 ms                                                                | 150 ms: 1.24x slower                                                  |
| meteor_contest             | 156 ms                                                                | 196 ms: 1.26x slower                                                  |
| async_generators           | 588 ms                                                                | 739 ms: 1.26x slower                                                  |
| python_startup             | 23.5 ms                                                               | 29.7 ms: 1.26x slower                                                 |
| mdp                        | 4.01 sec                                                              | 5.14 sec: 1.28x slower                                                |
| python_startup_no_site     | 16.0 ms                                                               | 20.6 ms: 1.29x slower                                                 |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 8.89 ms: 1.30x slower                                                 |
| pylint                     | 466 ms                                                                | 607 ms: 1.30x slower                                                  |
| bench_thread_pool          | 3.01 ms                                                               | 4.01 ms: 1.33x slower                                                 |
| pycparser                  | 1.71 sec                                                              | 2.28 sec: 1.33x slower                                                |
| scimark_fft                | 469 ms                                                                | 633 ms: 1.35x slower                                                  |
| xml_etree_generate         | 120 ms                                                                | 162 ms: 1.36x slower                                                  |
| json_dumps                 | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                                 |
| tornado_http               | 253 ms                                                                | 349 ms: 1.38x slower                                                  |
| deepcopy_reduce            | 4.31 us                                                               | 6.01 us: 1.40x slower                                                 |
| generators                 | 40.7 ms                                                               | 58.0 ms: 1.42x slower                                                 |
| deepcopy_memo              | 50.9 us                                                               | 72.8 us: 1.43x slower                                                 |
| nqueens                    | 108 ms                                                                | 157 ms: 1.45x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 43.2 ms: 1.47x slower                                                 |
| 2to3                       | 441 ms                                                                | 650 ms: 1.47x slower                                                  |
| tomli_loads                | 2.84 sec                                                              | 4.22 sec: 1.49x slower                                                |
| dulwich_log                | 97.5 ms                                                               | 146 ms: 1.50x slower                                                  |
| sympy_integrate            | 28.7 ms                                                               | 43.3 ms: 1.51x slower                                                 |
| fannkuch                   | 535 ms                                                                | 808 ms: 1.51x slower                                                  |
| html5lib                   | 92.0 ms                                                               | 139 ms: 1.51x slower                                                  |
| crypto_pyaes               | 102 ms                                                                | 155 ms: 1.52x slower                                                  |
| typing_runtime_protocols   | 222 us                                                                | 339 us: 1.53x slower                                                  |
| regex_compile              | 189 ms                                                                | 291 ms: 1.54x slower                                                  |
| xml_etree_process          | 82.2 ms                                                               | 127 ms: 1.54x slower                                                  |
| sqlglot_normalize          | 150 ms                                                                | 238 ms: 1.58x slower                                                  |
| bpe_tokeniser              | 6.53 sec                                                              | 10.3 sec: 1.58x slower                                                |
| pyflate                    | 710 ms                                                                | 1.13 sec: 1.59x slower                                                |
| thrift                     | 1.09 ms                                                               | 1.74 ms: 1.60x slower                                                 |
| genshi_xml                 | 71.9 ms                                                               | 116 ms: 1.61x slower                                                  |
| spectral_norm              | 151 ms                                                                | 246 ms: 1.63x slower                                                  |
| sqlglot_optimize           | 77.9 ms                                                               | 128 ms: 1.64x slower                                                  |
| logging_simple             | 9.16 us                                                               | 15.3 us: 1.67x slower                                                 |
| richards                   | 68.8 ms                                                               | 115 ms: 1.67x slower                                                  |
| pprint_safe_repr           | 991 ms                                                                | 1.71 sec: 1.72x slower                                                |
| comprehensions             | 22.6 us                                                               | 39.2 us: 1.73x slower                                                 |
| genshi_text                | 31.6 ms                                                               | 54.9 ms: 1.74x slower                                                 |
| django_template            | 46.1 ms                                                               | 80.4 ms: 1.74x slower                                                 |
| float                      | 115 ms                                                                | 202 ms: 1.75x slower                                                  |
| pprint_pformat             | 2.04 sec                                                              | 3.58 sec: 1.76x slower                                                |
| sympy_str                  | 376 ms                                                                | 667 ms: 1.77x slower                                                  |
| mako                       | 16.7 ms                                                               | 30.4 ms: 1.82x slower                                                 |
| logging_silent             | 137 ns                                                                | 251 ns: 1.84x slower                                                  |
| logging_format             | 9.36 us                                                               | 17.3 us: 1.85x slower                                                 |
| richards_super             | 73.5 ms                                                               | 136 ms: 1.85x slower                                                  |
| pickle_pure_python         | 428 us                                                                | 805 us: 1.88x slower                                                  |
| hexiom                     | 8.42 ms                                                               | 16.2 ms: 1.92x slower                                                 |
| scimark_monte_carlo        | 89.0 ms                                                               | 171 ms: 1.93x slower                                                  |
| scimark_sor                | 176 ms                                                                | 341 ms: 1.94x slower                                                  |
| sympy_expand               | 638 ms                                                                | 1.25 sec: 1.96x slower                                                |
| sqlglot_parse              | 1.92 ms                                                               | 3.96 ms: 2.07x slower                                                 |
| sympy_sum                  | 226 ms                                                                | 477 ms: 2.11x slower                                                  |
| unpickle_pure_python       | 285 us                                                                | 609 us: 2.14x slower                                                  |
| chaos                      | 81.5 ms                                                               | 175 ms: 2.14x slower                                                  |
| go                         | 193 ms                                                                | 421 ms: 2.18x slower                                                  |
| sqlglot_transpile          | 2.24 ms                                                               | 4.92 ms: 2.19x slower                                                 |
| scimark_lu                 | 150 ms                                                                | 332 ms: 2.22x slower                                                  |
| raytrace                   | 351 ms                                                                | 802 ms: 2.29x slower                                                  |
| nbody                      | 126 ms                                                                | 288 ms: 2.29x slower                                                  |
| deltablue                  | 4.55 ms                                                               | 11.7 ms: 2.56x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 210 ns: 3.84x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.36x slower                                                          |

Benchmark hidden because not significant (5): async_tree_memoization_tg, regex_v8, regex_effbot, unpickle, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.16x