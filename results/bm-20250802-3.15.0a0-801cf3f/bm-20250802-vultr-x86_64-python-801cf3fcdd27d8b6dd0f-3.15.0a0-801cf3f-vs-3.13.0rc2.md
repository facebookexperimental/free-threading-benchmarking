# Results vs. 3.13.0rc2

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.034x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                  |
| async_tree_io              | 876 ms                                                       | 603 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 498 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 213 ms: 1.02x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.8 us: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| unpickle             | 14.3 us                                                      | 13.9 us: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.2 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.06 us: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 303 us: 1.03x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 4.94 us: 1.05x slower                                                 |
| json_loads           | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| pickle               | 11.3 us                                                      | 12.2 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                 |
| django_template | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.06x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                  |
| async_tree_io              | 876 ms                                                       | 603 ms: 1.45x faster                                                  |
| deepcopy                   | 355 us                                                       | 253 us: 1.41x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.0 us: 1.35x faster                                                 |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                  |
| spectral_norm              | 111 ms                                                       | 92.7 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 395 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.1 ms: 1.13x faster                                                 |
| unpack_sequence            | 44.8 ns                                                      | 39.9 ns: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 60.5 ms: 1.11x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.2 ms: 1.09x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.5 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 682 ms: 1.08x faster                                                  |
| scimark_fft                | 349 ms                                                       | 324 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.40 sec: 1.07x faster                                                |
| float                      | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.16 sec: 1.07x faster                                                |
| logging_silent             | 103 ns                                                       | 96.6 ns: 1.06x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.6 ms: 1.06x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.81 us: 1.06x faster                                                 |
| pickle_dict                | 32.5 us                                                      | 30.8 us: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.05x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.58 us: 1.04x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                                 |
| unpickle                   | 14.3 us                                                      | 13.9 us: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.2 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.8 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.58 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| genshi_xml                 | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.4 ms: 1.02x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 77.2 ms: 1.02x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                |
| pidigits                   | 217 ms                                                       | 213 ms: 1.02x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 498 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.1 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.1 ms: 1.00x slower                                                 |
| django_template            | 34.1 ms                                                      | 34.7 ms: 1.02x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                 |
| sympy_expand               | 457 ms                                                       | 468 ms: 1.02x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.06 us: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 303 us: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| fannkuch                   | 370 ms                                                       | 384 ms: 1.04x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 4.94 us: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                 |
| json                       | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.9 us: 1.07x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.2 us: 1.08x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.36 ms: 1.39x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.96 ms: 1.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.33x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.21x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (4): typing_runtime_protocols, regex_dna, asyncio_tcp_ssl, coroutines
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x