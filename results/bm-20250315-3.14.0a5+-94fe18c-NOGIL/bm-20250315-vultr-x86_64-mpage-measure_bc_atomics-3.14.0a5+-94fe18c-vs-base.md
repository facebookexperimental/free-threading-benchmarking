# Results vs. base

- fork: mpage
- ref: measure_bc_atomics
- machine: linux-x86_64
- commit hash: 94fe18c
- commit date: 2025-03-15
- overall geometric mean: 1.008x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 297 ms: 1.01x faster                                                |
| html5lib       | 72.0 ms                                                                | 69.2 ms: 1.04x faster                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 486 ms: 1.09x faster                                                |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 518 ms: 1.08x faster                                                |
| coroutines                 | 24.1 ms                                                                | 23.9 ms: 1.01x faster                                               |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                                |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_memoization_tg, asyncio_websockets, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 77.9 ms                                                                | 75.9 ms: 1.03x faster                                               |
| nbody          | 134 ms                                                                 | 131 ms: 1.02x faster                                                |
| pidigits       | 202 ms                                                                 | 202 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 184 ms                                                                 | 169 ms: 1.09x faster                                                |
| regex_compile  | 158 ms                                                                 | 156 ms: 1.02x faster                                                |
| regex_v8       | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                               |
| regex_effbot   | 2.70 ms                                                                | 2.79 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 257 us                                                                 | 254 us: 1.01x faster                                                |
| pickle_pure_python   | 360 us                                                                 | 357 us: 1.01x faster                                                |
| json_dumps           | 12.8 ms                                                                | 12.8 ms: 1.01x faster                                               |
| tomli_loads          | 2.38 sec                                                               | 2.37 sec: 1.00x faster                                              |
| json_loads           | 29.2 us                                                                | 29.1 us: 1.00x faster                                               |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (3): xml_etree_generate, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                               |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                               |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                               |
| genshi_text    | 28.1 ms                                                                | 27.9 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 486 ms: 1.09x faster                                                |
| regex_dna                  | 184 ms                                                                 | 169 ms: 1.09x faster                                                |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 518 ms: 1.08x faster                                                |
| deepcopy_reduce            | 3.26 us                                                                | 3.13 us: 1.04x faster                                               |
| html5lib                   | 72.0 ms                                                                | 69.2 ms: 1.04x faster                                               |
| comprehensions             | 21.1 us                                                                | 20.5 us: 1.03x faster                                               |
| thrift                     | 889 us                                                                 | 862 us: 1.03x faster                                                |
| go                         | 145 ms                                                                 | 141 ms: 1.03x faster                                                |
| float                      | 77.9 ms                                                                | 75.9 ms: 1.03x faster                                               |
| richards                   | 55.1 ms                                                                | 53.7 ms: 1.02x faster                                               |
| telco                      | 9.05 ms                                                                | 8.84 ms: 1.02x faster                                               |
| pprint_safe_repr           | 848 ms                                                                 | 828 ms: 1.02x faster                                                |
| logging_simple             | 7.21 us                                                                | 7.05 us: 1.02x faster                                               |
| logging_format             | 8.26 us                                                                | 8.08 us: 1.02x faster                                               |
| coverage                   | 99.6 ms                                                                | 97.5 ms: 1.02x faster                                               |
| nbody                      | 134 ms                                                                 | 131 ms: 1.02x faster                                                |
| scimark_monte_carlo        | 84.1 ms                                                                | 82.6 ms: 1.02x faster                                               |
| sqlglot_parse              | 1.61 ms                                                                | 1.58 ms: 1.02x faster                                               |
| pprint_pformat             | 1.74 sec                                                               | 1.71 sec: 1.02x faster                                              |
| regex_compile              | 158 ms                                                                 | 156 ms: 1.02x faster                                                |
| chaos                      | 70.1 ms                                                                | 69.0 ms: 1.02x faster                                               |
| sqlglot_transpile          | 1.93 ms                                                                | 1.90 ms: 1.01x faster                                               |
| mako                       | 15.9 ms                                                                | 15.7 ms: 1.01x faster                                               |
| many_optionals             | 1.18 ms                                                                | 1.16 ms: 1.01x faster                                               |
| sympy_integrate            | 24.2 ms                                                                | 23.9 ms: 1.01x faster                                               |
| spectral_norm              | 115 ms                                                                 | 113 ms: 1.01x faster                                                |
| coroutines                 | 24.1 ms                                                                | 23.9 ms: 1.01x faster                                               |
| unpickle_pure_python       | 257 us                                                                 | 254 us: 1.01x faster                                                |
| bench_mp_pool              | 95.9 ms                                                                | 94.9 ms: 1.01x faster                                               |
| subparsers                 | 25.6 ms                                                                | 25.4 ms: 1.01x faster                                               |
| hexiom                     | 7.65 ms                                                                | 7.57 ms: 1.01x faster                                               |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                               |
| pickle_pure_python         | 360 us                                                                 | 357 us: 1.01x faster                                                |
| typing_runtime_protocols   | 197 us                                                                 | 195 us: 1.01x faster                                                |
| deltablue                  | 3.90 ms                                                                | 3.87 ms: 1.01x faster                                               |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                               |
| genshi_text                | 28.1 ms                                                                | 27.9 ms: 1.01x faster                                               |
| 2to3                       | 299 ms                                                                 | 297 ms: 1.01x faster                                                |
| sympy_sum                  | 188 ms                                                                 | 187 ms: 1.01x faster                                                |
| bpe_tokeniser              | 4.84 sec                                                               | 4.82 sec: 1.01x faster                                              |
| deepcopy_memo              | 38.8 us                                                                | 38.6 us: 1.01x faster                                               |
| json_dumps                 | 12.8 ms                                                                | 12.8 ms: 1.01x faster                                               |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                                |
| sqlalchemy_declarative     | 157 ms                                                                 | 157 ms: 1.00x faster                                                |
| tomli_loads                | 2.38 sec                                                               | 2.37 sec: 1.00x faster                                              |
| pycparser                  | 1.19 sec                                                               | 1.19 sec: 1.00x faster                                              |
| pyflate                    | 509 ms                                                                 | 507 ms: 1.00x faster                                                |
| crypto_pyaes               | 87.8 ms                                                                | 87.4 ms: 1.00x faster                                               |
| fannkuch                   | 499 ms                                                                 | 497 ms: 1.00x faster                                                |
| scimark_sor                | 136 ms                                                                 | 135 ms: 1.00x faster                                                |
| json_loads                 | 29.2 us                                                                | 29.1 us: 1.00x faster                                               |
| pidigits                   | 202 ms                                                                 | 202 ms: 1.00x slower                                                |
| logging_silent             | 111 ns                                                                 | 112 ns: 1.01x slower                                                |
| nqueens                    | 97.8 ms                                                                | 98.5 ms: 1.01x slower                                               |
| regex_v8                   | 23.4 ms                                                                | 23.6 ms: 1.01x slower                                               |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.01x slower                                                |
| scimark_lu                 | 139 ms                                                                 | 141 ms: 1.01x slower                                                |
| sqlite_synth               | 2.02 us                                                                | 2.05 us: 1.01x slower                                               |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                               |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 5.79 ms: 1.02x slower                                               |
| generators                 | 31.6 ms                                                                | 32.3 ms: 1.02x slower                                               |
| regex_effbot               | 2.70 ms                                                                | 2.79 ms: 1.03x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (34): pylint, richards_super, sqlalchemy_imperative, json, sphinx, sqlglot_normalize, connected_components, async_tree_memoization, docutils, sqlglot_optimize, scimark_fft, async_tree_none_tg, async_tree_none, async_tree_memoization_tg, mdp, raytrace, deepcopy, bench_thread_pool, sympy_expand, django_template, shortest_path, asyncio_websockets, async_tree_io, dulwich_log, gc_traversal, xml_etree_generate, xml_etree_process, sympy_str, create_gc_cycles, async_tree_io_tg, k_core, xml_etree_iterparse, genshi_xml, meteor_contest

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x