# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_120321_gen_atomic
- machine: linux-x86_64
- commit hash: bc054db
- commit date: 2025-12-11
- overall geometric mean: 1.009x slower
- HPT reliability: 57.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 269 ms: 1.04x slower                                                      |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 67.0 ms                                                      | 63.1 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                        | 1.00x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                      |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 337 ms: 1.37x faster                                                      |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.31x faster                                                      |
| async_tree_none            | 354 ms                                                       | 270 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 515 ms: 1.29x faster                                                      |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.04x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                      |
| float          | 77.5 ms                                                      | 68.8 ms: 1.13x faster                                                     |
| nbody          | 85.1 ms                                                      | 115 ms: 1.35x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                     |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| regex_compile  | 132 ms                                                       | 134 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.75 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.4 ms: 1.02x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 88.0 ms: 1.03x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 62.4 ms: 1.05x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 225 us: 1.07x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                      |
| xml_etree_parse      | 136 ms                                                       | 148 ms: 1.09x slower                                                      |
| tomli_loads          | 2.01 sec                                                     | 2.21 sec: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                                     |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                     |
| genshi_xml      | 48.8 ms                                                      | 52.9 ms: 1.08x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 23.9 ms: 1.11x slower                                                     |
| mako            | 11.3 ms                                                      | 14.9 ms: 1.31x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.14x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.28 sec: 1.84x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 7.32 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                      |
| deepcopy                   | 355 us                                                       | 246 us: 1.44x faster                                                      |
| gc_traversal               | 3.14 ms                                                      | 2.26 ms: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 337 ms: 1.37x faster                                                      |
| deepcopy_memo              | 39.1 us                                                      | 28.8 us: 1.36x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 251 ms: 1.34x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 313 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.31x faster                                                      |
| async_tree_none            | 354 ms                                                       | 270 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 515 ms: 1.29x faster                                                      |
| go                         | 141 ms                                                       | 113 ms: 1.24x faster                                                      |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.18x faster                                                     |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                      |
| logging_silent             | 103 ns                                                       | 89.5 ns: 1.15x faster                                                     |
| float                      | 77.5 ms                                                      | 68.8 ms: 1.13x faster                                                     |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                     |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                      |
| pylint                     | 317 ms                                                       | 285 ms: 1.11x faster                                                      |
| spectral_norm              | 111 ms                                                       | 101 ms: 1.10x faster                                                      |
| sqlite_synth               | 2.21 us                                                      | 2.03 us: 1.09x faster                                                     |
| json_dumps                 | 10.5 ms                                                      | 9.75 ms: 1.08x faster                                                     |
| html5lib                   | 67.0 ms                                                      | 63.1 ms: 1.06x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.5 ms: 1.04x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 72.4 ms: 1.03x faster                                                     |
| pyflate                    | 449 ms                                                       | 435 ms: 1.03x faster                                                      |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.4 ms: 1.02x faster                                                     |
| json                       | 4.93 ms                                                      | 4.86 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 730 ms: 1.01x faster                                                      |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                      |
| richards                   | 45.2 ms                                                      | 45.0 ms: 1.01x faster                                                     |
| comprehensions             | 16.5 us                                                      | 16.6 us: 1.01x slower                                                     |
| chaos                      | 57.3 ms                                                      | 57.7 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.51 sec: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.24 us: 1.01x slower                                                     |
| regex_compile              | 132 ms                                                       | 134 ms: 1.02x slower                                                      |
| richards_super             | 51.6 ms                                                      | 52.9 ms: 1.03x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 20.4 ms: 1.03x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 88.0 ms: 1.03x slower                                                     |
| 2to3                       | 260 ms                                                       | 269 ms: 1.04x slower                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 68.5 ms: 1.05x slower                                                     |
| logging_format             | 6.84 us                                                      | 7.19 us: 1.05x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 62.4 ms: 1.05x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 6.30 ms: 1.05x slower                                                     |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 83.5 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.02 ms: 1.07x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 166 ms: 1.07x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 225 us: 1.07x slower                                                      |
| sympy_str                  | 275 ms                                                       | 295 ms: 1.07x slower                                                      |
| thrift                     | 778 us                                                       | 837 us: 1.08x slower                                                      |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                      |
| raytrace                   | 253 ms                                                       | 274 ms: 1.08x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 52.9 ms: 1.08x slower                                                     |
| sympy_expand               | 457 ms                                                       | 496 ms: 1.08x slower                                                      |
| xml_etree_parse            | 136 ms                                                       | 148 ms: 1.09x slower                                                      |
| generators                 | 28.8 ms                                                      | 31.4 ms: 1.09x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.40 ms: 1.09x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 169 us: 1.09x slower                                                      |
| fannkuch                   | 370 ms                                                       | 406 ms: 1.10x slower                                                      |
| tomli_loads                | 2.01 sec                                                     | 2.21 sec: 1.10x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 23.9 ms: 1.11x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.53 ms: 1.14x slower                                                     |
| coverage                   | 83.0 ms                                                      | 95.9 ms: 1.16x slower                                                     |
| meteor_contest             | 102 ms                                                       | 118 ms: 1.16x slower                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 81.2 ms: 1.20x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 9.62 ms: 1.30x slower                                                     |
| mako                       | 11.3 ms                                                      | 14.9 ms: 1.31x slower                                                     |
| nbody                      | 85.1 ms                                                      | 115 ms: 1.35x slower                                                      |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.45 ms: 1.57x slower                                                     |
| telco                      | 7.82 ms                                                      | 165 ms: 21.09x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251211-3.15.0a2+-bc054db-CLANG,NOGIL/bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 57.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.44x