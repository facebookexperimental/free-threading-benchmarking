# Results vs. 3.13.0rc2

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: linux-x86_64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.054x slower
- HPT reliability: 95.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.0 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 527 ms: 1.73x faster                                                  |
| async_tree_io              | 876 ms                                                       | 553 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 228 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 285 ms: 1.45x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                  |
| async_generators           | 377 ms                                                       | 369 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.5 ms: 1.11x faster                                                 |
| pidigits       | 217 ms                                                       | 206 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                 |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| regex_compile  | 132 ms                                                       | 142 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                |
| unpickle_pure_python | 210 us                                                       | 230 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 94.9 ms: 1.11x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 335 us: 1.14x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.3 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.0 ms: 1.14x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 527 ms: 1.73x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.87 ms: 1.68x faster                                                 |
| async_tree_io              | 876 ms                                                       | 553 ms: 1.58x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 228 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 285 ms: 1.45x faster                                                  |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.37x faster                                                  |
| deepcopy                   | 355 us                                                       | 290 us: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 545 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 34.3 us: 1.14x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                 |
| float                      | 77.5 ms                                                      | 69.5 ms: 1.11x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                 |
| pidigits                   | 217 ms                                                       | 206 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.7 ms: 1.04x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 65.0 ms: 1.03x faster                                                 |
| async_generators           | 377 ms                                                       | 369 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.07 us: 1.01x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| pyflate                    | 449 ms                                                       | 457 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                 |
| scimark_fft                | 349 ms                                                       | 367 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 777 ms: 1.05x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.38 ms: 1.07x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.60 sec: 1.07x slower                                                |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| regex_compile              | 132 ms                                                       | 142 ms: 1.07x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.44 ms: 1.07x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                                |
| json                       | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                                 |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.7 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 230 us: 1.10x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.7 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 94.9 ms: 1.11x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.85 us: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.7 ms: 1.12x slower                                                 |
| thrift                     | 778 us                                                       | 874 us: 1.12x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.3 ms: 1.14x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                  |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.0 ms: 1.14x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.57 ms: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.38 ms: 1.14x slower                                                 |
| django_template            | 34.1 ms                                                      | 39.0 ms: 1.14x slower                                                 |
| sympy_expand               | 457 ms                                                       | 525 ms: 1.15x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.15x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.92 us: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.3 ms: 1.16x slower                                                 |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.8 ms: 1.19x slower                                                 |
| raytrace                   | 253 ms                                                       | 303 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 186 us: 1.20x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.2 ms: 1.22x slower                                                 |
| fannkuch                   | 370 ms                                                       | 454 ms: 1.23x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.0 ms: 1.28x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                 |
| nbody                      | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.18 ms: 3.46x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.78x slower                                                  |
| telco                      | 7.82 ms                                                      | 175 ms: 22.36x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (2): pylint, pathlib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 95.70% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x