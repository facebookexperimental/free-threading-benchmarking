# Results vs. 3.13.0rc2

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 650 ms: 1.46x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.88 sec: 1.22x slower                                                |
| html5lib       | 92.6 ms                                                      | 139 ms: 1.51x slower                                                  |
| tornado_http   | 251 ms                                                       | 349 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                        | 1.39x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.16 sec: 1.20x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                                |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 817 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 944 ms: 1.06x slower                                                  |
| asyncio_tcp                | 948 ms                                                       | 1.12 sec: 1.18x slower                                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                                |
| async_generators           | 567 ms                                                       | 739 ms: 1.30x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 43.2 ms: 1.40x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                          |

Benchmark hidden because not significant (5): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 202 ms: 1.74x slower                                                  |
| nbody          | 119 ms                                                       | 288 ms: 2.42x slower                                                  |
| Geometric mean | (ref)                                                        | 1.60x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 294 ms: 1.04x slower                                                  |
| regex_v8       | 32.8 ms                                                      | 36.3 ms: 1.11x slower                                                 |
| regex_compile  | 182 ms                                                       | 291 ms: 1.60x slower                                                  |
| Geometric mean | (ref)                                                        | 1.16x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 42.5 us: 1.11x faster                                                 |
| pickle_list          | 6.86 us                                                      | 6.30 us: 1.09x faster                                                 |
| pickle               | 15.1 us                                                      | 14.5 us: 1.04x faster                                                 |
| unpickle             | 20.5 us                                                      | 22.3 us: 1.09x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 8.14 us: 1.22x slower                                                 |
| json_loads           | 34.3 us                                                      | 42.7 us: 1.25x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 162 ms: 1.33x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 19.0 ms: 1.35x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 127 ms: 1.47x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.22 sec: 1.52x slower                                                |
| pickle_pure_python   | 416 us                                                       | 805 us: 1.93x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 609 us: 2.10x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.7 ms: 1.33x slower                                                 |
| python_startup_no_site | 15.3 ms                                                      | 20.6 ms: 1.34x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 116 ms: 1.61x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 54.9 ms: 1.73x slower                                                 |
| django_template | 44.3 ms                                                      | 80.4 ms: 1.82x slower                                                 |
| mako            | 15.9 ms                                                      | 30.4 ms: 1.91x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool              | 18.7 ms                                                      | 13.4 ms: 1.39x faster                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 1.94 ms: 1.24x faster                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.16 sec: 1.20x faster                                                |
| gc_traversal               | 5.70 ms                                                      | 4.76 ms: 1.20x faster                                                 |
| pickle_dict                | 47.2 us                                                      | 42.5 us: 1.11x faster                                                 |
| pickle_list                | 6.86 us                                                      | 6.30 us: 1.09x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                                |
| pickle                     | 15.1 us                                                      | 14.5 us: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 817 ms: 1.04x faster                                                  |
| regex_dna                  | 282 ms                                                       | 294 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 944 ms: 1.06x slower                                                  |
| unpickle                   | 20.5 us                                                      | 22.3 us: 1.09x slower                                                 |
| telco                      | 12.2 ms                                                      | 13.2 ms: 1.09x slower                                                 |
| sqlite_synth               | 3.99 us                                                      | 4.35 us: 1.09x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 36.3 ms: 1.11x slower                                                 |
| pathlib                    | 29.9 ms                                                      | 34.8 ms: 1.16x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 1.12 sec: 1.18x slower                                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.36 sec: 1.21x slower                                                |
| docutils                   | 4.01 sec                                                     | 4.88 sec: 1.22x slower                                                |
| deepcopy                   | 498 us                                                       | 606 us: 1.22x slower                                                  |
| unpickle_list              | 6.68 us                                                      | 8.14 us: 1.22x slower                                                 |
| json                       | 6.51 ms                                                      | 7.98 ms: 1.23x slower                                                 |
| json_loads                 | 34.3 us                                                      | 42.7 us: 1.25x slower                                                 |
| pylint                     | 470 ms                                                       | 607 ms: 1.29x slower                                                  |
| async_generators           | 567 ms                                                       | 739 ms: 1.30x slower                                                  |
| meteor_contest             | 150 ms                                                       | 196 ms: 1.31x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.89 ms: 1.32x slower                                                 |
| python_startup             | 22.4 ms                                                      | 29.7 ms: 1.33x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 162 ms: 1.33x slower                                                  |
| scimark_fft                | 473 ms                                                       | 633 ms: 1.34x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 20.6 ms: 1.34x slower                                                 |
| json_dumps                 | 14.1 ms                                                      | 19.0 ms: 1.35x slower                                                 |
| mdp                        | 3.80 sec                                                     | 5.14 sec: 1.35x slower                                                |
| bench_thread_pool          | 2.89 ms                                                      | 4.01 ms: 1.39x slower                                                 |
| tornado_http               | 251 ms                                                       | 349 ms: 1.39x slower                                                  |
| coverage                   | 107 ms                                                       | 150 ms: 1.39x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 43.2 ms: 1.40x slower                                                 |
| nqueens                    | 112 ms                                                       | 157 ms: 1.41x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 43.3 ms: 1.43x slower                                                 |
| generators                 | 40.0 ms                                                      | 58.0 ms: 1.45x slower                                                 |
| pycparser                  | 1.57 sec                                                     | 2.28 sec: 1.45x slower                                                |
| deepcopy_memo              | 50.1 us                                                      | 72.8 us: 1.45x slower                                                 |
| 2to3                       | 445 ms                                                       | 650 ms: 1.46x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 6.01 us: 1.47x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 127 ms: 1.47x slower                                                  |
| fannkuch                   | 547 ms                                                       | 808 ms: 1.48x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 339 us: 1.50x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 139 ms: 1.51x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 4.22 sec: 1.52x slower                                                |
| crypto_pyaes               | 100 ms                                                       | 155 ms: 1.54x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 146 ms: 1.56x slower                                                  |
| spectral_norm              | 157 ms                                                       | 246 ms: 1.57x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.74 ms: 1.58x slower                                                 |
| regex_compile              | 182 ms                                                       | 291 ms: 1.60x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 116 ms: 1.61x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 10.3 sec: 1.65x slower                                                |
| sqlglot_normalize          | 140 ms                                                       | 238 ms: 1.70x slower                                                  |
| pyflate                    | 664 ms                                                       | 1.13 sec: 1.70x slower                                                |
| sqlglot_optimize           | 74.7 ms                                                      | 128 ms: 1.71x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.71 sec: 1.73x slower                                                |
| genshi_text                | 31.7 ms                                                      | 54.9 ms: 1.73x slower                                                 |
| float                      | 116 ms                                                       | 202 ms: 1.74x slower                                                  |
| richards                   | 65.5 ms                                                      | 115 ms: 1.76x slower                                                  |
| sympy_str                  | 379 ms                                                       | 667 ms: 1.76x slower                                                  |
| comprehensions             | 22.2 us                                                      | 39.2 us: 1.76x slower                                                 |
| logging_simple             | 8.56 us                                                      | 15.3 us: 1.78x slower                                                 |
| django_template            | 44.3 ms                                                      | 80.4 ms: 1.82x slower                                                 |
| pprint_pformat             | 1.94 sec                                                     | 3.58 sec: 1.84x slower                                                |
| richards_super             | 73.2 ms                                                      | 136 ms: 1.86x slower                                                  |
| logging_format             | 9.24 us                                                      | 17.3 us: 1.87x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 171 ms: 1.89x slower                                                  |
| mako                       | 15.9 ms                                                      | 30.4 ms: 1.91x slower                                                 |
| scimark_sor                | 179 ms                                                       | 341 ms: 1.91x slower                                                  |
| logging_silent             | 130 ns                                                       | 251 ns: 1.93x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 805 us: 1.93x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 16.2 ms: 1.99x slower                                                 |
| sympy_expand               | 601 ms                                                       | 1.25 sec: 2.09x slower                                                |
| chaos                      | 83.6 ms                                                      | 175 ms: 2.09x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 609 us: 2.10x slower                                                  |
| go                         | 191 ms                                                       | 421 ms: 2.20x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 4.92 ms: 2.24x slower                                                 |
| sqlglot_parse              | 1.76 ms                                                      | 3.96 ms: 2.26x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 332 ms: 2.27x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 477 ms: 2.27x slower                                                  |
| raytrace                   | 344 ms                                                       | 802 ms: 2.33x slower                                                  |
| nbody                      | 119 ms                                                       | 288 ms: 2.42x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 11.7 ms: 2.63x slower                                                 |
| unpack_sequence            | 74.3 ns                                                      | 210 ns: 2.82x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.43x slower                                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, regex_effbot, async_tree_none_tg, pidigits, asyncio_websockets, xml_etree_parse, async_tree_memoization_tg, async_tree_memoization, async_tree_none
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.15x