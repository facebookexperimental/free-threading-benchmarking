# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: b10c3be
- commit date: 2025-02-26
- overall geometric mean: 1.025x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 297 ms: 1.03x faster                                                  |
| docutils       | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                | 24.1 ms                                                                | 23.4 ms: 1.03x faster                                                 |
| async_tree_memoization_tg | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| async_tree_none           | 275 ms                                                                 | 271 ms: 1.01x faster                                                  |
| async_tree_none_tg        | 237 ms                                                                 | 234 ms: 1.01x faster                                                  |
| async_tree_memoization    | 340 ms                                                                 | 337 ms: 1.01x faster                                                  |
| asyncio_websockets        | 512 ms                                                                 | 518 ms: 1.01x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (5): async_tree_io, async_generators, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 135 ms                                                                 | 122 ms: 1.11x faster                                                  |
| float          | 76.5 ms                                                                | 70.6 ms: 1.08x faster                                                 |
| pidigits       | 212 ms                                                                 | 198 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                                 | 153 ms: 1.02x faster                                                  |
| regex_effbot   | 2.77 ms                                                                | 2.82 ms: 1.02x slower                                                 |
| regex_v8       | 23.1 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| regex_dna      | 169 ms                                                                 | 182 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 371 us                                                                 | 347 us: 1.07x faster                                                  |
| tomli_loads          | 2.43 sec                                                               | 2.29 sec: 1.06x faster                                                |
| unpickle_pure_python | 255 us                                                                 | 241 us: 1.06x faster                                                  |
| json_dumps           | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 70.1 ms                                                                | 69.9 ms: 1.00x faster                                                 |
| xml_etree_iterparse  | 87.2 ms                                                                | 88.5 ms: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_generate, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.68 ms                                                                | 9.62 ms: 1.01x faster                                                 |
| python_startup         | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 28.5 ms                                                                | 26.9 ms: 1.06x faster                                                 |
| genshi_xml      | 60.0 ms                                                                | 57.7 ms: 1.04x faster                                                 |
| django_template | 43.5 ms                                                                | 42.4 ms: 1.03x faster                                                 |
| mako            | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                     | 135 ms                                                                 | 122 ms: 1.11x faster                                                  |
| scimark_fft               | 399 ms                                                                 | 361 ms: 1.10x faster                                                  |
| scimark_sparse_mat_mult   | 5.62 ms                                                                | 5.12 ms: 1.10x faster                                                 |
| scimark_monte_carlo       | 84.7 ms                                                                | 77.4 ms: 1.09x faster                                                 |
| go                        | 144 ms                                                                 | 132 ms: 1.09x faster                                                  |
| scimark_sor               | 138 ms                                                                 | 127 ms: 1.09x faster                                                  |
| float                     | 76.5 ms                                                                | 70.6 ms: 1.08x faster                                                 |
| spectral_norm             | 115 ms                                                                 | 106 ms: 1.08x faster                                                  |
| raytrace                  | 324 ms                                                                 | 302 ms: 1.08x faster                                                  |
| pidigits                  | 212 ms                                                                 | 198 ms: 1.07x faster                                                  |
| logging_silent            | 116 ns                                                                 | 108 ns: 1.07x faster                                                  |
| pyflate                   | 507 ms                                                                 | 474 ms: 1.07x faster                                                  |
| pickle_pure_python        | 371 us                                                                 | 347 us: 1.07x faster                                                  |
| tomli_loads               | 2.43 sec                                                               | 2.29 sec: 1.06x faster                                                |
| deltablue                 | 3.91 ms                                                                | 3.67 ms: 1.06x faster                                                 |
| fannkuch                  | 496 ms                                                                 | 466 ms: 1.06x faster                                                  |
| sqlglot_parse             | 1.60 ms                                                                | 1.51 ms: 1.06x faster                                                 |
| unpickle_pure_python      | 255 us                                                                 | 241 us: 1.06x faster                                                  |
| genshi_text               | 28.5 ms                                                                | 26.9 ms: 1.06x faster                                                 |
| hexiom                    | 7.63 ms                                                                | 7.22 ms: 1.06x faster                                                 |
| chaos                     | 70.6 ms                                                                | 66.9 ms: 1.06x faster                                                 |
| deepcopy_memo             | 38.6 us                                                                | 36.7 us: 1.05x faster                                                 |
| pprint_safe_repr          | 845 ms                                                                 | 804 ms: 1.05x faster                                                  |
| pprint_pformat            | 1.74 sec                                                               | 1.66 sec: 1.05x faster                                                |
| richards_super            | 64.5 ms                                                                | 61.6 ms: 1.05x faster                                                 |
| sqlglot_transpile         | 1.93 ms                                                                | 1.84 ms: 1.05x faster                                                 |
| richards                  | 55.5 ms                                                                | 53.1 ms: 1.05x faster                                                 |
| deepcopy                  | 314 us                                                                 | 300 us: 1.04x faster                                                  |
| comprehensions            | 20.3 us                                                                | 19.5 us: 1.04x faster                                                 |
| nqueens                   | 98.5 ms                                                                | 94.4 ms: 1.04x faster                                                 |
| genshi_xml                | 60.0 ms                                                                | 57.7 ms: 1.04x faster                                                 |
| meteor_contest            | 128 ms                                                                 | 124 ms: 1.04x faster                                                  |
| crypto_pyaes              | 88.3 ms                                                                | 85.1 ms: 1.04x faster                                                 |
| deepcopy_reduce           | 3.18 us                                                                | 3.08 us: 1.03x faster                                                 |
| bpe_tokeniser             | 4.79 sec                                                               | 4.65 sec: 1.03x faster                                                |
| coroutines                | 24.1 ms                                                                | 23.4 ms: 1.03x faster                                                 |
| 2to3                      | 305 ms                                                                 | 297 ms: 1.03x faster                                                  |
| scimark_lu                | 139 ms                                                                 | 136 ms: 1.03x faster                                                  |
| django_template           | 43.5 ms                                                                | 42.4 ms: 1.03x faster                                                 |
| logging_format            | 8.31 us                                                                | 8.11 us: 1.03x faster                                                 |
| regex_compile             | 156 ms                                                                 | 153 ms: 1.02x faster                                                  |
| connected_components      | 494 ms                                                                 | 483 ms: 1.02x faster                                                  |
| shortest_path             | 548 ms                                                                 | 537 ms: 1.02x faster                                                  |
| json_dumps                | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| sqlglot_normalize         | 121 ms                                                                 | 119 ms: 1.02x faster                                                  |
| pycparser                 | 1.19 sec                                                               | 1.17 sec: 1.02x faster                                                |
| json                      | 5.15 ms                                                                | 5.06 ms: 1.02x faster                                                 |
| async_tree_memoization_tg | 307 ms                                                                 | 302 ms: 1.02x faster                                                  |
| sympy_integrate           | 24.2 ms                                                                | 23.8 ms: 1.02x faster                                                 |
| mdp                       | 2.77 sec                                                               | 2.73 sec: 1.02x faster                                                |
| k_core                    | 2.30 sec                                                               | 2.26 sec: 1.02x faster                                                |
| sqlglot_optimize          | 61.4 ms                                                                | 60.5 ms: 1.01x faster                                                 |
| typing_runtime_protocols  | 201 us                                                                 | 198 us: 1.01x faster                                                  |
| many_optionals            | 1.17 ms                                                                | 1.15 ms: 1.01x faster                                                 |
| coverage                  | 96.9 ms                                                                | 95.7 ms: 1.01x faster                                                 |
| async_tree_none           | 275 ms                                                                 | 271 ms: 1.01x faster                                                  |
| async_tree_none_tg        | 237 ms                                                                 | 234 ms: 1.01x faster                                                  |
| docutils                  | 2.80 sec                                                               | 2.77 sec: 1.01x faster                                                |
| sympy_str                 | 335 ms                                                                 | 332 ms: 1.01x faster                                                  |
| async_tree_memoization    | 340 ms                                                                 | 337 ms: 1.01x faster                                                  |
| bench_thread_pool         | 3.32 ms                                                                | 3.29 ms: 1.01x faster                                                 |
| mako                      | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                                 |
| bench_mp_pool             | 95.4 ms                                                                | 94.7 ms: 1.01x faster                                                 |
| telco                     | 8.61 ms                                                                | 8.55 ms: 1.01x faster                                                 |
| pathlib                   | 19.9 ms                                                                | 19.8 ms: 1.01x faster                                                 |
| python_startup_no_site    | 9.68 ms                                                                | 9.62 ms: 1.01x faster                                                 |
| xml_etree_process         | 70.1 ms                                                                | 69.9 ms: 1.00x faster                                                 |
| python_startup            | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| gc_traversal              | 1.71 ms                                                                | 1.72 ms: 1.01x slower                                                 |
| sqlalchemy_declarative    | 156 ms                                                                 | 158 ms: 1.01x slower                                                  |
| asyncio_websockets        | 512 ms                                                                 | 518 ms: 1.01x slower                                                  |
| thrift                    | 867 us                                                                 | 878 us: 1.01x slower                                                  |
| subparsers                | 25.1 ms                                                                | 25.5 ms: 1.01x slower                                                 |
| xml_etree_iterparse       | 87.2 ms                                                                | 88.5 ms: 1.02x slower                                                 |
| regex_effbot              | 2.77 ms                                                                | 2.82 ms: 1.02x slower                                                 |
| generators                | 31.9 ms                                                                | 32.5 ms: 1.02x slower                                                 |
| regex_v8                  | 23.1 ms                                                                | 24.3 ms: 1.05x slower                                                 |
| regex_dna                 | 169 ms                                                                 | 182 ms: 1.08x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (18): sqlalchemy_imperative, async_tree_io, sphinx, async_generators, sympy_expand, async_tree_cpu_io_mixed_tg, create_gc_cycles, xml_etree_generate, html5lib, dulwich_log, logging_simple, json_loads, sympy_sum, xml_etree_parse, async_tree_cpu_io_mixed, sqlite_synth, pylint, async_tree_io_tg

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x