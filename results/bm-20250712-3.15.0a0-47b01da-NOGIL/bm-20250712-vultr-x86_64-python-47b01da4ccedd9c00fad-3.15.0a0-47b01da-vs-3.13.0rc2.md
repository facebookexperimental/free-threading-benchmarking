# Results vs. 3.13.0rc2

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: linux-x86_64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.060x slower
- HPT reliability: 97.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 285 ms: 1.10x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| html5lib       | 67.0 ms                                                      | 66.1 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 536 ms: 1.70x faster                                                  |
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 322 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 264 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 515 ms: 1.29x faster                                                  |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 518 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float          | 77.5 ms                                                      | 69.9 ms: 1.11x faster                                                 |
| nbody          | 85.1 ms                                                      | 122 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.4 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 32.8 us: 1.01x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.22 us: 1.06x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                |
| pickle               | 11.3 us                                                      | 12.4 us: 1.09x slower                                                 |
| unpickle             | 14.3 us                                                      | 15.7 us: 1.10x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 231 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.33 us: 1.13x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 339 us: 1.15x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.2 ms: 1.16x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 57.8 ms: 1.18x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                 |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.78x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 536 ms: 1.70x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.88 ms: 1.67x faster                                                 |
| async_tree_io              | 876 ms                                                       | 564 ms: 1.55x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 322 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 264 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 515 ms: 1.29x faster                                                  |
| deepcopy                   | 355 us                                                       | 294 us: 1.21x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 34.7 us: 1.13x faster                                                 |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 69.9 ms: 1.11x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.4 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                 |
| scimark_sor                | 134 ms                                                       | 125 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.8 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.03x faster                                                  |
| async_generators           | 377 ms                                                       | 371 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 66.1 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                |
| pickle_dict                | 32.5 us                                                      | 32.8 us: 1.01x slower                                                 |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                  |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| asyncio_tcp                | 505 ms                                                       | 518 ms: 1.03x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.7 ms: 1.03x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| pyflate                    | 449 ms                                                       | 467 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.22 us: 1.06x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 783 ms: 1.06x slower                                                  |
| scimark_fft                | 349 ms                                                       | 373 ms: 1.07x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                |
| json                       | 4.93 ms                                                      | 5.35 ms: 1.08x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.51 ms: 1.09x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.63 sec: 1.09x slower                                                |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.46 ms: 1.09x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.4 us: 1.09x slower                                                 |
| chaos                      | 57.3 ms                                                      | 62.8 ms: 1.10x slower                                                 |
| unpickle                   | 14.3 us                                                      | 15.7 us: 1.10x slower                                                 |
| 2to3                       | 260 ms                                                       | 285 ms: 1.10x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 231 us: 1.10x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.1 ms: 1.12x slower                                                 |
| generators                 | 28.8 ms                                                      | 32.2 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.1 ms: 1.12x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.9 ms: 1.13x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.33 us: 1.13x slower                                                 |
| richards                   | 45.2 ms                                                      | 51.4 ms: 1.14x slower                                                 |
| thrift                     | 778 us                                                       | 885 us: 1.14x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.02 us: 1.14x slower                                                 |
| richards_super             | 51.6 ms                                                      | 59.0 ms: 1.14x slower                                                 |
| sympy_str                  | 275 ms                                                       | 314 ms: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 339 us: 1.15x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                  |
| sympy_expand               | 457 ms                                                       | 528 ms: 1.16x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.2 ms: 1.16x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.3 us: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.65 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.07 us: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.57 ms: 1.18x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 57.8 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.9 ms: 1.19x slower                                                 |
| raytrace                   | 253 ms                                                       | 302 ms: 1.19x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                |
| fannkuch                   | 370 ms                                                       | 454 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 191 us: 1.23x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 55.5 ns: 1.24x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 86.7 ms: 1.28x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.33x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.16 ms: 3.44x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.88x slower                                                  |
| telco                      | 7.82 ms                                                      | 177 ms: 22.56x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 97.03% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x