# Results vs. 3.13.0rc2

- fork: python
- ref: b5e4c46be24d1fade0de
- machine: linux-x86_64
- commit hash: b5e4c46
- commit date: 2026-03-20
- overall geometric mean: 1.036x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 309 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 504 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 508 ms: 1.25x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                  |
| pidigits       | 217 ms                                                       | 208 ms: 1.04x faster                                                   |
| nbody          | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| regex_dna      | 180 ms                                                       | 166 ms: 1.09x faster                                                   |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.1 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.6 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                  |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                   |
| deepcopy                   | 355 us                                                       | 234 us: 1.52x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 309 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 504 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 508 ms: 1.25x faster                                                   |
| spectral_norm              | 111 ms                                                       | 89.1 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                  |
| scimark_fft                | 349 ms                                                       | 309 ms: 1.13x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.1 ms: 1.11x faster                                                  |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                 |
| pyflate                    | 449 ms                                                       | 406 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 68.4 ms: 1.09x faster                                                  |
| float                      | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.33 ms: 1.09x faster                                                  |
| regex_dna                  | 180 ms                                                       | 166 ms: 1.09x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                  |
| chaos                      | 57.3 ms                                                      | 53.5 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.3 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.4 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.47 sec: 1.06x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.2 ns: 1.06x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.90 us: 1.04x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.7 ms: 1.04x faster                                                  |
| pidigits                   | 217 ms                                                       | 208 ms: 1.04x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 75.6 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 714 ms: 1.03x faster                                                   |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.6 ms: 1.01x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.44 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 384 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 163 us: 1.05x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 483 ms: 1.06x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.33 ms: 1.07x slower                                                  |
| nbody                      | 85.1 ms                                                      | 92.1 ms: 1.08x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.34 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.88 ms: 1.40x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.29x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 287 ms: 26.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (5): comprehensions, coverage, coroutines, raytrace, thrift
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260320-3.15.0a7+-b5e4c46/bm-20260320-vultr-x86_64-python-b5e4c46be24d1fade0de-3.15.0a7+-b5e4c46.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x