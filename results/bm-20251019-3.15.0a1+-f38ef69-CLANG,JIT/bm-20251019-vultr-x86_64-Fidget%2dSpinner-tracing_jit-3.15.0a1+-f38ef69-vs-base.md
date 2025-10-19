# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.021x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 251 ms: 1.01x slower                                                    |
| docutils       | 2.55 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| html5lib       | 59.5 ms                                                                | 64.4 ms: 1.08x slower                                                   |
| sphinx         | 970 ms                                                                 | 983 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 472 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 470 ms                                                                 | 474 ms: 1.01x slower                                                    |
| async_tree_memoization     | 301 ms                                                                 | 305 ms: 1.01x slower                                                    |
| async_tree_io              | 588 ms                                                                 | 595 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.02x slower                                                    |
| coroutines                 | 22.4 ms                                                                | 23.2 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (5): async_generators, asyncio_websockets, async_tree_memoization_tg, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.8 ms                                                                | 62.6 ms: 1.08x faster                                                   |
| pidigits       | 193 ms                                                                 | 192 ms: 1.00x faster                                                    |
| nbody          | 86.8 ms                                                                | 90.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 186 ms: 1.03x slower                                                    |
| regex_v8       | 21.4 ms                                                                | 22.8 ms: 1.06x slower                                                   |
| regex_effbot   | 2.87 ms                                                                | 3.10 ms: 1.08x slower                                                   |
| regex_compile  | 121 ms                                                                 | 140 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 8.97 ms                                                                | 8.71 ms: 1.03x faster                                                   |
| xml_etree_iterparse | 94.8 ms                                                                | 93.6 ms: 1.01x faster                                                   |
| pickle_pure_python  | 294 us                                                                 | 293 us: 1.01x faster                                                    |
| json_loads          | 25.6 us                                                                | 25.9 us: 1.01x slower                                                   |
| xml_etree_process   | 51.1 ms                                                                | 54.7 ms: 1.07x slower                                                   |
| tomli_loads         | 1.69 sec                                                               | 1.81 sec: 1.07x slower                                                  |
| xml_etree_generate  | 74.2 ms                                                                | 80.2 ms: 1.08x slower                                                   |
| Geometric mean      | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                | 12.7 ms: 1.00x slower                                                   |
| python_startup_no_site | 7.34 ms                                                                | 7.39 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.4 ms                                                                | 11.0 ms: 1.04x faster                                                   |
| django_template | 33.3 ms                                                                | 34.0 ms: 1.02x slower                                                   |
| genshi_text     | 19.4 ms                                                                | 21.3 ms: 1.10x slower                                                   |
| genshi_xml      | 47.1 ms                                                                | 57.7 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.07x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 38.0 ms                                                                | 28.8 ms: 1.32x faster                                                   |
| richards_super             | 43.8 ms                                                                | 33.6 ms: 1.30x faster                                                   |
| deepcopy_memo              | 24.7 us                                                                | 21.7 us: 1.14x faster                                                   |
| float                      | 67.8 ms                                                                | 62.6 ms: 1.08x faster                                                   |
| deltablue                  | 2.97 ms                                                                | 2.77 ms: 1.07x faster                                                   |
| logging_silent             | 84.4 ns                                                                | 79.6 ns: 1.06x faster                                                   |
| pprint_safe_repr           | 686 ms                                                                 | 654 ms: 1.05x faster                                                    |
| mako                       | 11.4 ms                                                                | 11.0 ms: 1.04x faster                                                   |
| spectral_norm              | 85.5 ms                                                                | 82.4 ms: 1.04x faster                                                   |
| comprehensions             | 15.2 us                                                                | 14.7 us: 1.04x faster                                                   |
| pprint_pformat             | 1.41 sec                                                               | 1.37 sec: 1.03x faster                                                  |
| json_dumps                 | 8.97 ms                                                                | 8.71 ms: 1.03x faster                                                   |
| crypto_pyaes               | 66.9 ms                                                                | 65.5 ms: 1.02x faster                                                   |
| json                       | 4.94 ms                                                                | 4.88 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 94.8 ms                                                                | 93.6 ms: 1.01x faster                                                   |
| bpe_tokeniser              | 3.94 sec                                                               | 3.91 sec: 1.01x faster                                                  |
| pickle_pure_python         | 294 us                                                                 | 293 us: 1.01x faster                                                    |
| pidigits                   | 193 ms                                                                 | 192 ms: 1.00x faster                                                    |
| scimark_sor                | 99.6 ms                                                                | 99.9 ms: 1.00x slower                                                   |
| python_startup             | 12.6 ms                                                                | 12.7 ms: 1.00x slower                                                   |
| telco                      | 156 ms                                                                 | 157 ms: 1.01x slower                                                    |
| 2to3                       | 250 ms                                                                 | 251 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.34 ms                                                                | 7.39 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 2.38 us                                                                | 2.40 us: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 472 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 470 ms                                                                 | 474 ms: 1.01x slower                                                    |
| json_loads                 | 25.6 us                                                                | 25.9 us: 1.01x slower                                                   |
| async_tree_memoization     | 301 ms                                                                 | 305 ms: 1.01x slower                                                    |
| docutils                   | 2.55 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| async_tree_io              | 588 ms                                                                 | 595 ms: 1.01x slower                                                    |
| sphinx                     | 970 ms                                                                 | 983 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 244 ms: 1.02x slower                                                    |
| sympy_integrate            | 18.5 ms                                                                | 18.8 ms: 1.02x slower                                                   |
| thrift                     | 734 us                                                                 | 747 us: 1.02x slower                                                    |
| pycparser                  | 1.07 sec                                                               | 1.09 sec: 1.02x slower                                                  |
| scimark_fft                | 245 ms                                                                 | 250 ms: 1.02x slower                                                    |
| scimark_monte_carlo        | 56.3 ms                                                                | 57.5 ms: 1.02x slower                                                   |
| scimark_lu                 | 99.7 ms                                                                | 102 ms: 1.02x slower                                                    |
| django_template            | 33.3 ms                                                                | 34.0 ms: 1.02x slower                                                   |
| pyflate                    | 386 ms                                                                 | 396 ms: 1.03x slower                                                    |
| many_optionals             | 1.23 ms                                                                | 1.27 ms: 1.03x slower                                                   |
| coverage                   | 74.2 ms                                                                | 76.2 ms: 1.03x slower                                                   |
| logging_format             | 6.31 us                                                                | 6.49 us: 1.03x slower                                                   |
| sympy_sum                  | 150 ms                                                                 | 154 ms: 1.03x slower                                                    |
| regex_dna                  | 181 ms                                                                 | 186 ms: 1.03x slower                                                    |
| sympy_expand               | 457 ms                                                                 | 471 ms: 1.03x slower                                                    |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.50 ms: 1.03x slower                                                   |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.21 ms: 1.04x slower                                                   |
| coroutines                 | 22.4 ms                                                                | 23.2 ms: 1.04x slower                                                   |
| logging_simple             | 5.58 us                                                                | 5.79 us: 1.04x slower                                                   |
| deepcopy                   | 224 us                                                                 | 232 us: 1.04x slower                                                    |
| nbody                      | 86.8 ms                                                                | 90.2 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize        | 48.9 ms                                                                | 50.9 ms: 1.04x slower                                                   |
| sympy_str                  | 267 ms                                                                 | 277 ms: 1.04x slower                                                    |
| hexiom                     | 5.56 ms                                                                | 5.80 ms: 1.04x slower                                                   |
| nqueens                    | 75.9 ms                                                                | 79.5 ms: 1.05x slower                                                   |
| subparsers                 | 44.4 ms                                                                | 46.9 ms: 1.05x slower                                                   |
| sqlglot_v2_normalize       | 97.9 ms                                                                | 103 ms: 1.06x slower                                                    |
| gc_traversal               | 4.24 ms                                                                | 4.48 ms: 1.06x slower                                                   |
| regex_v8                   | 21.4 ms                                                                | 22.8 ms: 1.06x slower                                                   |
| chaos                      | 50.1 ms                                                                | 53.5 ms: 1.07x slower                                                   |
| xml_etree_process          | 51.1 ms                                                                | 54.7 ms: 1.07x slower                                                   |
| dulwich_log                | 68.2 ms                                                                | 73.2 ms: 1.07x slower                                                   |
| tomli_loads                | 1.69 sec                                                               | 1.81 sec: 1.07x slower                                                  |
| regex_effbot               | 2.87 ms                                                                | 3.10 ms: 1.08x slower                                                   |
| html5lib                   | 59.5 ms                                                                | 64.4 ms: 1.08x slower                                                   |
| xml_etree_generate         | 74.2 ms                                                                | 80.2 ms: 1.08x slower                                                   |
| mdp                        | 1.11 sec                                                               | 1.22 sec: 1.09x slower                                                  |
| genshi_text                | 19.4 ms                                                                | 21.3 ms: 1.10x slower                                                   |
| pathlib                    | 16.9 ms                                                                | 19.0 ms: 1.13x slower                                                   |
| raytrace                   | 235 ms                                                                 | 269 ms: 1.15x slower                                                    |
| regex_compile              | 121 ms                                                                 | 140 ms: 1.15x slower                                                    |
| meteor_contest             | 103 ms                                                                 | 124 ms: 1.20x slower                                                    |
| genshi_xml                 | 47.1 ms                                                                | 57.7 ms: 1.22x slower                                                   |
| go                         | 99.7 ms                                                                | 122 ms: 1.23x slower                                                    |
| generators                 | 27.1 ms                                                                | 36.2 ms: 1.33x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (18): k_core, scimark_sparse_mat_mult, fannkuch, async_generators, asyncio_websockets, bench_mp_pool, typing_runtime_protocols, bench_thread_pool, connected_components, xml_etree_parse, shortest_path, create_gc_cycles, async_tree_memoization_tg, unpickle_pure_python, sqlite_synth, async_tree_none, async_tree_io_tg, pylint

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x