# Results vs. 3.12.6

- fork: python
- ref: 7dbc7975db8e34db8be8
- machine: linux-x86_64
- commit hash: 7dbc797
- commit date: 2026-10-18
- overall geometric mean: 1.045x slower
- HPT reliability: 86.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 293 ms: 1.11x slower                                                      |
| docutils       | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                    |
| html5lib       | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                  | 1.09x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 707 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 404 ms: 1.38x faster                                                      |
| async_tree_none            | 464 ms                                                 | 345 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 428 ms: 1.30x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 684 ms: 1.06x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 701 ms: 1.02x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                      |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                     |
| async_generators           | 384 ms                                                 | 417 ms: 1.08x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 83.5 ms: 1.03x slower                                                     |
| pidigits       | 184 ms                                                 | 218 ms: 1.18x slower                                                      |
| nbody          | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                  | 1.16x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                      |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 96.4 ms: 1.00x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                      |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 75.4 ms: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                     |
| python_startup         | 9.93 ms                                                | 16.2 ms: 1.63x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.8 ms: 1.20x slower                                                     |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 130 ms: 2.45x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.72 ms: 1.61x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 707 ms: 1.57x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 404 ms: 1.38x faster                                                      |
| async_tree_none            | 464 ms                                                 | 345 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                      |
| deepcopy                   | 352 us                                                 | 271 us: 1.30x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 428 ms: 1.30x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 33.0 us: 1.22x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                     |
| go                         | 139 ms                                                 | 121 ms: 1.16x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 143 us: 1.14x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.2 ms: 1.11x faster                                                     |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.09x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                    |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 684 ms: 1.06x faster                                                      |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.05x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.93 us: 1.05x faster                                                     |
| chaos                      | 62.8 ms                                                | 60.4 ms: 1.04x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                     |
| scimark_fft                | 342 ms                                                 | 332 ms: 1.03x faster                                                      |
| pyflate                    | 448 ms                                                 | 438 ms: 1.02x faster                                                      |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 701 ms: 1.02x faster                                                      |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 96.4 ms: 1.00x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                      |
| float                      | 80.8 ms                                                | 83.5 ms: 1.03x slower                                                     |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                      |
| generators                 | 32.2 ms                                                | 33.7 ms: 1.05x slower                                                     |
| html5lib                   | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.60 ms: 1.07x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                     |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.70 ms: 1.07x slower                                                     |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                                     |
| logging_format             | 7.35 us                                                | 7.95 us: 1.08x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                      |
| async_generators           | 384 ms                                                 | 417 ms: 1.08x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                      |
| docutils                   | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                    |
| sympy_str                  | 292 ms                                                 | 321 ms: 1.10x slower                                                      |
| nqueens                    | 80.1 ms                                                | 88.2 ms: 1.10x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 819 ms: 1.10x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 183 ms: 1.11x slower                                                      |
| 2to3                       | 264 ms                                                 | 293 ms: 1.11x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 76.6 ms: 1.12x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.01 ms: 1.14x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                      |
| richards                   | 45.9 ms                                                | 52.7 ms: 1.15x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| sympy_expand               | 468 ms                                                 | 540 ms: 1.15x slower                                                      |
| richards_super             | 51.9 ms                                                | 60.2 ms: 1.16x slower                                                     |
| pidigits                   | 184 ms                                                 | 218 ms: 1.18x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                      |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                      |
| thrift                     | 791 us                                                 | 947 us: 1.20x slower                                                      |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.20x slower                                                      |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.20x slower                                                     |
| fannkuch                   | 372 ms                                                 | 462 ms: 1.24x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.25x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 75.4 ms: 1.28x slower                                                     |
| nbody                      | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                     |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                     |
| coverage                   | 71.4 ms                                                | 116 ms: 1.62x slower                                                      |
| python_startup             | 9.93 ms                                                | 16.2 ms: 1.63x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.64 ms: 1.74x slower                                                     |
| telco                      | 6.53 ms                                                | 179 ms: 27.41x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                              |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261018-3.16.0a1+dev-7dbc797-NOGIL/bm-20261018-vultr-x86_64-python-7dbc7975db8e34db8be8-3.16.0a1+dev-7dbc797.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 86.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x