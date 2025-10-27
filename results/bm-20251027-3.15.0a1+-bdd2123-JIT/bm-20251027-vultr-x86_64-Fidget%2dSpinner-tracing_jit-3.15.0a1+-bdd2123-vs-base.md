# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: bdd2123
- commit date: 2025-10-27
- overall geometric mean: 1.003x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.60 sec                                                               | 2.70 sec: 1.04x slower                                                  |
| html5lib       | 60.7 ms                                                                | 70.0 ms: 1.15x slower                                                   |
| sphinx         | 989 ms                                                                 | 1.01 sec: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| async_generators           | 367 ms                                                                 | 375 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 311 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_io              | 552 ms                                                                 | 563 ms: 1.02x slower                                                    |
| async_tree_none            | 243 ms                                                                 | 250 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 494 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 493 ms: 1.03x slower                                                    |
| async_tree_memoization     | 304 ms                                                                 | 313 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.9 ms                                                                | 62.3 ms: 1.15x faster                                                   |
| nbody          | 92.6 ms                                                                | 90.5 ms: 1.02x faster                                                   |
| pidigits       | 194 ms                                                                 | 204 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 176 ms: 1.06x faster                                                    |
| regex_v8       | 23.1 ms                                                                | 22.1 ms: 1.04x faster                                                   |
| regex_effbot   | 2.86 ms                                                                | 2.79 ms: 1.02x faster                                                   |
| regex_compile  | 124 ms                                                                 | 130 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 309 us                                                                 | 299 us: 1.04x faster                                                    |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                    |
| unpickle_pure_python | 183 us                                                                 | 186 us: 1.02x slower                                                    |
| xml_etree_generate   | 77.1 ms                                                                | 80.6 ms: 1.05x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 57.0 ms: 1.06x slower                                                   |
| tomli_loads          | 1.72 sec                                                               | 1.83 sec: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.25 ms                                                                | 7.27 ms: 1.00x slower                                                   |
| python_startup         | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                   |
| genshi_text     | 20.8 ms                                                                | 21.5 ms: 1.04x slower                                                   |
| django_template | 34.5 ms                                                                | 38.8 ms: 1.13x slower                                                   |
| genshi_xml      | 49.7 ms                                                                | 56.2 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251024-vultr-x86_64-python-92c0c45563bdc041b208-3.15.0a1+-92c0c45 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 40.8 ms                                                                | 20.8 ms: 1.97x faster                                                   |
| richards_super             | 46.7 ms                                                                | 25.2 ms: 1.86x faster                                                   |
| spectral_norm              | 99.1 ms                                                                | 84.8 ms: 1.17x faster                                                   |
| logging_silent             | 101 ns                                                                 | 86.8 ns: 1.17x faster                                                   |
| float                      | 71.9 ms                                                                | 62.3 ms: 1.15x faster                                                   |
| deltablue                  | 3.28 ms                                                                | 2.84 ms: 1.15x faster                                                   |
| deepcopy_memo              | 26.8 us                                                                | 23.3 us: 1.15x faster                                                   |
| scimark_sor                | 109 ms                                                                 | 97.0 ms: 1.13x faster                                                   |
| scimark_lu                 | 111 ms                                                                 | 103 ms: 1.08x faster                                                    |
| scimark_monte_carlo        | 61.8 ms                                                                | 57.9 ms: 1.07x faster                                                   |
| regex_dna                  | 187 ms                                                                 | 176 ms: 1.06x faster                                                    |
| regex_v8                   | 23.1 ms                                                                | 22.1 ms: 1.04x faster                                                   |
| chaos                      | 56.5 ms                                                                | 54.3 ms: 1.04x faster                                                   |
| pickle_pure_python         | 309 us                                                                 | 299 us: 1.04x faster                                                    |
| regex_effbot               | 2.86 ms                                                                | 2.79 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 4.22 ms: 1.02x faster                                                   |
| nbody                      | 92.6 ms                                                                | 90.5 ms: 1.02x faster                                                   |
| pyflate                    | 401 ms                                                                 | 393 ms: 1.02x faster                                                    |
| json                       | 5.03 ms                                                                | 4.93 ms: 1.02x faster                                                   |
| deepcopy_reduce            | 2.66 us                                                                | 2.61 us: 1.02x faster                                                   |
| crypto_pyaes               | 68.6 ms                                                                | 67.9 ms: 1.01x faster                                                   |
| coverage                   | 82.3 ms                                                                | 81.5 ms: 1.01x faster                                                   |
| create_gc_cycles           | 1.95 ms                                                                | 1.93 ms: 1.01x faster                                                   |
| comprehensions             | 16.3 us                                                                | 16.1 us: 1.01x faster                                                   |
| k_core                     | 1.88 sec                                                               | 1.87 sec: 1.01x faster                                                  |
| scimark_fft                | 262 ms                                                                 | 260 ms: 1.01x faster                                                    |
| python_startup_no_site     | 7.25 ms                                                                | 7.27 ms: 1.00x slower                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.22 ms: 1.01x slower                                                   |
| fannkuch                   | 367 ms                                                                 | 370 ms: 1.01x slower                                                    |
| bench_thread_pool          | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                    |
| python_startup             | 12.4 ms                                                                | 12.5 ms: 1.01x slower                                                   |
| generators                 | 28.0 ms                                                                | 28.3 ms: 1.01x slower                                                   |
| bpe_tokeniser              | 4.01 sec                                                               | 4.06 sec: 1.01x slower                                                  |
| bench_mp_pool              | 12.5 ms                                                                | 12.6 ms: 1.01x slower                                                   |
| async_tree_io_tg           | 591 ms                                                                 | 599 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 183 us                                                                 | 186 us: 1.02x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.54 ms: 1.02x slower                                                   |
| async_generators           | 367 ms                                                                 | 375 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.19 us                                                                | 2.23 us: 1.02x slower                                                   |
| async_tree_memoization_tg  | 305 ms                                                                 | 311 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 243 ms                                                                 | 248 ms: 1.02x slower                                                    |
| async_tree_io              | 552 ms                                                                 | 563 ms: 1.02x slower                                                    |
| pprint_pformat             | 1.41 sec                                                               | 1.45 sec: 1.02x slower                                                  |
| mako                       | 10.5 ms                                                                | 10.8 ms: 1.02x slower                                                   |
| sphinx                     | 989 ms                                                                 | 1.01 sec: 1.02x slower                                                  |
| async_tree_none            | 243 ms                                                                 | 250 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed    | 480 ms                                                                 | 494 ms: 1.03x slower                                                    |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 493 ms: 1.03x slower                                                    |
| telco                      | 158 ms                                                                 | 163 ms: 1.03x slower                                                    |
| async_tree_memoization     | 304 ms                                                                 | 313 ms: 1.03x slower                                                    |
| deepcopy                   | 249 us                                                                 | 257 us: 1.03x slower                                                    |
| genshi_text                | 20.8 ms                                                                | 21.5 ms: 1.04x slower                                                   |
| docutils                   | 2.60 sec                                                               | 2.70 sec: 1.04x slower                                                  |
| xml_etree_generate         | 77.1 ms                                                                | 80.6 ms: 1.05x slower                                                   |
| regex_compile              | 124 ms                                                                 | 130 ms: 1.05x slower                                                    |
| sympy_integrate            | 19.3 ms                                                                | 20.3 ms: 1.05x slower                                                   |
| pidigits                   | 194 ms                                                                 | 204 ms: 1.05x slower                                                    |
| logging_simple             | 5.78 us                                                                | 6.13 us: 1.06x slower                                                   |
| xml_etree_process          | 53.7 ms                                                                | 57.0 ms: 1.06x slower                                                   |
| tomli_loads                | 1.72 sec                                                               | 1.83 sec: 1.06x slower                                                  |
| pylint                     | 292 ms                                                                 | 311 ms: 1.06x slower                                                    |
| subparsers                 | 44.7 ms                                                                | 47.6 ms: 1.06x slower                                                   |
| sympy_sum                  | 157 ms                                                                 | 168 ms: 1.07x slower                                                    |
| many_optionals             | 1.25 ms                                                                | 1.34 ms: 1.07x slower                                                   |
| sympy_expand               | 489 ms                                                                 | 523 ms: 1.07x slower                                                    |
| logging_format             | 6.59 us                                                                | 7.05 us: 1.07x slower                                                   |
| thrift                     | 742 us                                                                 | 794 us: 1.07x slower                                                    |
| hexiom                     | 5.88 ms                                                                | 6.31 ms: 1.07x slower                                                   |
| pathlib                    | 17.6 ms                                                                | 19.0 ms: 1.08x slower                                                   |
| dulwich_log                | 68.5 ms                                                                | 73.8 ms: 1.08x slower                                                   |
| sympy_str                  | 282 ms                                                                 | 304 ms: 1.08x slower                                                    |
| mdp                        | 1.17 sec                                                               | 1.27 sec: 1.08x slower                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 56.1 ms: 1.09x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.17 sec: 1.09x slower                                                  |
| go                         | 107 ms                                                                 | 116 ms: 1.09x slower                                                    |
| raytrace                   | 251 ms                                                                 | 278 ms: 1.11x slower                                                    |
| nqueens                    | 79.2 ms                                                                | 88.0 ms: 1.11x slower                                                   |
| django_template            | 34.5 ms                                                                | 38.8 ms: 1.13x slower                                                   |
| gc_traversal               | 4.32 ms                                                                | 4.88 ms: 1.13x slower                                                   |
| genshi_xml                 | 49.7 ms                                                                | 56.2 ms: 1.13x slower                                                   |
| sqlglot_v2_normalize       | 102 ms                                                                 | 116 ms: 1.14x slower                                                    |
| html5lib                   | 60.7 ms                                                                | 70.0 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (11): pprint_safe_repr, json_loads, xml_etree_iterparse, shortest_path, connected_components, json_dumps, asyncio_websockets, 2to3, coroutines, meteor_contest, typing_runtime_protocols

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x