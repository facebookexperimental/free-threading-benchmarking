# Results vs. 3.12.6

- fork: colesbury
- ref: gh_120321_gen_atomic
- machine: linux-x86_64
- commit hash: bc054db
- commit date: 2025-12-11
- overall geometric mean: 1.025x faster
- HPT reliability: 95.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.45x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                      |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                      |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                      |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                      |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                     |
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                      |
| nbody          | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                     |
| regex_compile  | 142 ms                                                 | 134 ms: 1.06x faster                                                      |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                     |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                  | 1.00x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.4 ms                                                | 9.75 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 225 us: 1.02x slower                                                      |
| json_loads           | 26.5 us                                                | 27.1 us: 1.02x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 88.0 ms: 1.03x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.21 sec: 1.05x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 62.4 ms: 1.06x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 148 ms: 1.07x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                     |
| genshi_text     | 22.8 ms                                                | 23.9 ms: 1.05x slower                                                     |
| genshi_xml      | 50.2 ms                                                | 52.9 ms: 1.05x slower                                                     |
| mako            | 11.0 ms                                                | 14.9 ms: 1.35x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.12x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.28 sec: 1.89x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                      |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 2.26 ms: 1.53x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                      |
| bench_mp_pool              | 10.8 ms                                                | 7.32 ms: 1.47x faster                                                     |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 515 ms: 1.39x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                     |
| go                         | 139 ms                                                 | 113 ms: 1.23x faster                                                      |
| logging_silent             | 109 ns                                                 | 89.5 ns: 1.22x faster                                                     |
| comprehensions             | 19.8 us                                                | 16.6 us: 1.20x faster                                                     |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                      |
| float                      | 80.8 ms                                                | 68.8 ms: 1.17x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                     |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                      |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                    |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                      |
| raytrace                   | 299 ms                                                 | 274 ms: 1.09x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                     |
| spectral_norm              | 110 ms                                                 | 101 ms: 1.09x faster                                                      |
| chaos                      | 62.8 ms                                                | 57.7 ms: 1.09x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.75 ms: 1.06x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.24 us: 1.06x faster                                                     |
| regex_compile              | 142 ms                                                 | 134 ms: 1.06x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                     |
| json                       | 5.02 ms                                                | 4.86 ms: 1.03x faster                                                     |
| pyflate                    | 448 ms                                                 | 435 ms: 1.03x faster                                                      |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                                     |
| logging_format             | 7.35 us                                                | 7.19 us: 1.02x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                      |
| richards                   | 45.9 ms                                                | 45.0 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 730 ms: 1.02x faster                                                      |
| deltablue                  | 3.45 ms                                                | 3.40 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.51 sec: 1.01x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 20.4 ms: 1.01x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                    |
| sympy_str                  | 292 ms                                                 | 295 ms: 1.01x slower                                                      |
| pidigits                   | 184 ms                                                 | 187 ms: 1.01x slower                                                      |
| unpickle_pure_python       | 221 us                                                 | 225 us: 1.02x slower                                                      |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                      |
| richards_super             | 51.9 ms                                                | 52.9 ms: 1.02x slower                                                     |
| json_loads                 | 26.5 us                                                | 27.1 us: 1.02x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.30 ms: 1.02x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 88.0 ms: 1.03x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 169 us: 1.03x slower                                                      |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                     |
| nqueens                    | 80.1 ms                                                | 83.5 ms: 1.04x slower                                                     |
| genshi_text                | 22.8 ms                                                | 23.9 ms: 1.05x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.21 sec: 1.05x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 52.9 ms: 1.05x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                     |
| thrift                     | 791 us                                                 | 837 us: 1.06x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 62.4 ms: 1.06x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 81.2 ms: 1.06x slower                                                     |
| sympy_expand               | 468 ms                                                 | 496 ms: 1.06x slower                                                      |
| xml_etree_parse            | 139 ms                                                 | 148 ms: 1.07x slower                                                      |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                      |
| fannkuch                   | 372 ms                                                 | 406 ms: 1.09x slower                                                      |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.02 ms: 1.14x slower                                                     |
| nbody                      | 89.3 ms                                                | 115 ms: 1.29x slower                                                      |
| coverage                   | 71.4 ms                                                | 95.9 ms: 1.34x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                     |
| mako                       | 11.0 ms                                                | 14.9 ms: 1.35x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.45 ms: 1.54x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                     |
| telco                      | 6.53 ms                                                | 165 ms: 25.28x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (3): html5lib, sympy_sum, scimark_monte_carlo
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251211-3.15.0a2+-bc054db-CLANG,NOGIL/bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 95.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.45x