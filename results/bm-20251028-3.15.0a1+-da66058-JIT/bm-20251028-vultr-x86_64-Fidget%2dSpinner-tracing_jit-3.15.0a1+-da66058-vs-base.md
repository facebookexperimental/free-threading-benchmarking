# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: da66058
- commit date: 2025-10-28
- overall geometric mean: 1.006x faster
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 253 ms: 1.00x slower                                                    |
| docutils       | 2.59 sec                                                               | 2.75 sec: 1.06x slower                                                  |
| html5lib       | 60.6 ms                                                                | 68.9 ms: 1.14x slower                                                   |
| sphinx         | 977 ms                                                                 | 1.03 sec: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 496 ms                                                                 | 486 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 482 ms: 1.02x faster                                                    |
| coroutines                 | 23.8 ms                                                                | 24.0 ms: 1.00x slower                                                   |
| async_generators           | 361 ms                                                                 | 363 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (7): async_tree_io_tg, asyncio_websockets, async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.2 ms                                                                | 60.0 ms: 1.19x faster                                                   |
| pidigits       | 200 ms                                                                 | 195 ms: 1.02x faster                                                    |
| nbody          | 87.8 ms                                                                | 86.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 178 ms                                                                 | 179 ms: 1.01x slower                                                    |
| regex_v8       | 21.9 ms                                                                | 22.3 ms: 1.02x slower                                                   |
| regex_compile  | 124 ms                                                                 | 127 ms: 1.03x slower                                                    |
| regex_effbot   | 2.72 ms                                                                | 2.80 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 306 us                                                                 | 299 us: 1.02x faster                                                    |
| xml_etree_iterparse  | 84.3 ms                                                                | 83.1 ms: 1.01x faster                                                   |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                    |
| unpickle_pure_python | 183 us                                                                 | 184 us: 1.01x slower                                                    |
| xml_etree_process    | 53.9 ms                                                                | 55.2 ms: 1.03x slower                                                   |
| xml_etree_generate   | 77.2 ms                                                                | 79.9 ms: 1.03x slower                                                   |
| tomli_loads          | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.23 ms                                                                | 7.26 ms: 1.01x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                   |
| genshi_text    | 20.4 ms                                                                | 21.1 ms: 1.03x slower                                                   |
| genshi_xml     | 47.8 ms                                                                | 53.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251028-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-da66058 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 41.1 ms                                                                | 21.2 ms: 1.94x faster                                                   |
| richards_super             | 47.0 ms                                                                | 25.4 ms: 1.85x faster                                                   |
| float                      | 71.2 ms                                                                | 60.0 ms: 1.19x faster                                                   |
| deltablue                  | 3.31 ms                                                                | 2.84 ms: 1.17x faster                                                   |
| logging_silent             | 102 ns                                                                 | 88.1 ns: 1.15x faster                                                   |
| deepcopy_memo              | 26.9 us                                                                | 23.3 us: 1.15x faster                                                   |
| spectral_norm              | 95.9 ms                                                                | 84.0 ms: 1.14x faster                                                   |
| scimark_sor                | 107 ms                                                                 | 96.7 ms: 1.11x faster                                                   |
| scimark_monte_carlo        | 61.5 ms                                                                | 57.3 ms: 1.07x faster                                                   |
| pyflate                    | 400 ms                                                                 | 381 ms: 1.05x faster                                                    |
| chaos                      | 56.0 ms                                                                | 53.6 ms: 1.05x faster                                                   |
| scimark_lu                 | 108 ms                                                                 | 104 ms: 1.04x faster                                                    |
| crypto_pyaes               | 67.9 ms                                                                | 66.1 ms: 1.03x faster                                                   |
| pickle_pure_python         | 306 us                                                                 | 299 us: 1.02x faster                                                    |
| pidigits                   | 200 ms                                                                 | 195 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.59 us                                                                | 2.54 us: 1.02x faster                                                   |
| async_tree_cpu_io_mixed    | 496 ms                                                                 | 486 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 492 ms                                                                 | 482 ms: 1.02x faster                                                    |
| nbody                      | 87.8 ms                                                                | 86.5 ms: 1.02x faster                                                   |
| json                       | 5.02 ms                                                                | 4.94 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 84.3 ms                                                                | 83.1 ms: 1.01x faster                                                   |
| scimark_fft                | 257 ms                                                                 | 253 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult    | 4.27 ms                                                                | 4.23 ms: 1.01x faster                                                   |
| coverage                   | 82.0 ms                                                                | 81.5 ms: 1.01x faster                                                   |
| 2to3                       | 253 ms                                                                 | 253 ms: 1.00x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 24.0 ms: 1.00x slower                                                   |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.23 ms                                                                | 7.26 ms: 1.01x slower                                                   |
| async_generators           | 361 ms                                                                 | 363 ms: 1.01x slower                                                    |
| bench_thread_pool          | 1.01 ms                                                                | 1.01 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 183 us                                                                 | 184 us: 1.01x slower                                                    |
| mako                       | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                   |
| sqlglot_v2_parse           | 1.20 ms                                                                | 1.21 ms: 1.01x slower                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.52 ms: 1.01x slower                                                   |
| regex_dna                  | 178 ms                                                                 | 179 ms: 1.01x slower                                                    |
| shortest_path              | 434 ms                                                                 | 438 ms: 1.01x slower                                                    |
| bench_mp_pool              | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| meteor_contest             | 99.6 ms                                                                | 101 ms: 1.01x slower                                                    |
| python_startup             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| comprehensions             | 15.8 us                                                                | 16.1 us: 1.01x slower                                                   |
| typing_runtime_protocols   | 156 us                                                                 | 159 us: 1.02x slower                                                    |
| subparsers                 | 44.9 ms                                                                | 45.7 ms: 1.02x slower                                                   |
| regex_v8                   | 21.9 ms                                                                | 22.3 ms: 1.02x slower                                                   |
| bpe_tokeniser              | 3.96 sec                                                               | 4.04 sec: 1.02x slower                                                  |
| gc_traversal               | 4.30 ms                                                                | 4.40 ms: 1.02x slower                                                   |
| pprint_safe_repr           | 682 ms                                                                 | 698 ms: 1.02x slower                                                    |
| xml_etree_process          | 53.9 ms                                                                | 55.2 ms: 1.03x slower                                                   |
| generators                 | 27.7 ms                                                                | 28.4 ms: 1.03x slower                                                   |
| regex_compile              | 124 ms                                                                 | 127 ms: 1.03x slower                                                    |
| regex_effbot               | 2.72 ms                                                                | 2.80 ms: 1.03x slower                                                   |
| xml_etree_generate         | 77.2 ms                                                                | 79.9 ms: 1.03x slower                                                   |
| genshi_text                | 20.4 ms                                                                | 21.1 ms: 1.03x slower                                                   |
| sympy_expand               | 491 ms                                                                 | 509 ms: 1.04x slower                                                    |
| sqlglot_v2_optimize        | 51.3 ms                                                                | 53.2 ms: 1.04x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 106 ms: 1.04x slower                                                    |
| telco                      | 156 ms                                                                 | 163 ms: 1.04x slower                                                    |
| dulwich_log                | 69.2 ms                                                                | 72.6 ms: 1.05x slower                                                   |
| sympy_integrate            | 19.3 ms                                                                | 20.3 ms: 1.05x slower                                                   |
| many_optionals             | 1.25 ms                                                                | 1.31 ms: 1.05x slower                                                   |
| sphinx                     | 977 ms                                                                 | 1.03 sec: 1.05x slower                                                  |
| tomli_loads                | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| thrift                     | 742 us                                                                 | 787 us: 1.06x slower                                                    |
| pycparser                  | 1.09 sec                                                               | 1.16 sec: 1.06x slower                                                  |
| docutils                   | 2.59 sec                                                               | 2.75 sec: 1.06x slower                                                  |
| raytrace                   | 252 ms                                                                 | 272 ms: 1.08x slower                                                    |
| hexiom                     | 5.81 ms                                                                | 6.27 ms: 1.08x slower                                                   |
| pylint                     | 289 ms                                                                 | 313 ms: 1.08x slower                                                    |
| sympy_sum                  | 156 ms                                                                 | 169 ms: 1.09x slower                                                    |
| sympy_str                  | 281 ms                                                                 | 308 ms: 1.09x slower                                                    |
| nqueens                    | 78.6 ms                                                                | 86.3 ms: 1.10x slower                                                   |
| go                         | 105 ms                                                                 | 116 ms: 1.10x slower                                                    |
| genshi_xml                 | 47.8 ms                                                                | 53.7 ms: 1.12x slower                                                   |
| html5lib                   | 60.6 ms                                                                | 68.9 ms: 1.14x slower                                                   |
| mdp                        | 1.16 sec                                                               | 1.33 sec: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (20): pprint_pformat, logging_format, sqlite_synth, pathlib, json_dumps, async_tree_io_tg, asyncio_websockets, async_tree_io, k_core, json_loads, create_gc_cycles, async_tree_memoization_tg, logging_simple, fannkuch, deepcopy, async_tree_memoization, connected_components, django_template, async_tree_none_tg, async_tree_none

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x