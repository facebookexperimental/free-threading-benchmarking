# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit_regalloc
- machine: linux-x86_64
- commit hash: 7be738d
- commit date: 2025-10-28
- overall geometric mean: 1.012x faster
- HPT reliability: 99.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| html5lib       | 60.6 ms                                                                | 67.2 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 496 ms                                                                 | 490 ms: 1.01x faster                                                             |
| async_tree_memoization_tg | 308 ms                                                                 | 309 ms: 1.01x slower                                                             |
| coroutines                | 23.8 ms                                                                | 24.1 ms: 1.01x slower                                                            |
| async_tree_io_tg          | 594 ms                                                                 | 603 ms: 1.01x slower                                                             |
| async_generators          | 361 ms                                                                 | 371 ms: 1.03x slower                                                             |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 87.8 ms                                                                | 73.5 ms: 1.19x faster                                                            |
| float          | 71.2 ms                                                                | 60.5 ms: 1.18x faster                                                            |
| pidigits       | 200 ms                                                                 | 194 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 2.72 ms                                                                | 2.55 ms: 1.06x faster                                                            |
| regex_dna      | 178 ms                                                                 | 168 ms: 1.06x faster                                                             |
| regex_compile  | 124 ms                                                                 | 127 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|---------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python  | 306 us                                                                 | 296 us: 1.04x faster                                                             |
| json_dumps          | 9.55 ms                                                                | 9.48 ms: 1.01x faster                                                            |
| xml_etree_iterparse | 84.3 ms                                                                | 83.7 ms: 1.01x faster                                                            |
| tomli_loads         | 1.77 sec                                                               | 1.80 sec: 1.02x slower                                                           |
| xml_etree_process   | 53.9 ms                                                                | 55.4 ms: 1.03x slower                                                            |
| xml_etree_generate  | 77.2 ms                                                                | 81.0 ms: 1.05x slower                                                            |
| Geometric mean      | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.23 ms                                                                | 7.28 ms: 1.01x slower                                                            |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.3 ms                                                                | 34.7 ms: 1.01x slower                                                            |
| mako            | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                            |
| genshi_text     | 20.4 ms                                                                | 21.3 ms: 1.04x slower                                                            |
| genshi_xml      | 47.8 ms                                                                | 54.0 ms: 1.13x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                 | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit_regalloc-3.15.0a1+-7be738d |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| richards                  | 41.1 ms                                                                | 20.0 ms: 2.05x faster                                                            |
| richards_super            | 47.0 ms                                                                | 24.0 ms: 1.96x faster                                                            |
| nbody                     | 87.8 ms                                                                | 73.5 ms: 1.19x faster                                                            |
| deltablue                 | 3.31 ms                                                                | 2.78 ms: 1.19x faster                                                            |
| float                     | 71.2 ms                                                                | 60.5 ms: 1.18x faster                                                            |
| logging_silent            | 102 ns                                                                 | 86.7 ns: 1.17x faster                                                            |
| deepcopy_memo             | 26.9 us                                                                | 23.7 us: 1.13x faster                                                            |
| spectral_norm             | 95.9 ms                                                                | 87.0 ms: 1.10x faster                                                            |
| scimark_sor               | 107 ms                                                                 | 97.2 ms: 1.10x faster                                                            |
| scimark_monte_carlo       | 61.5 ms                                                                | 56.5 ms: 1.09x faster                                                            |
| regex_effbot              | 2.72 ms                                                                | 2.55 ms: 1.06x faster                                                            |
| regex_dna                 | 178 ms                                                                 | 168 ms: 1.06x faster                                                             |
| pyflate                   | 400 ms                                                                 | 381 ms: 1.05x faster                                                             |
| scimark_lu                | 108 ms                                                                 | 103 ms: 1.05x faster                                                             |
| chaos                     | 56.0 ms                                                                | 53.7 ms: 1.04x faster                                                            |
| pickle_pure_python        | 306 us                                                                 | 296 us: 1.04x faster                                                             |
| pidigits                  | 200 ms                                                                 | 194 ms: 1.03x faster                                                             |
| json                      | 5.02 ms                                                                | 4.89 ms: 1.03x faster                                                            |
| logging_format            | 6.56 us                                                                | 6.45 us: 1.02x faster                                                            |
| crypto_pyaes              | 67.9 ms                                                                | 67.0 ms: 1.01x faster                                                            |
| async_tree_cpu_io_mixed   | 496 ms                                                                 | 490 ms: 1.01x faster                                                             |
| pathlib                   | 17.8 ms                                                                | 17.6 ms: 1.01x faster                                                            |
| sqlite_synth              | 2.21 us                                                                | 2.19 us: 1.01x faster                                                            |
| k_core                    | 1.87 sec                                                               | 1.86 sec: 1.01x faster                                                           |
| json_dumps                | 9.55 ms                                                                | 9.48 ms: 1.01x faster                                                            |
| connected_components      | 390 ms                                                                 | 387 ms: 1.01x faster                                                             |
| xml_etree_iterparse       | 84.3 ms                                                                | 83.7 ms: 1.01x faster                                                            |
| scimark_sparse_mat_mult   | 4.27 ms                                                                | 4.27 ms: 1.00x slower                                                            |
| async_tree_memoization_tg | 308 ms                                                                 | 309 ms: 1.01x slower                                                             |
| python_startup_no_site    | 7.23 ms                                                                | 7.28 ms: 1.01x slower                                                            |
| bench_mp_pool             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                            |
| python_startup            | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                            |
| subparsers                | 44.9 ms                                                                | 45.3 ms: 1.01x slower                                                            |
| shortest_path             | 434 ms                                                                 | 438 ms: 1.01x slower                                                             |
| coverage                  | 82.0 ms                                                                | 82.8 ms: 1.01x slower                                                            |
| django_template           | 34.3 ms                                                                | 34.7 ms: 1.01x slower                                                            |
| bench_thread_pool         | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                            |
| meteor_contest            | 99.6 ms                                                                | 101 ms: 1.01x slower                                                             |
| coroutines                | 23.8 ms                                                                | 24.1 ms: 1.01x slower                                                            |
| gc_traversal              | 4.30 ms                                                                | 4.35 ms: 1.01x slower                                                            |
| async_tree_io_tg          | 594 ms                                                                 | 603 ms: 1.01x slower                                                             |
| scimark_fft               | 257 ms                                                                 | 261 ms: 1.02x slower                                                             |
| mako                      | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                            |
| tomli_loads               | 1.77 sec                                                               | 1.80 sec: 1.02x slower                                                           |
| typing_runtime_protocols  | 156 us                                                                 | 160 us: 1.02x slower                                                             |
| pprint_safe_repr          | 682 ms                                                                 | 696 ms: 1.02x slower                                                             |
| bpe_tokeniser             | 3.96 sec                                                               | 4.05 sec: 1.02x slower                                                           |
| regex_compile             | 124 ms                                                                 | 127 ms: 1.02x slower                                                             |
| create_gc_cycles          | 1.92 ms                                                                | 1.96 ms: 1.02x slower                                                            |
| generators                | 27.7 ms                                                                | 28.4 ms: 1.03x slower                                                            |
| sympy_expand              | 491 ms                                                                 | 504 ms: 1.03x slower                                                             |
| telco                     | 156 ms                                                                 | 160 ms: 1.03x slower                                                             |
| async_generators          | 361 ms                                                                 | 371 ms: 1.03x slower                                                             |
| xml_etree_process         | 53.9 ms                                                                | 55.4 ms: 1.03x slower                                                            |
| deepcopy_reduce           | 2.59 us                                                                | 2.68 us: 1.03x slower                                                            |
| deepcopy                  | 244 us                                                                 | 253 us: 1.03x slower                                                             |
| comprehensions            | 15.8 us                                                                | 16.4 us: 1.04x slower                                                            |
| thrift                    | 742 us                                                                 | 771 us: 1.04x slower                                                             |
| genshi_text               | 20.4 ms                                                                | 21.3 ms: 1.04x slower                                                            |
| dulwich_log               | 69.2 ms                                                                | 72.3 ms: 1.04x slower                                                            |
| pycparser                 | 1.09 sec                                                               | 1.14 sec: 1.05x slower                                                           |
| xml_etree_generate        | 77.2 ms                                                                | 81.0 ms: 1.05x slower                                                            |
| many_optionals            | 1.25 ms                                                                | 1.31 ms: 1.05x slower                                                            |
| sqlglot_v2_optimize       | 51.3 ms                                                                | 53.8 ms: 1.05x slower                                                            |
| sympy_integrate           | 19.3 ms                                                                | 20.3 ms: 1.05x slower                                                            |
| sqlglot_v2_normalize      | 102 ms                                                                 | 108 ms: 1.06x slower                                                             |
| raytrace                  | 252 ms                                                                 | 269 ms: 1.07x slower                                                             |
| sympy_sum                 | 156 ms                                                                 | 169 ms: 1.09x slower                                                             |
| go                        | 105 ms                                                                 | 115 ms: 1.09x slower                                                             |
| sympy_str                 | 281 ms                                                                 | 307 ms: 1.09x slower                                                             |
| hexiom                    | 5.81 ms                                                                | 6.38 ms: 1.10x slower                                                            |
| html5lib                  | 60.6 ms                                                                | 67.2 ms: 1.11x slower                                                            |
| nqueens                   | 78.6 ms                                                                | 87.6 ms: 1.11x slower                                                            |
| genshi_xml                | 47.8 ms                                                                | 54.0 ms: 1.13x slower                                                            |
| mdp                       | 1.16 sec                                                               | 1.35 sec: 1.16x slower                                                           |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (16): async_tree_cpu_io_mixed_tg, asyncio_websockets, sqlglot_v2_parse, 2to3, fannkuch, regex_v8, xml_etree_parse, sqlglot_v2_transpile, logging_simple, json_loads, unpickle_pure_python, async_tree_none_tg, async_tree_memoization, pprint_pformat, async_tree_io, async_tree_none
Ignored benchmarks (3) of results/bm-20251027-3.15.0a1+-a716091-JIT/bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091.json: docutils, pylint, sphinx

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 99.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x