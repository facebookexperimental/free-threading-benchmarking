# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 55892a4
- commit date: 2025-10-20
- overall geometric mean: 1.014x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.55 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| html5lib       | 58.3 ms                                                                | 64.3 ms: 1.10x slower                                                   |
| sphinx         | 970 ms                                                                 | 994 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines                 | 22.5 ms                                                                | 21.8 ms: 1.03x faster                                                   |
| async_generators           | 336 ms                                                                 | 337 ms: 1.00x slower                                                    |
| async_tree_none_tg         | 240 ms                                                                 | 244 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 468 ms                                                                 | 477 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 477 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 302 ms                                                                 | 308 ms: 1.02x slower                                                    |
| async_tree_io              | 584 ms                                                                 | 599 ms: 1.03x slower                                                    |
| async_tree_memoization     | 301 ms                                                                 | 310 ms: 1.03x slower                                                    |
| async_tree_none            | 253 ms                                                                 | 261 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 66.8 ms                                                                | 62.5 ms: 1.07x faster                                                   |
| nbody          | 95.1 ms                                                                | 92.0 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 175 ms: 1.07x faster                                                    |
| regex_effbot   | 3.11 ms                                                                | 2.93 ms: 1.06x faster                                                   |
| regex_v8       | 21.5 ms                                                                | 22.0 ms: 1.03x slower                                                   |
| regex_compile  | 122 ms                                                                 | 129 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps          | 9.05 ms                                                                | 8.74 ms: 1.04x faster                                                   |
| xml_etree_iterparse | 95.1 ms                                                                | 94.5 ms: 1.01x faster                                                   |
| xml_etree_parse     | 143 ms                                                                 | 144 ms: 1.01x slower                                                    |
| pickle_pure_python  | 295 us                                                                 | 298 us: 1.01x slower                                                    |
| json_loads          | 25.5 us                                                                | 26.1 us: 1.02x slower                                                   |
| xml_etree_process   | 51.1 ms                                                                | 52.7 ms: 1.03x slower                                                   |
| xml_etree_generate  | 74.4 ms                                                                | 77.2 ms: 1.04x slower                                                   |
| tomli_loads         | 1.69 sec                                                               | 2.02 sec: 1.20x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| python_startup_no_site | 7.35 ms                                                                | 7.44 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                   |
| mako            | 11.1 ms                                                                | 11.4 ms: 1.02x slower                                                   |
| django_template | 32.8 ms                                                                | 33.9 ms: 1.03x slower                                                   |
| genshi_xml      | 46.5 ms                                                                | 51.6 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-55892a4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 36.7 ms                                                                | 24.2 ms: 1.52x faster                                                   |
| richards_super             | 42.1 ms                                                                | 28.8 ms: 1.46x faster                                                   |
| deepcopy_memo              | 24.0 us                                                                | 22.0 us: 1.09x faster                                                   |
| regex_dna                  | 187 ms                                                                 | 175 ms: 1.07x faster                                                    |
| float                      | 66.8 ms                                                                | 62.5 ms: 1.07x faster                                                   |
| regex_effbot               | 3.11 ms                                                                | 2.93 ms: 1.06x faster                                                   |
| scimark_lu                 | 99.5 ms                                                                | 94.7 ms: 1.05x faster                                                   |
| logging_silent             | 81.7 ns                                                                | 78.0 ns: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 3.98 ms                                                                | 3.82 ms: 1.04x faster                                                   |
| comprehensions             | 15.1 us                                                                | 14.6 us: 1.04x faster                                                   |
| json_dumps                 | 9.05 ms                                                                | 8.74 ms: 1.04x faster                                                   |
| nbody                      | 95.1 ms                                                                | 92.0 ms: 1.03x faster                                                   |
| coroutines                 | 22.5 ms                                                                | 21.8 ms: 1.03x faster                                                   |
| deltablue                  | 2.88 ms                                                                | 2.79 ms: 1.03x faster                                                   |
| crypto_pyaes               | 67.4 ms                                                                | 66.6 ms: 1.01x faster                                                   |
| coverage                   | 74.9 ms                                                                | 74.1 ms: 1.01x faster                                                   |
| scimark_fft                | 244 ms                                                                 | 242 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 95.1 ms                                                                | 94.5 ms: 1.01x faster                                                   |
| telco                      | 155 ms                                                                 | 154 ms: 1.00x faster                                                    |
| async_generators           | 336 ms                                                                 | 337 ms: 1.00x slower                                                    |
| xml_etree_parse            | 143 ms                                                                 | 144 ms: 1.01x slower                                                    |
| pickle_pure_python         | 295 us                                                                 | 298 us: 1.01x slower                                                    |
| bench_mp_pool              | 12.3 ms                                                                | 12.4 ms: 1.01x slower                                                   |
| python_startup             | 12.6 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 146 us                                                                 | 148 us: 1.01x slower                                                    |
| python_startup_no_site     | 7.35 ms                                                                | 7.44 ms: 1.01x slower                                                   |
| shortest_path              | 438 ms                                                                 | 444 ms: 1.01x slower                                                    |
| meteor_contest             | 104 ms                                                                 | 106 ms: 1.01x slower                                                    |
| connected_components       | 401 ms                                                                 | 407 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 240 ms                                                                 | 244 ms: 1.02x slower                                                    |
| bpe_tokeniser              | 3.96 sec                                                               | 4.03 sec: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 468 ms                                                                 | 477 ms: 1.02x slower                                                    |
| genshi_text                | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed    | 468 ms                                                                 | 477 ms: 1.02x slower                                                    |
| async_tree_memoization_tg  | 302 ms                                                                 | 308 ms: 1.02x slower                                                    |
| generators                 | 27.3 ms                                                                | 27.8 ms: 1.02x slower                                                   |
| pprint_pformat             | 1.40 sec                                                               | 1.43 sec: 1.02x slower                                                  |
| json_loads                 | 25.5 us                                                                | 26.1 us: 1.02x slower                                                   |
| mako                       | 11.1 ms                                                                | 11.4 ms: 1.02x slower                                                   |
| pyflate                    | 385 ms                                                                 | 395 ms: 1.02x slower                                                    |
| regex_v8                   | 21.5 ms                                                                | 22.0 ms: 1.03x slower                                                   |
| sphinx                     | 970 ms                                                                 | 994 ms: 1.03x slower                                                    |
| async_tree_io              | 584 ms                                                                 | 599 ms: 1.03x slower                                                    |
| docutils                   | 2.55 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| async_tree_memoization     | 301 ms                                                                 | 310 ms: 1.03x slower                                                    |
| sympy_integrate            | 18.4 ms                                                                | 18.9 ms: 1.03x slower                                                   |
| sqlglot_v2_transpile       | 1.47 ms                                                                | 1.51 ms: 1.03x slower                                                   |
| scimark_monte_carlo        | 55.4 ms                                                                | 57.0 ms: 1.03x slower                                                   |
| async_tree_none            | 253 ms                                                                 | 261 ms: 1.03x slower                                                    |
| xml_etree_process          | 51.1 ms                                                                | 52.7 ms: 1.03x slower                                                   |
| pylint                     | 273 ms                                                                 | 282 ms: 1.03x slower                                                    |
| django_template            | 32.8 ms                                                                | 33.9 ms: 1.03x slower                                                   |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.21 ms: 1.03x slower                                                   |
| many_optionals             | 1.24 ms                                                                | 1.29 ms: 1.03x slower                                                   |
| xml_etree_generate         | 74.4 ms                                                                | 77.2 ms: 1.04x slower                                                   |
| thrift                     | 711 us                                                                 | 737 us: 1.04x slower                                                    |
| deepcopy_reduce            | 2.36 us                                                                | 2.46 us: 1.04x slower                                                   |
| sympy_sum                  | 150 ms                                                                 | 156 ms: 1.04x slower                                                    |
| sqlglot_v2_optimize        | 48.6 ms                                                                | 50.6 ms: 1.04x slower                                                   |
| sympy_str                  | 268 ms                                                                 | 279 ms: 1.04x slower                                                    |
| sympy_expand               | 460 ms                                                                 | 479 ms: 1.04x slower                                                    |
| regex_compile              | 122 ms                                                                 | 129 ms: 1.06x slower                                                    |
| chaos                      | 49.8 ms                                                                | 52.7 ms: 1.06x slower                                                   |
| deepcopy                   | 221 us                                                                 | 235 us: 1.06x slower                                                    |
| sqlglot_v2_normalize       | 97.3 ms                                                                | 104 ms: 1.06x slower                                                    |
| mdp                        | 1.10 sec                                                               | 1.18 sec: 1.06x slower                                                  |
| nqueens                    | 75.0 ms                                                                | 80.6 ms: 1.07x slower                                                   |
| hexiom                     | 5.48 ms                                                                | 5.91 ms: 1.08x slower                                                   |
| subparsers                 | 44.8 ms                                                                | 48.4 ms: 1.08x slower                                                   |
| pycparser                  | 1.06 sec                                                               | 1.15 sec: 1.08x slower                                                  |
| html5lib                   | 58.3 ms                                                                | 64.3 ms: 1.10x slower                                                   |
| logging_format             | 6.21 us                                                                | 6.86 us: 1.10x slower                                                   |
| dulwich_log                | 68.3 ms                                                                | 75.4 ms: 1.10x slower                                                   |
| genshi_xml                 | 46.5 ms                                                                | 51.6 ms: 1.11x slower                                                   |
| logging_simple             | 5.48 us                                                                | 6.11 us: 1.12x slower                                                   |
| pathlib                    | 16.8 ms                                                                | 19.3 ms: 1.14x slower                                                   |
| raytrace                   | 232 ms                                                                 | 266 ms: 1.15x slower                                                    |
| go                         | 99.7 ms                                                                | 116 ms: 1.16x slower                                                    |
| tomli_loads                | 1.69 sec                                                               | 2.02 sec: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (15): sqlite_synth, pprint_safe_repr, gc_traversal, json, k_core, fannkuch, spectral_norm, scimark_sor, asyncio_websockets, pidigits, create_gc_cycles, 2to3, bench_thread_pool, unpickle_pure_python, async_tree_io_tg

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.01x