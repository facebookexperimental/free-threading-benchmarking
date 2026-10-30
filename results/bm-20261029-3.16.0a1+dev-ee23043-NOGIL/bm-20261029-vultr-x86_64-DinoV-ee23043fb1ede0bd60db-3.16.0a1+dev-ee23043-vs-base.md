# Results vs. base

- fork: DinoV
- ref: ee23043fb1ede0bd60db
- machine: linux-x86_64
- commit hash: ee23043
- commit date: 2026-10-29
- overall geometric mean: 1.010x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 293 ms                                                                    | 296 ms: 1.01x slower                                                     |
| docutils       | 2.89 sec                                                                  | 2.91 sec: 1.01x slower                                                   |
| html5lib       | 66.3 ms                                                                   | 65.3 ms: 1.01x faster                                                    |
| sphinx         | 1.12 sec                                                                  | 1.13 sec: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 26.4 ms                                                                   | 25.9 ms: 1.02x faster                                                    |
| asyncio_websockets         | 509 ms                                                                    | 513 ms: 1.01x slower                                                     |
| async_generators           | 290 ms                                                                    | 294 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg | 585 ms                                                                    | 596 ms: 1.02x slower                                                     |
| async_tree_none            | 343 ms                                                                    | 354 ms: 1.03x slower                                                     |
| async_tree_memoization_tg  | 405 ms                                                                    | 418 ms: 1.03x slower                                                     |
| async_tree_io              | 715 ms                                                                    | 743 ms: 1.04x slower                                                     |
| async_tree_none_tg         | 334 ms                                                                    | 354 ms: 1.06x slower                                                     |
| async_tree_io_tg           | 695 ms                                                                    | 736 ms: 1.06x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.02x slower                                                             |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 188 ms                                                                    | 181 ms: 1.04x faster                                                     |
| nbody          | 116 ms                                                                    | 117 ms: 1.01x slower                                                     |
| float          | 84.3 ms                                                                   | 90.9 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 171 ms                                                                    | 170 ms: 1.00x faster                                                     |
| regex_v8       | 20.9 ms                                                                   | 21.2 ms: 1.01x slower                                                    |
| regex_dna      | 172 ms                                                                    | 184 ms: 1.07x slower                                                     |
| regex_effbot   | 2.74 ms                                                                   | 3.03 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 348 us                                                                    | 341 us: 1.02x faster                                                     |
| unpickle_pure_python | 242 us                                                                    | 238 us: 1.02x faster                                                     |
| json_loads           | 30.5 us                                                                   | 30.0 us: 1.02x faster                                                    |
| json_dumps           | 10.2 ms                                                                   | 10.3 ms: 1.01x slower                                                    |
| tomli_loads          | 1.92 sec                                                                  | 1.94 sec: 1.01x slower                                                   |
| xml_etree_iterparse  | 96.3 ms                                                                   | 97.4 ms: 1.01x slower                                                    |
| xml_etree_process    | 76.7 ms                                                                   | 78.2 ms: 1.02x slower                                                    |
| xml_etree_generate   | 102 ms                                                                    | 105 ms: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                                     | 1.00x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 13.9 ms                                                                   | 14.5 ms: 1.04x slower                                                    |
| python_startup_no_site | 9.10 ms                                                                   | 9.66 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                                     | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 15.9 ms                                                                   | 16.2 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20261030-vultr-x86_64-python-386d9d071cee2168bee1-3.16.0a1+dev-386d9d0 | bm-20261029-vultr-x86_64-DinoV-ee23043fb1ede0bd60db-3.16.0a1+dev-ee23043 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_sparse_mat_mult    | 5.05 ms                                                                   | 4.82 ms: 1.05x faster                                                    |
| pidigits                   | 188 ms                                                                    | 181 ms: 1.04x faster                                                     |
| generators                 | 34.2 ms                                                                   | 33.0 ms: 1.04x faster                                                    |
| logging_silent             | 110 ns                                                                    | 107 ns: 1.03x faster                                                     |
| deepcopy_reduce            | 3.06 us                                                                   | 2.96 us: 1.03x faster                                                    |
| pickle_pure_python         | 348 us                                                                    | 341 us: 1.02x faster                                                     |
| scimark_lu                 | 131 ms                                                                    | 128 ms: 1.02x faster                                                     |
| coroutines                 | 26.4 ms                                                                   | 25.9 ms: 1.02x faster                                                    |
| unpickle_pure_python       | 242 us                                                                    | 238 us: 1.02x faster                                                     |
| json_loads                 | 30.5 us                                                                   | 30.0 us: 1.02x faster                                                    |
| html5lib                   | 66.3 ms                                                                   | 65.3 ms: 1.01x faster                                                    |
| json                       | 5.40 ms                                                                   | 5.34 ms: 1.01x faster                                                    |
| subparsers                 | 10.4 ms                                                                   | 10.3 ms: 1.01x faster                                                    |
| coverage                   | 118 ms                                                                    | 117 ms: 1.01x faster                                                     |
| chaos                      | 60.7 ms                                                                   | 60.3 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.05 us                                                                   | 2.03 us: 1.01x faster                                                    |
| telco                      | 178 ms                                                                    | 177 ms: 1.01x faster                                                     |
| nqueens                    | 89.1 ms                                                                   | 88.6 ms: 1.00x faster                                                    |
| comprehensions             | 17.9 us                                                                   | 17.8 us: 1.00x faster                                                    |
| richards                   | 52.9 ms                                                                   | 52.7 ms: 1.00x faster                                                    |
| fannkuch                   | 469 ms                                                                    | 467 ms: 1.00x faster                                                     |
| pprint_pformat             | 1.71 sec                                                                  | 1.70 sec: 1.00x faster                                                   |
| richards_super             | 60.5 ms                                                                   | 60.3 ms: 1.00x faster                                                    |
| regex_compile              | 171 ms                                                                    | 170 ms: 1.00x faster                                                     |
| scimark_fft                | 319 ms                                                                    | 320 ms: 1.00x slower                                                     |
| create_gc_cycles           | 1.32 ms                                                                   | 1.32 ms: 1.00x slower                                                    |
| dulwich_log                | 70.3 ms                                                                   | 70.6 ms: 1.00x slower                                                    |
| sympy_sum                  | 183 ms                                                                    | 184 ms: 1.01x slower                                                     |
| meteor_contest             | 125 ms                                                                    | 126 ms: 1.01x slower                                                     |
| deepcopy_memo              | 33.0 us                                                                   | 33.2 us: 1.01x slower                                                    |
| bpe_tokeniser              | 4.39 sec                                                                  | 4.41 sec: 1.01x slower                                                   |
| pprint_safe_repr           | 825 ms                                                                    | 830 ms: 1.01x slower                                                     |
| pathlib                    | 18.5 ms                                                                   | 18.6 ms: 1.01x slower                                                    |
| asyncio_websockets         | 509 ms                                                                    | 513 ms: 1.01x slower                                                     |
| 2to3                       | 293 ms                                                                    | 296 ms: 1.01x slower                                                     |
| json_dumps                 | 10.2 ms                                                                   | 10.3 ms: 1.01x slower                                                    |
| docutils                   | 2.89 sec                                                                  | 2.91 sec: 1.01x slower                                                   |
| sphinx                     | 1.12 sec                                                                  | 1.13 sec: 1.01x slower                                                   |
| tomli_loads                | 1.92 sec                                                                  | 1.94 sec: 1.01x slower                                                   |
| hexiom                     | 6.57 ms                                                                   | 6.63 ms: 1.01x slower                                                    |
| gc_traversal               | 1.79 ms                                                                   | 1.80 ms: 1.01x slower                                                    |
| many_optionals             | 982 us                                                                    | 992 us: 1.01x slower                                                     |
| mdp                        | 1.30 sec                                                                  | 1.31 sec: 1.01x slower                                                   |
| xml_etree_iterparse        | 96.3 ms                                                                   | 97.4 ms: 1.01x slower                                                    |
| regex_v8                   | 20.9 ms                                                                   | 21.2 ms: 1.01x slower                                                    |
| nbody                      | 116 ms                                                                    | 117 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 140 us                                                                    | 141 us: 1.01x slower                                                     |
| mako                       | 15.9 ms                                                                   | 16.2 ms: 1.01x slower                                                    |
| scimark_sor                | 119 ms                                                                    | 121 ms: 1.01x slower                                                     |
| async_generators           | 290 ms                                                                    | 294 ms: 1.02x slower                                                     |
| crypto_pyaes               | 87.7 ms                                                                   | 89.2 ms: 1.02x slower                                                    |
| thrift                     | 933 us                                                                    | 949 us: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg | 585 ms                                                                    | 596 ms: 1.02x slower                                                     |
| xml_etree_process          | 76.7 ms                                                                   | 78.2 ms: 1.02x slower                                                    |
| pyflate                    | 450 ms                                                                    | 459 ms: 1.02x slower                                                     |
| k_core                     | 2.24 sec                                                                  | 2.30 sec: 1.02x slower                                                   |
| pycparser                  | 1.16 sec                                                                  | 1.19 sec: 1.03x slower                                                   |
| xml_etree_generate         | 102 ms                                                                    | 105 ms: 1.03x slower                                                     |
| async_tree_none            | 343 ms                                                                    | 354 ms: 1.03x slower                                                     |
| async_tree_memoization_tg  | 405 ms                                                                    | 418 ms: 1.03x slower                                                     |
| shortest_path              | 530 ms                                                                    | 550 ms: 1.04x slower                                                     |
| async_tree_io              | 715 ms                                                                    | 743 ms: 1.04x slower                                                     |
| connected_components       | 486 ms                                                                    | 506 ms: 1.04x slower                                                     |
| python_startup             | 13.9 ms                                                                   | 14.5 ms: 1.04x slower                                                    |
| spectral_norm              | 98.7 ms                                                                   | 103 ms: 1.04x slower                                                     |
| logging_format             | 7.97 us                                                                   | 8.40 us: 1.05x slower                                                    |
| async_tree_none_tg         | 334 ms                                                                    | 354 ms: 1.06x slower                                                     |
| async_tree_io_tg           | 695 ms                                                                    | 736 ms: 1.06x slower                                                     |
| python_startup_no_site     | 9.10 ms                                                                   | 9.66 ms: 1.06x slower                                                    |
| regex_dna                  | 172 ms                                                                    | 184 ms: 1.07x slower                                                     |
| logging_simple             | 7.02 us                                                                   | 7.55 us: 1.07x slower                                                    |
| float                      | 84.3 ms                                                                   | 90.9 ms: 1.08x slower                                                    |
| bench_mp_pool              | 6.58 ms                                                                   | 7.16 ms: 1.09x slower                                                    |
| regex_effbot               | 2.74 ms                                                                   | 3.03 ms: 1.10x slower                                                    |
| Geometric mean             | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (18): scimark_monte_carlo, bench_thread_pool, go, sympy_expand, django_template, xml_etree_parse, sympy_str, sympy_integrate, deepcopy, sqlglot_v2_transpile, raytrace, sqlglot_v2_normalize, deltablue, sqlglot_v2_parse, sqlglot_v2_optimize, async_tree_memoization, async_tree_cpu_io_mixed, pylint

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x