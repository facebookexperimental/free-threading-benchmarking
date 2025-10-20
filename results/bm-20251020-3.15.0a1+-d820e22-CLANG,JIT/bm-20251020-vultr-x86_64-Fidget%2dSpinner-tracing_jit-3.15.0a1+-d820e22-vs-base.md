# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d820e22
- commit date: 2025-10-20
- overall geometric mean: 1.029x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 250 ms: 1.01x slower                                                    |
| docutils       | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| html5lib       | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                   |
| sphinx         | 974 ms                                                                 | 993 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 22.0 ms                                                                | 22.1 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 475 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 473 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.01x slower                                                    |
| async_tree_none            | 254 ms                                                                 | 259 ms: 1.02x slower                                                    |
| async_tree_io              | 582 ms                                                                 | 594 ms: 1.02x slower                                                    |
| async_tree_memoization     | 298 ms                                                                 | 306 ms: 1.03x slower                                                    |
| async_generators           | 334 ms                                                                 | 487 ms: 1.46x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                            |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 68.8 ms                                                                | 61.8 ms: 1.11x faster                                                   |
| pidigits       | 192 ms                                                                 | 192 ms: 1.00x faster                                                    |
| nbody          | 94.3 ms                                                                | 96.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.10 ms                                                                | 3.05 ms: 1.02x faster                                                   |
| regex_dna      | 187 ms                                                                 | 185 ms: 1.01x faster                                                    |
| regex_v8       | 21.4 ms                                                                | 22.6 ms: 1.05x slower                                                   |
| regex_compile  | 122 ms                                                                 | 133 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.06 ms                                                                | 8.89 ms: 1.02x faster                                                   |
| xml_etree_iterparse  | 97.0 ms                                                                | 95.5 ms: 1.01x faster                                                   |
| unpickle_pure_python | 186 us                                                                 | 183 us: 1.01x faster                                                    |
| json_loads           | 25.9 us                                                                | 25.7 us: 1.01x faster                                                   |
| xml_etree_parse      | 148 ms                                                                 | 147 ms: 1.01x faster                                                    |
| xml_etree_process    | 51.1 ms                                                                | 52.2 ms: 1.02x slower                                                   |
| pickle_pure_python   | 293 us                                                                 | 305 us: 1.04x slower                                                    |
| tomli_loads          | 1.67 sec                                                               | 1.82 sec: 1.09x slower                                                  |
| xml_etree_generate   | 75.0 ms                                                                | 83.2 ms: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                | 12.7 ms: 1.01x faster                                                   |
| python_startup_no_site | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 47.0 ms                                                                | 51.8 ms: 1.10x slower                                                   |
| genshi_text     | 19.1 ms                                                                | 21.3 ms: 1.11x slower                                                   |
| django_template | 32.7 ms                                                                | 37.2 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.08x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d820e22 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 37.2 ms                                                                | 30.7 ms: 1.21x faster                                                   |
| richards_super             | 42.6 ms                                                                | 36.3 ms: 1.17x faster                                                   |
| float                      | 68.8 ms                                                                | 61.8 ms: 1.11x faster                                                   |
| pprint_safe_repr           | 713 ms                                                                 | 667 ms: 1.07x faster                                                    |
| deepcopy_memo              | 23.9 us                                                                | 22.4 us: 1.07x faster                                                   |
| logging_silent             | 84.0 ns                                                                | 80.0 ns: 1.05x faster                                                   |
| deltablue                  | 2.91 ms                                                                | 2.78 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 2.38 us                                                                | 2.32 us: 1.03x faster                                                   |
| crypto_pyaes               | 66.6 ms                                                                | 64.8 ms: 1.03x faster                                                   |
| json                       | 4.98 ms                                                                | 4.88 ms: 1.02x faster                                                   |
| json_dumps                 | 9.06 ms                                                                | 8.89 ms: 1.02x faster                                                   |
| regex_effbot               | 3.10 ms                                                                | 3.05 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 97.0 ms                                                                | 95.5 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 55.7 ms                                                                | 55.0 ms: 1.01x faster                                                   |
| telco                      | 156 ms                                                                 | 154 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 186 us                                                                 | 183 us: 1.01x faster                                                    |
| typing_runtime_protocols   | 148 us                                                                 | 146 us: 1.01x faster                                                    |
| json_loads                 | 25.9 us                                                                | 25.7 us: 1.01x faster                                                   |
| pyflate                    | 387 ms                                                                 | 384 ms: 1.01x faster                                                    |
| regex_dna                  | 187 ms                                                                 | 185 ms: 1.01x faster                                                    |
| xml_etree_parse            | 148 ms                                                                 | 147 ms: 1.01x faster                                                    |
| python_startup             | 12.7 ms                                                                | 12.7 ms: 1.01x faster                                                   |
| pidigits                   | 192 ms                                                                 | 192 ms: 1.00x faster                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| fannkuch                   | 355 ms                                                                 | 357 ms: 1.00x slower                                                    |
| coroutines                 | 22.0 ms                                                                | 22.1 ms: 1.01x slower                                                   |
| bench_thread_pool          | 962 us                                                                 | 968 us: 1.01x slower                                                    |
| 2to3                       | 249 ms                                                                 | 250 ms: 1.01x slower                                                    |
| coverage                   | 75.0 ms                                                                | 75.5 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 475 ms: 1.01x slower                                                    |
| gc_traversal               | 4.37 ms                                                                | 4.40 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 473 ms: 1.01x slower                                                    |
| meteor_contest             | 104 ms                                                                 | 105 ms: 1.01x slower                                                    |
| docutils                   | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.48 ms: 1.01x slower                                                   |
| scimark_fft                | 244 ms                                                                 | 247 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.01x slower                                                    |
| bpe_tokeniser              | 3.94 sec                                                               | 3.99 sec: 1.01x slower                                                  |
| many_optionals             | 1.25 ms                                                                | 1.26 ms: 1.01x slower                                                   |
| connected_components       | 402 ms                                                                 | 407 ms: 1.01x slower                                                    |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.19 ms: 1.01x slower                                                   |
| create_gc_cycles           | 2.00 ms                                                                | 2.03 ms: 1.02x slower                                                   |
| sympy_integrate            | 18.3 ms                                                                | 18.7 ms: 1.02x slower                                                   |
| shortest_path              | 439 ms                                                                 | 446 ms: 1.02x slower                                                    |
| async_tree_none            | 254 ms                                                                 | 259 ms: 1.02x slower                                                    |
| sphinx                     | 974 ms                                                                 | 993 ms: 1.02x slower                                                    |
| xml_etree_process          | 51.1 ms                                                                | 52.2 ms: 1.02x slower                                                   |
| async_tree_io              | 582 ms                                                                 | 594 ms: 1.02x slower                                                    |
| scimark_sor                | 98.7 ms                                                                | 101 ms: 1.02x slower                                                    |
| async_tree_memoization     | 298 ms                                                                 | 306 ms: 1.03x slower                                                    |
| nbody                      | 94.3 ms                                                                | 96.8 ms: 1.03x slower                                                   |
| sqlglot_v2_optimize        | 48.6 ms                                                                | 50.0 ms: 1.03x slower                                                   |
| sympy_sum                  | 149 ms                                                                 | 154 ms: 1.03x slower                                                    |
| nqueens                    | 74.4 ms                                                                | 77.0 ms: 1.04x slower                                                   |
| pycparser                  | 1.09 sec                                                               | 1.13 sec: 1.04x slower                                                  |
| sympy_str                  | 266 ms                                                                 | 277 ms: 1.04x slower                                                    |
| thrift                     | 698 us                                                                 | 726 us: 1.04x slower                                                    |
| pickle_pure_python         | 293 us                                                                 | 305 us: 1.04x slower                                                    |
| deepcopy                   | 219 us                                                                 | 228 us: 1.04x slower                                                    |
| sympy_expand               | 457 ms                                                                 | 479 ms: 1.05x slower                                                    |
| subparsers                 | 45.0 ms                                                                | 47.3 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult    | 3.89 ms                                                                | 4.09 ms: 1.05x slower                                                   |
| sqlglot_v2_normalize       | 96.6 ms                                                                | 102 ms: 1.05x slower                                                    |
| regex_v8                   | 21.4 ms                                                                | 22.6 ms: 1.05x slower                                                   |
| mdp                        | 1.10 sec                                                               | 1.17 sec: 1.06x slower                                                  |
| chaos                      | 50.3 ms                                                                | 53.4 ms: 1.06x slower                                                   |
| hexiom                     | 5.47 ms                                                                | 5.82 ms: 1.06x slower                                                   |
| tomli_loads                | 1.67 sec                                                               | 1.82 sec: 1.09x slower                                                  |
| regex_compile              | 122 ms                                                                 | 133 ms: 1.10x slower                                                    |
| genshi_xml                 | 47.0 ms                                                                | 51.8 ms: 1.10x slower                                                   |
| dulwich_log                | 67.9 ms                                                                | 75.0 ms: 1.11x slower                                                   |
| xml_etree_generate         | 75.0 ms                                                                | 83.2 ms: 1.11x slower                                                   |
| genshi_text                | 19.1 ms                                                                | 21.3 ms: 1.11x slower                                                   |
| logging_simple             | 5.57 us                                                                | 6.28 us: 1.13x slower                                                   |
| django_template            | 32.7 ms                                                                | 37.2 ms: 1.14x slower                                                   |
| logging_format             | 6.36 us                                                                | 7.24 us: 1.14x slower                                                   |
| raytrace                   | 233 ms                                                                 | 269 ms: 1.15x slower                                                    |
| go                         | 99.6 ms                                                                | 115 ms: 1.15x slower                                                    |
| html5lib                   | 59.2 ms                                                                | 68.6 ms: 1.16x slower                                                   |
| pathlib                    | 16.8 ms                                                                | 21.1 ms: 1.26x slower                                                   |
| async_generators           | 334 ms                                                                 | 487 ms: 1.46x slower                                                    |
| scimark_lu                 | 101 ms                                                                 | 160 ms: 1.59x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (12): mako, spectral_norm, k_core, comprehensions, bench_mp_pool, asyncio_websockets, generators, sqlite_synth, pprint_pformat, async_tree_memoization_tg, pylint, async_tree_io_tg

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x