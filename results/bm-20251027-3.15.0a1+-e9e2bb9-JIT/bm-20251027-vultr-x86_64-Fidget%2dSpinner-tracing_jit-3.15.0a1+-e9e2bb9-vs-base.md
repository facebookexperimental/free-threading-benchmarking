# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: e9e2bb9
- commit date: 2025-10-27
- overall geometric mean: 1.007x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 251 ms: 1.00x faster                                                    |
| docutils       | 2.59 sec                                                               | 2.80 sec: 1.08x slower                                                  |
| html5lib       | 60.6 ms                                                                | 69.0 ms: 1.14x slower                                                   |
| sphinx         | 977 ms                                                                 | 1.04 sec: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators          | 361 ms                                                                 | 364 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 308 ms                                                                 | 311 ms: 1.01x slower                                                    |
| coroutines                | 23.8 ms                                                                | 24.5 ms: 1.03x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_memoization, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.2 ms                                                                | 60.6 ms: 1.18x faster                                                   |
| nbody          | 87.8 ms                                                                | 84.1 ms: 1.04x faster                                                   |
| pidigits       | 200 ms                                                                 | 198 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 2.72 ms                                                                | 2.78 ms: 1.02x slower                                                   |
| regex_v8       | 21.9 ms                                                                | 22.6 ms: 1.03x slower                                                   |
| regex_compile  | 124 ms                                                                 | 128 ms: 1.03x slower                                                    |
| regex_dna      | 178 ms                                                                 | 185 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.55 ms                                                                | 9.42 ms: 1.01x faster                                                   |
| xml_etree_iterparse  | 84.3 ms                                                                | 83.4 ms: 1.01x faster                                                   |
| unpickle_pure_python | 183 us                                                                 | 186 us: 1.02x slower                                                    |
| xml_etree_generate   | 77.2 ms                                                                | 80.1 ms: 1.04x slower                                                   |
| xml_etree_process    | 53.9 ms                                                                | 56.6 ms: 1.05x slower                                                   |
| tomli_loads          | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.23 ms                                                                | 7.24 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| genshi_text     | 20.4 ms                                                                | 21.2 ms: 1.04x slower                                                   |
| genshi_xml      | 47.8 ms                                                                | 54.4 ms: 1.14x slower                                                   |
| django_template | 34.3 ms                                                                | 39.6 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20251027-vultr-x86_64-python-a7160912274003672dc1-3.15.0a1+-a716091 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                  | 41.1 ms                                                                | 21.2 ms: 1.94x faster                                                   |
| richards_super            | 47.0 ms                                                                | 25.8 ms: 1.82x faster                                                   |
| float                     | 71.2 ms                                                                | 60.6 ms: 1.18x faster                                                   |
| logging_silent            | 102 ns                                                                 | 88.3 ns: 1.15x faster                                                   |
| deepcopy_memo             | 26.9 us                                                                | 23.4 us: 1.15x faster                                                   |
| deltablue                 | 3.31 ms                                                                | 2.89 ms: 1.15x faster                                                   |
| spectral_norm             | 95.9 ms                                                                | 84.0 ms: 1.14x faster                                                   |
| scimark_sor               | 107 ms                                                                 | 99.8 ms: 1.07x faster                                                   |
| scimark_monte_carlo       | 61.5 ms                                                                | 57.8 ms: 1.06x faster                                                   |
| scimark_lu                | 108 ms                                                                 | 102 ms: 1.06x faster                                                    |
| nbody                     | 87.8 ms                                                                | 84.1 ms: 1.04x faster                                                   |
| pyflate                   | 400 ms                                                                 | 387 ms: 1.03x faster                                                    |
| json                      | 5.02 ms                                                                | 4.88 ms: 1.03x faster                                                   |
| chaos                     | 56.0 ms                                                                | 54.8 ms: 1.02x faster                                                   |
| crypto_pyaes              | 67.9 ms                                                                | 66.9 ms: 1.02x faster                                                   |
| json_dumps                | 9.55 ms                                                                | 9.42 ms: 1.01x faster                                                   |
| mako                      | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| pidigits                  | 200 ms                                                                 | 198 ms: 1.01x faster                                                    |
| sqlite_synth              | 2.21 us                                                                | 2.19 us: 1.01x faster                                                   |
| xml_etree_iterparse       | 84.3 ms                                                                | 83.4 ms: 1.01x faster                                                   |
| 2to3                      | 253 ms                                                                 | 251 ms: 1.00x faster                                                    |
| scimark_sparse_mat_mult   | 4.27 ms                                                                | 4.25 ms: 1.00x faster                                                   |
| python_startup_no_site    | 7.23 ms                                                                | 7.24 ms: 1.00x slower                                                   |
| coverage                  | 82.0 ms                                                                | 82.3 ms: 1.00x slower                                                   |
| python_startup            | 12.4 ms                                                                | 12.4 ms: 1.00x slower                                                   |
| bench_thread_pool         | 1.01 ms                                                                | 1.01 ms: 1.01x slower                                                   |
| bench_mp_pool             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| async_generators          | 361 ms                                                                 | 364 ms: 1.01x slower                                                    |
| connected_components      | 390 ms                                                                 | 394 ms: 1.01x slower                                                    |
| scimark_fft               | 257 ms                                                                 | 260 ms: 1.01x slower                                                    |
| async_tree_memoization_tg | 308 ms                                                                 | 311 ms: 1.01x slower                                                    |
| comprehensions            | 15.8 us                                                                | 16.1 us: 1.01x slower                                                   |
| unpickle_pure_python      | 183 us                                                                 | 186 us: 1.02x slower                                                    |
| meteor_contest            | 99.6 ms                                                                | 102 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile      | 1.51 ms                                                                | 1.54 ms: 1.02x slower                                                   |
| bpe_tokeniser             | 3.96 sec                                                               | 4.06 sec: 1.02x slower                                                  |
| generators                | 27.7 ms                                                                | 28.3 ms: 1.02x slower                                                   |
| regex_effbot              | 2.72 ms                                                                | 2.78 ms: 1.02x slower                                                   |
| sqlglot_v2_parse          | 1.20 ms                                                                | 1.23 ms: 1.03x slower                                                   |
| typing_runtime_protocols  | 156 us                                                                 | 160 us: 1.03x slower                                                    |
| coroutines                | 23.8 ms                                                                | 24.5 ms: 1.03x slower                                                   |
| fannkuch                  | 362 ms                                                                 | 373 ms: 1.03x slower                                                    |
| regex_v8                  | 21.9 ms                                                                | 22.6 ms: 1.03x slower                                                   |
| regex_compile             | 124 ms                                                                 | 128 ms: 1.03x slower                                                    |
| genshi_text               | 20.4 ms                                                                | 21.2 ms: 1.04x slower                                                   |
| xml_etree_generate        | 77.2 ms                                                                | 80.1 ms: 1.04x slower                                                   |
| logging_format            | 6.56 us                                                                | 6.81 us: 1.04x slower                                                   |
| regex_dna                 | 178 ms                                                                 | 185 ms: 1.04x slower                                                    |
| subparsers                | 44.9 ms                                                                | 46.8 ms: 1.04x slower                                                   |
| pprint_pformat            | 1.41 sec                                                               | 1.47 sec: 1.04x slower                                                  |
| thrift                    | 742 us                                                                 | 777 us: 1.05x slower                                                    |
| xml_etree_process         | 53.9 ms                                                                | 56.6 ms: 1.05x slower                                                   |
| deepcopy                  | 244 us                                                                 | 257 us: 1.05x slower                                                    |
| telco                     | 156 ms                                                                 | 164 ms: 1.05x slower                                                    |
| tomli_loads               | 1.77 sec                                                               | 1.86 sec: 1.05x slower                                                  |
| many_optionals            | 1.25 ms                                                                | 1.32 ms: 1.05x slower                                                   |
| sympy_integrate           | 19.3 ms                                                                | 20.5 ms: 1.06x slower                                                   |
| sphinx                    | 977 ms                                                                 | 1.04 sec: 1.06x slower                                                  |
| sympy_expand              | 491 ms                                                                 | 522 ms: 1.06x slower                                                    |
| dulwich_log               | 69.2 ms                                                                | 73.7 ms: 1.06x slower                                                   |
| logging_simple            | 5.75 us                                                                | 6.13 us: 1.07x slower                                                   |
| pathlib                   | 17.8 ms                                                                | 19.1 ms: 1.07x slower                                                   |
| pycparser                 | 1.09 sec                                                               | 1.17 sec: 1.07x slower                                                  |
| docutils                  | 2.59 sec                                                               | 2.80 sec: 1.08x slower                                                  |
| sqlglot_v2_optimize       | 51.3 ms                                                                | 55.9 ms: 1.09x slower                                                   |
| sympy_sum                 | 156 ms                                                                 | 170 ms: 1.09x slower                                                    |
| pylint                    | 289 ms                                                                 | 318 ms: 1.10x slower                                                    |
| hexiom                    | 5.81 ms                                                                | 6.40 ms: 1.10x slower                                                   |
| sympy_str                 | 281 ms                                                                 | 310 ms: 1.10x slower                                                    |
| nqueens                   | 78.6 ms                                                                | 87.3 ms: 1.11x slower                                                   |
| go                        | 105 ms                                                                 | 117 ms: 1.11x slower                                                    |
| gc_traversal              | 4.30 ms                                                                | 4.78 ms: 1.11x slower                                                   |
| raytrace                  | 252 ms                                                                 | 281 ms: 1.11x slower                                                    |
| genshi_xml                | 47.8 ms                                                                | 54.4 ms: 1.14x slower                                                   |
| html5lib                  | 60.6 ms                                                                | 69.0 ms: 1.14x slower                                                   |
| sqlglot_v2_normalize      | 102 ms                                                                 | 117 ms: 1.15x slower                                                    |
| mdp                       | 1.16 sec                                                               | 1.33 sec: 1.15x slower                                                  |
| django_template           | 34.3 ms                                                                | 39.6 ms: 1.15x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (16): pickle_pure_python, async_tree_cpu_io_mixed, k_core, async_tree_cpu_io_mixed_tg, asyncio_websockets, xml_etree_parse, json_loads, create_gc_cycles, async_tree_memoization, async_tree_io, shortest_path, deepcopy_reduce, async_tree_io_tg, async_tree_none, async_tree_none_tg, pprint_safe_repr

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x