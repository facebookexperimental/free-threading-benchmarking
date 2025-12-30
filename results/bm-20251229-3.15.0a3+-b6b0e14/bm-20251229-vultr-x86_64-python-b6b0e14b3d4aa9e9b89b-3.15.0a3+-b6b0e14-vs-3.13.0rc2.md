# Results vs. 3.13.0rc2

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: linux-x86_64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.039x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.7 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 542 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                  |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| nbody          | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.6 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.0 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                  |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io              | 876 ms                                                       | 542 ms: 1.62x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                                  |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.48x faster                                                   |
| deepcopy                   | 355 us                                                       | 245 us: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| spectral_norm              | 111 ms                                                       | 92.0 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                  |
| scimark_fft                | 349 ms                                                       | 302 ms: 1.16x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 66.6 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.7 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                   |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.34 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| float                      | 77.5 ms                                                      | 71.7 ms: 1.08x faster                                                  |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                   |
| richards                   | 45.2 ms                                                      | 42.1 ms: 1.07x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 105 ms: 1.07x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 689 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.0 ms: 1.05x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.85 us: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                  |
| thrift                     | 778 us                                                       | 749 us: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.5 ms: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 99.7 ns: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 80.7 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.66 us: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.3 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.28 ms: 1.01x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                   |
| sympy_str                  | 275 ms                                                       | 272 ms: 1.01x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.6 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.0 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| raytrace                   | 253 ms                                                       | 257 ms: 1.02x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 69.2 ms: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 475 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 542 ms: 1.04x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                  |
| fannkuch                   | 370 ms                                                       | 387 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.34 ms: 1.07x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.89 ms: 1.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.30 ms: 1.42x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.66 ms: 1.48x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.43x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 312 ms: 28.41x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): typing_runtime_protocols, meteor_contest, nqueens
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251229-3.15.0a3+-b6b0e14/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x