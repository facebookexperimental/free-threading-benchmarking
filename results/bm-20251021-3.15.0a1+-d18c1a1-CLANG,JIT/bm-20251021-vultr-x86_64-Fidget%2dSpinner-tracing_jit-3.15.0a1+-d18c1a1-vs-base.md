# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: d18c1a1
- commit date: 2025-10-21
- overall geometric mean: 1.009x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.56 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| html5lib       | 59.0 ms                                                                | 63.2 ms: 1.07x slower                                                   |
| sphinx         | 971 ms                                                                 | 992 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 474 ms                                                                 | 472 ms: 1.00x faster                                                    |
| async_tree_memoization     | 301 ms                                                                 | 305 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 240 ms                                                                 | 245 ms: 1.02x slower                                                    |
| async_tree_none            | 255 ms                                                                 | 260 ms: 1.02x slower                                                    |
| async_generators           | 332 ms                                                                 | 339 ms: 1.02x slower                                                    |
| coroutines                 | 22.2 ms                                                                | 22.7 ms: 1.02x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.8 ms                                                                | 62.7 ms: 1.08x faster                                                   |
| pidigits       | 195 ms                                                                 | 193 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                 | 176 ms: 1.03x faster                                                    |
| regex_effbot   | 2.89 ms                                                                | 2.92 ms: 1.01x slower                                                   |
| regex_v8       | 21.3 ms                                                                | 22.2 ms: 1.04x slower                                                   |
| regex_compile  | 121 ms                                                                 | 139 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.05 ms                                                                | 8.79 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 96.6 ms                                                                | 95.2 ms: 1.01x faster                                                   |
| unpickle_pure_python | 187 us                                                                 | 185 us: 1.01x faster                                                    |
| xml_etree_parse      | 148 ms                                                                 | 148 ms: 1.00x faster                                                    |
| xml_etree_generate   | 75.2 ms                                                                | 76.6 ms: 1.02x slower                                                   |
| xml_etree_process    | 51.6 ms                                                                | 52.7 ms: 1.02x slower                                                   |
| pickle_pure_python   | 295 us                                                                 | 304 us: 1.03x slower                                                    |
| tomli_loads          | 1.73 sec                                                               | 2.00 sec: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.37 ms                                                                | 7.46 ms: 1.01x slower                                                   |
| python_startup         | 12.6 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.0 ms: 1.02x faster                                                   |
| django_template | 32.7 ms                                                                | 33.4 ms: 1.02x slower                                                   |
| genshi_text     | 19.2 ms                                                                | 19.7 ms: 1.03x slower                                                   |
| genshi_xml      | 47.1 ms                                                                | 50.1 ms: 1.06x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-d18c1a1 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 37.5 ms                                                                | 22.0 ms: 1.70x faster                                                   |
| richards_super             | 42.9 ms                                                                | 26.8 ms: 1.60x faster                                                   |
| deepcopy_memo              | 24.5 us                                                                | 22.0 us: 1.11x faster                                                   |
| float                      | 67.8 ms                                                                | 62.7 ms: 1.08x faster                                                   |
| logging_silent             | 84.6 ns                                                                | 78.9 ns: 1.07x faster                                                   |
| deltablue                  | 2.95 ms                                                                | 2.78 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 688 ms                                                                 | 653 ms: 1.05x faster                                                    |
| comprehensions             | 15.1 us                                                                | 14.6 us: 1.03x faster                                                   |
| json_dumps                 | 9.05 ms                                                                | 8.79 ms: 1.03x faster                                                   |
| spectral_norm              | 86.1 ms                                                                | 83.6 ms: 1.03x faster                                                   |
| regex_dna                  | 181 ms                                                                 | 176 ms: 1.03x faster                                                    |
| json                       | 4.95 ms                                                                | 4.84 ms: 1.02x faster                                                   |
| scimark_lu                 | 98.6 ms                                                                | 96.6 ms: 1.02x faster                                                   |
| mako                       | 11.2 ms                                                                | 11.0 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 96.6 ms                                                                | 95.2 ms: 1.01x faster                                                   |
| fannkuch                   | 358 ms                                                                 | 353 ms: 1.01x faster                                                    |
| deepcopy_reduce            | 2.36 us                                                                | 2.33 us: 1.01x faster                                                   |
| pidigits                   | 195 ms                                                                 | 193 ms: 1.01x faster                                                    |
| coverage                   | 75.9 ms                                                                | 75.2 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 187 us                                                                 | 185 us: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 474 ms                                                                 | 472 ms: 1.00x faster                                                    |
| xml_etree_parse            | 148 ms                                                                 | 148 ms: 1.00x faster                                                    |
| scimark_sparse_mat_mult    | 4.00 ms                                                                | 4.01 ms: 1.00x slower                                                   |
| scimark_fft                | 245 ms                                                                 | 247 ms: 1.01x slower                                                    |
| async_tree_memoization     | 301 ms                                                                 | 305 ms: 1.01x slower                                                    |
| generators                 | 27.3 ms                                                                | 27.6 ms: 1.01x slower                                                   |
| regex_effbot               | 2.89 ms                                                                | 2.92 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.37 ms                                                                | 7.46 ms: 1.01x slower                                                   |
| pyflate                    | 391 ms                                                                 | 396 ms: 1.01x slower                                                    |
| python_startup             | 12.6 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| sympy_integrate            | 18.4 ms                                                                | 18.7 ms: 1.01x slower                                                   |
| bench_mp_pool              | 12.2 ms                                                                | 12.4 ms: 1.01x slower                                                   |
| shortest_path              | 442 ms                                                                 | 449 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 240 ms                                                                 | 245 ms: 1.02x slower                                                    |
| async_tree_none            | 255 ms                                                                 | 260 ms: 1.02x slower                                                    |
| meteor_contest             | 104 ms                                                                 | 106 ms: 1.02x slower                                                    |
| xml_etree_generate         | 75.2 ms                                                                | 76.6 ms: 1.02x slower                                                   |
| xml_etree_process          | 51.6 ms                                                                | 52.7 ms: 1.02x slower                                                   |
| typing_runtime_protocols   | 145 us                                                                 | 148 us: 1.02x slower                                                    |
| scimark_monte_carlo        | 54.9 ms                                                                | 56.0 ms: 1.02x slower                                                   |
| async_generators           | 332 ms                                                                 | 339 ms: 1.02x slower                                                    |
| sphinx                     | 971 ms                                                                 | 992 ms: 1.02x slower                                                    |
| connected_components       | 400 ms                                                                 | 409 ms: 1.02x slower                                                    |
| django_template            | 32.7 ms                                                                | 33.4 ms: 1.02x slower                                                   |
| coroutines                 | 22.2 ms                                                                | 22.7 ms: 1.02x slower                                                   |
| genshi_text                | 19.2 ms                                                                | 19.7 ms: 1.03x slower                                                   |
| docutils                   | 2.56 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| pickle_pure_python         | 295 us                                                                 | 304 us: 1.03x slower                                                    |
| sympy_sum                  | 150 ms                                                                 | 154 ms: 1.03x slower                                                    |
| deepcopy                   | 221 us                                                                 | 229 us: 1.04x slower                                                    |
| sympy_expand               | 457 ms                                                                 | 475 ms: 1.04x slower                                                    |
| sqlglot_v2_optimize        | 48.6 ms                                                                | 50.7 ms: 1.04x slower                                                   |
| many_optionals             | 1.24 ms                                                                | 1.29 ms: 1.04x slower                                                   |
| regex_v8                   | 21.3 ms                                                                | 22.2 ms: 1.04x slower                                                   |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.52 ms: 1.05x slower                                                   |
| sqlglot_v2_parse           | 1.16 ms                                                                | 1.21 ms: 1.05x slower                                                   |
| logging_simple             | 5.60 us                                                                | 5.87 us: 1.05x slower                                                   |
| sympy_str                  | 266 ms                                                                 | 279 ms: 1.05x slower                                                    |
| logging_format             | 6.27 us                                                                | 6.58 us: 1.05x slower                                                   |
| nqueens                    | 77.0 ms                                                                | 81.1 ms: 1.05x slower                                                   |
| gc_traversal               | 4.28 ms                                                                | 4.51 ms: 1.05x slower                                                   |
| chaos                      | 50.0 ms                                                                | 52.9 ms: 1.06x slower                                                   |
| thrift                     | 711 us                                                                 | 753 us: 1.06x slower                                                    |
| mdp                        | 1.11 sec                                                               | 1.18 sec: 1.06x slower                                                  |
| hexiom                     | 5.54 ms                                                                | 5.88 ms: 1.06x slower                                                   |
| genshi_xml                 | 47.1 ms                                                                | 50.1 ms: 1.06x slower                                                   |
| html5lib                   | 59.0 ms                                                                | 63.2 ms: 1.07x slower                                                   |
| dulwich_log                | 68.5 ms                                                                | 73.5 ms: 1.07x slower                                                   |
| sqlglot_v2_normalize       | 97.6 ms                                                                | 105 ms: 1.07x slower                                                    |
| subparsers                 | 45.2 ms                                                                | 48.8 ms: 1.08x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.20 sec: 1.11x slower                                                  |
| regex_compile              | 121 ms                                                                 | 139 ms: 1.15x slower                                                    |
| pathlib                    | 16.8 ms                                                                | 19.3 ms: 1.15x slower                                                   |
| tomli_loads                | 1.73 sec                                                               | 2.00 sec: 1.15x slower                                                  |
| raytrace                   | 235 ms                                                                 | 273 ms: 1.16x slower                                                    |
| go                         | 101 ms                                                                 | 121 ms: 1.20x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (18): pprint_pformat, k_core, crypto_pyaes, scimark_sor, async_tree_cpu_io_mixed, asyncio_websockets, nbody, 2to3, bpe_tokeniser, create_gc_cycles, bench_thread_pool, async_tree_io_tg, json_loads, telco, sqlite_synth, async_tree_io, async_tree_memoization_tg, pylint

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x