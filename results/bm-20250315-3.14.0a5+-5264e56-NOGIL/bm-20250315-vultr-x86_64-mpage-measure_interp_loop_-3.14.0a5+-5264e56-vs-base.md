# Results vs. base

- fork: mpage
- ref: measure_interp_loop_
- machine: linux-x86_64
- commit hash: 5264e56
- commit date: 2025-03-15
- overall geometric mean: 1.015x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 299 ms                                                                 | 296 ms: 1.01x faster                                                  |
| docutils       | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                                |
| html5lib       | 72.0 ms                                                                | 71.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 484 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 518 ms: 1.08x faster                                                  |
| coroutines                 | 24.1 ms                                                                | 23.1 ms: 1.04x faster                                                 |
| async_tree_none_tg         | 236 ms                                                                 | 231 ms: 1.02x faster                                                  |
| async_tree_none            | 275 ms                                                                 | 270 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 546 ms                                                                 | 536 ms: 1.02x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 333 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 304 ms                                                                 | 300 ms: 1.02x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 576 ms: 1.01x faster                                                  |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 125 ms: 1.07x faster                                                  |
| float          | 77.9 ms                                                                | 73.3 ms: 1.06x faster                                                 |
| pidigits       | 202 ms                                                                 | 191 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 184 ms                                                                 | 180 ms: 1.02x faster                                                  |
| regex_compile  | 158 ms                                                                 | 155 ms: 1.02x faster                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.66 ms: 1.02x faster                                                 |
| regex_v8       | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 257 us                                                                 | 250 us: 1.03x faster                                                  |
| tomli_loads          | 2.38 sec                                                               | 2.33 sec: 1.02x faster                                                |
| pickle_pure_python   | 360 us                                                                 | 356 us: 1.01x faster                                                  |
| json_dumps           | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                                 |
| xml_etree_process    | 70.4 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| xml_etree_generate   | 96.6 ms                                                                | 96.9 ms: 1.00x slower                                                 |
| xml_etree_iterparse  | 87.7 ms                                                                | 88.6 ms: 1.01x slower                                                 |
| json_loads           | 29.2 us                                                                | 29.5 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 43.1 ms                                                                | 42.1 ms: 1.02x faster                                                 |
| mako            | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| genshi_xml      | 59.6 ms                                                                | 59.9 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 | bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5+-5264e56 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 530 ms                                                                 | 484 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 561 ms                                                                 | 518 ms: 1.08x faster                                                  |
| go                         | 145 ms                                                                 | 135 ms: 1.07x faster                                                  |
| nbody                      | 134 ms                                                                 | 125 ms: 1.07x faster                                                  |
| float                      | 77.9 ms                                                                | 73.3 ms: 1.06x faster                                                 |
| pidigits                   | 202 ms                                                                 | 191 ms: 1.05x faster                                                  |
| richards                   | 55.1 ms                                                                | 52.4 ms: 1.05x faster                                                 |
| deltablue                  | 3.90 ms                                                                | 3.72 ms: 1.05x faster                                                 |
| chaos                      | 70.1 ms                                                                | 66.9 ms: 1.05x faster                                                 |
| pyflate                    | 509 ms                                                                 | 486 ms: 1.05x faster                                                  |
| coroutines                 | 24.1 ms                                                                | 23.1 ms: 1.04x faster                                                 |
| raytrace                   | 323 ms                                                                 | 310 ms: 1.04x faster                                                  |
| richards_super             | 63.7 ms                                                                | 61.2 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 3.26 us                                                                | 3.13 us: 1.04x faster                                                 |
| thrift                     | 889 us                                                                 | 859 us: 1.04x faster                                                  |
| unpickle_pure_python       | 257 us                                                                 | 250 us: 1.03x faster                                                  |
| scimark_monte_carlo        | 84.1 ms                                                                | 81.8 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.29 ms: 1.03x faster                                                 |
| django_template            | 43.1 ms                                                                | 42.1 ms: 1.02x faster                                                 |
| telco                      | 9.05 ms                                                                | 8.85 ms: 1.02x faster                                                 |
| async_tree_none_tg         | 236 ms                                                                 | 231 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.61 ms                                                                | 1.57 ms: 1.02x faster                                                 |
| regex_dna                  | 184 ms                                                                 | 180 ms: 1.02x faster                                                  |
| hexiom                     | 7.65 ms                                                                | 7.48 ms: 1.02x faster                                                 |
| logging_format             | 8.26 us                                                                | 8.08 us: 1.02x faster                                                 |
| tomli_loads                | 2.38 sec                                                               | 2.33 sec: 1.02x faster                                                |
| coverage                   | 99.6 ms                                                                | 97.6 ms: 1.02x faster                                                 |
| logging_silent             | 111 ns                                                                 | 109 ns: 1.02x faster                                                  |
| regex_compile              | 158 ms                                                                 | 155 ms: 1.02x faster                                                  |
| fannkuch                   | 499 ms                                                                 | 490 ms: 1.02x faster                                                  |
| async_tree_none            | 275 ms                                                                 | 270 ms: 1.02x faster                                                  |
| logging_simple             | 7.21 us                                                                | 7.08 us: 1.02x faster                                                 |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.84 sec                                                               | 4.76 sec: 1.02x faster                                                |
| async_tree_io_tg           | 546 ms                                                                 | 536 ms: 1.02x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 333 ms: 1.02x faster                                                  |
| subparsers                 | 25.6 ms                                                                | 25.2 ms: 1.02x faster                                                 |
| sympy_integrate            | 24.2 ms                                                                | 23.8 ms: 1.02x faster                                                 |
| regex_effbot               | 2.70 ms                                                                | 2.66 ms: 1.02x faster                                                 |
| gc_traversal               | 1.74 ms                                                                | 1.71 ms: 1.02x faster                                                 |
| async_tree_memoization_tg  | 304 ms                                                                 | 300 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.93 ms                                                                | 1.90 ms: 1.01x faster                                                 |
| html5lib                   | 72.0 ms                                                                | 71.0 ms: 1.01x faster                                                 |
| crypto_pyaes               | 87.8 ms                                                                | 86.6 ms: 1.01x faster                                                 |
| deepcopy_memo              | 38.8 us                                                                | 38.3 us: 1.01x faster                                                 |
| many_optionals             | 1.18 ms                                                                | 1.16 ms: 1.01x faster                                                 |
| comprehensions             | 21.1 us                                                                | 20.9 us: 1.01x faster                                                 |
| async_tree_io              | 583 ms                                                                 | 576 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 5.61 ms: 1.01x faster                                                 |
| pickle_pure_python         | 360 us                                                                 | 356 us: 1.01x faster                                                  |
| sqlalchemy_declarative     | 157 ms                                                                 | 156 ms: 1.01x faster                                                  |
| async_generators           | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| docutils                   | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                                |
| json_dumps                 | 12.8 ms                                                                | 12.7 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 848 ms                                                                 | 841 ms: 1.01x faster                                                  |
| sympy_sum                  | 188 ms                                                                 | 186 ms: 1.01x faster                                                  |
| 2to3                       | 299 ms                                                                 | 296 ms: 1.01x faster                                                  |
| bench_mp_pool              | 95.9 ms                                                                | 95.2 ms: 1.01x faster                                                 |
| mdp                        | 2.79 sec                                                               | 2.77 sec: 1.01x faster                                                |
| mako                       | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.74 sec                                                               | 1.73 sec: 1.01x faster                                                |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| spectral_norm              | 115 ms                                                                 | 114 ms: 1.01x faster                                                  |
| xml_etree_process          | 70.4 ms                                                                | 70.0 ms: 1.01x faster                                                 |
| python_startup             | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                 |
| k_core                     | 2.31 sec                                                               | 2.30 sec: 1.00x faster                                                |
| scimark_sor                | 136 ms                                                                 | 136 ms: 1.00x slower                                                  |
| xml_etree_generate         | 96.6 ms                                                                | 96.9 ms: 1.00x slower                                                 |
| genshi_xml                 | 59.6 ms                                                                | 59.9 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 87.7 ms                                                                | 88.6 ms: 1.01x slower                                                 |
| json_loads                 | 29.2 us                                                                | 29.5 us: 1.01x slower                                                 |
| regex_v8                   | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                 |
| nqueens                    | 97.8 ms                                                                | 98.9 ms: 1.01x slower                                                 |
| scimark_lu                 | 139 ms                                                                 | 141 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| generators                 | 31.6 ms                                                                | 32.4 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (20): pylint, typing_runtime_protocols, sqlglot_optimize, deepcopy, sqlglot_normalize, connected_components, genshi_text, sqlite_synth, sphinx, sympy_str, shortest_path, dulwich_log, bench_thread_pool, sympy_expand, meteor_contest, json, asyncio_websockets, sqlalchemy_imperative, xml_etree_parse, scimark_fft

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x