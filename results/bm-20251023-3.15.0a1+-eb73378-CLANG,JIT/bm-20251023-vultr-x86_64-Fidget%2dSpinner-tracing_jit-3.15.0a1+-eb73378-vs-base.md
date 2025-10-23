# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: eb73378
- commit date: 2025-10-23
- overall geometric mean: 1.008x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 249 ms: 1.00x slower                                                    |
| docutils       | 2.54 sec                                                               | 2.65 sec: 1.05x slower                                                  |
| html5lib       | 59.0 ms                                                                | 63.9 ms: 1.08x slower                                                   |
| sphinx         | 964 ms                                                                 | 1.00 sec: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 471 ms                                                                 | 475 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 474 ms: 1.01x slower                                                    |
| async_tree_none            | 254 ms                                                                 | 258 ms: 1.02x slower                                                    |
| async_generators           | 330 ms                                                                 | 338 ms: 1.02x slower                                                    |
| async_tree_memoization     | 301 ms                                                                 | 308 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (5): asyncio_websockets, coroutines, async_tree_io_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.3 ms                                                                | 62.7 ms: 1.07x faster                                                   |
| nbody          | 87.6 ms                                                                | 83.3 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 191 ms: 1.05x slower                                                    |
| regex_v8       | 21.0 ms                                                                | 23.0 ms: 1.10x slower                                                   |
| regex_effbot   | 2.84 ms                                                                | 3.14 ms: 1.10x slower                                                   |
| regex_compile  | 121 ms                                                                 | 137 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.03 ms                                                                | 8.66 ms: 1.04x faster                                                   |
| xml_etree_parse      | 149 ms                                                                 | 143 ms: 1.04x faster                                                    |
| xml_etree_iterparse  | 96.3 ms                                                                | 93.6 ms: 1.03x faster                                                   |
| unpickle_pure_python | 186 us                                                                 | 183 us: 1.02x faster                                                    |
| json_loads           | 25.2 us                                                                | 25.7 us: 1.02x slower                                                   |
| xml_etree_generate   | 74.0 ms                                                                | 75.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 50.9 ms                                                                | 52.2 ms: 1.03x slower                                                   |
| pickle_pure_python   | 296 us                                                                 | 306 us: 1.03x slower                                                    |
| tomli_loads          | 1.67 sec                                                               | 1.77 sec: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.8 ms                                                                | 12.6 ms: 1.01x faster                                                   |
| python_startup_no_site | 7.41 ms                                                                | 7.37 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 33.0 ms                                                                | 33.4 ms: 1.01x slower                                                   |
| genshi_text     | 19.5 ms                                                                | 20.1 ms: 1.03x slower                                                   |
| mako            | 10.9 ms                                                                | 11.3 ms: 1.03x slower                                                   |
| genshi_xml      | 46.5 ms                                                                | 50.3 ms: 1.08x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 36.9 ms                                                                | 22.6 ms: 1.63x faster                                                   |
| richards_super             | 42.2 ms                                                                | 26.5 ms: 1.59x faster                                                   |
| deepcopy_memo              | 24.0 us                                                                | 22.0 us: 1.09x faster                                                   |
| float                      | 67.3 ms                                                                | 62.7 ms: 1.07x faster                                                   |
| coverage                   | 79.5 ms                                                                | 75.5 ms: 1.05x faster                                                   |
| nbody                      | 87.6 ms                                                                | 83.3 ms: 1.05x faster                                                   |
| logging_silent             | 80.8 ns                                                                | 76.9 ns: 1.05x faster                                                   |
| crypto_pyaes               | 67.4 ms                                                                | 64.3 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 3.98 ms                                                                | 3.80 ms: 1.05x faster                                                   |
| deltablue                  | 2.88 ms                                                                | 2.76 ms: 1.05x faster                                                   |
| comprehensions             | 15.0 us                                                                | 14.4 us: 1.04x faster                                                   |
| json_dumps                 | 9.03 ms                                                                | 8.66 ms: 1.04x faster                                                   |
| xml_etree_parse            | 149 ms                                                                 | 143 ms: 1.04x faster                                                    |
| gc_traversal               | 4.50 ms                                                                | 4.35 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 96.3 ms                                                                | 93.6 ms: 1.03x faster                                                   |
| scimark_lu                 | 98.6 ms                                                                | 95.9 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 672 ms                                                                 | 655 ms: 1.03x faster                                                    |
| scimark_monte_carlo        | 56.0 ms                                                                | 54.8 ms: 1.02x faster                                                   |
| unpickle_pure_python       | 186 us                                                                 | 183 us: 1.02x faster                                                    |
| scimark_sor                | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                   |
| python_startup             | 12.8 ms                                                                | 12.6 ms: 1.01x faster                                                   |
| bpe_tokeniser              | 3.93 sec                                                               | 3.90 sec: 1.01x faster                                                  |
| scimark_fft                | 244 ms                                                                 | 242 ms: 1.01x faster                                                    |
| create_gc_cycles           | 2.02 ms                                                                | 2.01 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.37 ms: 1.00x faster                                                   |
| sympy_integrate            | 18.5 ms                                                                | 18.5 ms: 1.00x slower                                                   |
| 2to3                       | 248 ms                                                                 | 249 ms: 1.00x slower                                                    |
| bench_mp_pool              | 12.3 ms                                                                | 12.3 ms: 1.00x slower                                                   |
| bench_thread_pool          | 964 us                                                                 | 970 us: 1.01x slower                                                    |
| shortest_path              | 442 ms                                                                 | 445 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 471 ms                                                                 | 475 ms: 1.01x slower                                                    |
| spectral_norm              | 83.6 ms                                                                | 84.3 ms: 1.01x slower                                                   |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 474 ms: 1.01x slower                                                    |
| django_template            | 33.0 ms                                                                | 33.4 ms: 1.01x slower                                                   |
| telco                      | 155 ms                                                                 | 157 ms: 1.01x slower                                                    |
| meteor_contest             | 103 ms                                                                 | 104 ms: 1.02x slower                                                    |
| pyflate                    | 384 ms                                                                 | 390 ms: 1.02x slower                                                    |
| async_tree_none            | 254 ms                                                                 | 258 ms: 1.02x slower                                                    |
| sqlglot_v2_transpile       | 1.47 ms                                                                | 1.49 ms: 1.02x slower                                                   |
| sqlglot_v2_parse           | 1.18 ms                                                                | 1.20 ms: 1.02x slower                                                   |
| sympy_expand               | 460 ms                                                                 | 469 ms: 1.02x slower                                                    |
| json_loads                 | 25.2 us                                                                | 25.7 us: 1.02x slower                                                   |
| thrift                     | 724 us                                                                 | 739 us: 1.02x slower                                                    |
| sqlite_synth               | 2.10 us                                                                | 2.15 us: 1.02x slower                                                   |
| async_generators           | 330 ms                                                                 | 338 ms: 1.02x slower                                                    |
| sympy_sum                  | 150 ms                                                                 | 153 ms: 1.02x slower                                                    |
| async_tree_memoization     | 301 ms                                                                 | 308 ms: 1.02x slower                                                    |
| xml_etree_generate         | 74.0 ms                                                                | 75.9 ms: 1.03x slower                                                   |
| xml_etree_process          | 50.9 ms                                                                | 52.2 ms: 1.03x slower                                                   |
| genshi_text                | 19.5 ms                                                                | 20.1 ms: 1.03x slower                                                   |
| sympy_str                  | 267 ms                                                                 | 275 ms: 1.03x slower                                                    |
| mako                       | 10.9 ms                                                                | 11.3 ms: 1.03x slower                                                   |
| pickle_pure_python         | 296 us                                                                 | 306 us: 1.03x slower                                                    |
| many_optionals             | 1.24 ms                                                                | 1.29 ms: 1.04x slower                                                   |
| generators                 | 27.0 ms                                                                | 28.1 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize        | 48.6 ms                                                                | 50.5 ms: 1.04x slower                                                   |
| sphinx                     | 964 ms                                                                 | 1.00 sec: 1.04x slower                                                  |
| deepcopy                   | 222 us                                                                 | 231 us: 1.04x slower                                                    |
| docutils                   | 2.54 sec                                                               | 2.65 sec: 1.05x slower                                                  |
| subparsers                 | 44.6 ms                                                                | 46.8 ms: 1.05x slower                                                   |
| regex_dna                  | 181 ms                                                                 | 191 ms: 1.05x slower                                                    |
| tomli_loads                | 1.67 sec                                                               | 1.77 sec: 1.05x slower                                                  |
| mdp                        | 1.11 sec                                                               | 1.17 sec: 1.06x slower                                                  |
| hexiom                     | 5.46 ms                                                                | 5.78 ms: 1.06x slower                                                   |
| chaos                      | 49.6 ms                                                                | 52.9 ms: 1.07x slower                                                   |
| sqlglot_v2_normalize       | 97.0 ms                                                                | 103 ms: 1.07x slower                                                    |
| logging_format             | 6.17 us                                                                | 6.60 us: 1.07x slower                                                   |
| logging_simple             | 5.47 us                                                                | 5.91 us: 1.08x slower                                                   |
| genshi_xml                 | 46.5 ms                                                                | 50.3 ms: 1.08x slower                                                   |
| html5lib                   | 59.0 ms                                                                | 63.9 ms: 1.08x slower                                                   |
| dulwich_log                | 68.1 ms                                                                | 74.1 ms: 1.09x slower                                                   |
| nqueens                    | 73.8 ms                                                                | 80.9 ms: 1.10x slower                                                   |
| regex_v8                   | 21.0 ms                                                                | 23.0 ms: 1.10x slower                                                   |
| regex_effbot               | 2.84 ms                                                                | 3.14 ms: 1.10x slower                                                   |
| pycparser                  | 1.05 sec                                                               | 1.16 sec: 1.11x slower                                                  |
| regex_compile              | 121 ms                                                                 | 137 ms: 1.14x slower                                                    |
| pathlib                    | 16.8 ms                                                                | 19.2 ms: 1.14x slower                                                   |
| raytrace                   | 233 ms                                                                 | 268 ms: 1.15x slower                                                    |
| go                         | 100 ms                                                                 | 120 ms: 1.20x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (14): json, k_core, deepcopy_reduce, typing_runtime_protocols, pidigits, asyncio_websockets, connected_components, coroutines, async_tree_io_tg, pprint_pformat, async_tree_io, fannkuch, async_tree_memoization_tg, pylint

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x