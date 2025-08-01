# Results vs. 3.13.0rc2

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: linux-x86_64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 510 ms: 1.25x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                 |
| regex_dna      | 180 ms                                                       | 164 ms: 1.10x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.7 ms: 1.01x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| django_template | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 617 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 599 ms: 1.46x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| go                         | 141 ms                                                       | 102 ms: 1.37x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.0 us: 1.35x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 505 ms: 1.32x faster                                                  |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 510 ms: 1.25x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.57 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                 |
| spectral_norm              | 111 ms                                                       | 97.1 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.8 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| richards                   | 45.2 ms                                                      | 40.5 ms: 1.12x faster                                                 |
| pyflate                    | 449 ms                                                       | 402 ms: 1.12x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.3 ms: 1.11x faster                                                 |
| regex_dna                  | 180 ms                                                       | 164 ms: 1.10x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                 |
| logging_silent             | 103 ns                                                       | 93.4 ns: 1.10x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.4 us: 1.07x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.1 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 695 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.9 ms: 1.06x faster                                                 |
| scimark_fft                | 349 ms                                                       | 333 ms: 1.05x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| deltablue                  | 3.12 ms                                                      | 2.99 ms: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| meteor_contest             | 102 ms                                                       | 98.9 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                |
| thrift                     | 778 us                                                       | 765 us: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.3 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.7 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.32 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 250 ms: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.79 us: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 155 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| django_template            | 34.1 ms                                                      | 34.4 ms: 1.01x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.7 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.01x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.8 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                                  |
| json                       | 4.93 ms                                                      | 5.15 ms: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 89.3 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.96 ms: 1.05x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.06 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.95 ms: 1.46x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 102 ms: 9.32x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (3): genshi_xml, sympy_expand, coverage
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x