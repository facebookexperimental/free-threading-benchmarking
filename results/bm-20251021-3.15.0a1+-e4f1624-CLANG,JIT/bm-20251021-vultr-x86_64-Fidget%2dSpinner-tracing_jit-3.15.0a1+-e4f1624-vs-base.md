# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: e4f1624
- commit date: 2025-10-21
- overall geometric mean: 1.016x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 250 ms: 1.00x slower                                                    |
| docutils       | 2.54 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| html5lib       | 57.8 ms                                                                | 63.8 ms: 1.10x slower                                                   |
| sphinx         | 968 ms                                                                 | 990 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 476 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 474 ms: 1.01x slower                                                    |
| async_tree_memoization     | 302 ms                                                                 | 306 ms: 1.01x slower                                                    |
| async_generators           | 332 ms                                                                 | 338 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 245 ms: 1.02x slower                                                    |
| coroutines                 | 22.0 ms                                                                | 22.8 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (5): asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.5 ms                                                                | 62.7 ms: 1.08x faster                                                   |
| pidigits       | 192 ms                                                                 | 192 ms: 1.00x faster                                                    |
| nbody          | 86.9 ms                                                                | 97.2 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 179 ms                                                                 | 186 ms: 1.04x slower                                                    |
| regex_v8       | 21.2 ms                                                                | 22.4 ms: 1.06x slower                                                   |
| regex_effbot   | 2.82 ms                                                                | 3.11 ms: 1.10x slower                                                   |
| regex_compile  | 121 ms                                                                 | 139 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                                | 93.9 ms: 1.01x faster                                                   |
| unpickle_pure_python | 184 us                                                                 | 185 us: 1.01x slower                                                    |
| xml_etree_generate   | 74.8 ms                                                                | 76.1 ms: 1.02x slower                                                   |
| xml_etree_process    | 51.0 ms                                                                | 52.2 ms: 1.02x slower                                                   |
| tomli_loads          | 1.69 sec                                                               | 1.99 sec: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (4): json_dumps, pickle_pure_python, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                                | 7.44 ms: 1.01x slower                                                   |
| python_startup         | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                   |
| genshi_text     | 19.4 ms                                                                | 19.7 ms: 1.01x slower                                                   |
| django_template | 32.8 ms                                                                | 34.4 ms: 1.05x slower                                                   |
| genshi_xml      | 46.3 ms                                                                | 49.4 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251021-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e4f1624 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 37.3 ms                                                                | 22.4 ms: 1.67x faster                                                   |
| richards_super             | 42.9 ms                                                                | 26.5 ms: 1.62x faster                                                   |
| deepcopy_memo              | 24.0 us                                                                | 21.8 us: 1.10x faster                                                   |
| logging_silent             | 83.3 ns                                                                | 76.1 ns: 1.10x faster                                                   |
| float                      | 67.5 ms                                                                | 62.7 ms: 1.08x faster                                                   |
| deltablue                  | 2.95 ms                                                                | 2.76 ms: 1.07x faster                                                   |
| scimark_lu                 | 99.3 ms                                                                | 94.5 ms: 1.05x faster                                                   |
| scimark_sor                | 101 ms                                                                 | 97.5 ms: 1.04x faster                                                   |
| comprehensions             | 15.2 us                                                                | 14.7 us: 1.03x faster                                                   |
| scimark_monte_carlo        | 56.4 ms                                                                | 54.9 ms: 1.03x faster                                                   |
| pprint_safe_repr           | 680 ms                                                                 | 662 ms: 1.03x faster                                                    |
| pprint_pformat             | 1.39 sec                                                               | 1.36 sec: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 3.93 ms                                                                | 3.84 ms: 1.02x faster                                                   |
| json                       | 4.89 ms                                                                | 4.81 ms: 1.02x faster                                                   |
| crypto_pyaes               | 66.7 ms                                                                | 65.7 ms: 1.02x faster                                                   |
| scimark_fft                | 246 ms                                                                 | 242 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.38 us                                                                | 2.35 us: 1.01x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                                | 93.9 ms: 1.01x faster                                                   |
| spectral_norm              | 84.6 ms                                                                | 84.4 ms: 1.00x faster                                                   |
| pidigits                   | 192 ms                                                                 | 192 ms: 1.00x faster                                                    |
| mako                       | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                   |
| 2to3                       | 249 ms                                                                 | 250 ms: 1.00x slower                                                    |
| unpickle_pure_python       | 184 us                                                                 | 185 us: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                                | 7.44 ms: 1.01x slower                                                   |
| python_startup             | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 145 us                                                                 | 146 us: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 476 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 469 ms                                                                 | 474 ms: 1.01x slower                                                    |
| connected_components       | 402 ms                                                                 | 407 ms: 1.01x slower                                                    |
| telco                      | 155 ms                                                                 | 157 ms: 1.01x slower                                                    |
| async_tree_memoization     | 302 ms                                                                 | 306 ms: 1.01x slower                                                    |
| pyflate                    | 389 ms                                                                 | 394 ms: 1.01x slower                                                    |
| genshi_text                | 19.4 ms                                                                | 19.7 ms: 1.01x slower                                                   |
| meteor_contest             | 104 ms                                                                 | 106 ms: 1.01x slower                                                    |
| shortest_path              | 441 ms                                                                 | 448 ms: 1.02x slower                                                    |
| sympy_integrate            | 18.4 ms                                                                | 18.7 ms: 1.02x slower                                                   |
| async_generators           | 332 ms                                                                 | 338 ms: 1.02x slower                                                    |
| xml_etree_generate         | 74.8 ms                                                                | 76.1 ms: 1.02x slower                                                   |
| async_tree_none_tg         | 241 ms                                                                 | 245 ms: 1.02x slower                                                    |
| xml_etree_process          | 51.0 ms                                                                | 52.2 ms: 1.02x slower                                                   |
| sphinx                     | 968 ms                                                                 | 990 ms: 1.02x slower                                                    |
| docutils                   | 2.54 sec                                                               | 2.62 sec: 1.03x slower                                                  |
| generators                 | 27.1 ms                                                                | 28.0 ms: 1.03x slower                                                   |
| sympy_expand               | 458 ms                                                                 | 473 ms: 1.03x slower                                                    |
| coroutines                 | 22.0 ms                                                                | 22.8 ms: 1.03x slower                                                   |
| logging_format             | 6.38 us                                                                | 6.61 us: 1.03x slower                                                   |
| regex_dna                  | 179 ms                                                                 | 186 ms: 1.04x slower                                                    |
| deepcopy                   | 218 us                                                                 | 227 us: 1.04x slower                                                    |
| sympy_sum                  | 150 ms                                                                 | 155 ms: 1.04x slower                                                    |
| sqlglot_v2_optimize        | 48.5 ms                                                                | 50.4 ms: 1.04x slower                                                   |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.52 ms: 1.04x slower                                                   |
| thrift                     | 707 us                                                                 | 740 us: 1.05x slower                                                    |
| sympy_str                  | 267 ms                                                                 | 279 ms: 1.05x slower                                                    |
| many_optionals             | 1.24 ms                                                                | 1.30 ms: 1.05x slower                                                   |
| logging_simple             | 5.61 us                                                                | 5.87 us: 1.05x slower                                                   |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.22 ms: 1.05x slower                                                   |
| django_template            | 32.8 ms                                                                | 34.4 ms: 1.05x slower                                                   |
| regex_v8                   | 21.2 ms                                                                | 22.4 ms: 1.06x slower                                                   |
| hexiom                     | 5.58 ms                                                                | 5.90 ms: 1.06x slower                                                   |
| chaos                      | 50.0 ms                                                                | 52.9 ms: 1.06x slower                                                   |
| sqlglot_v2_normalize       | 96.5 ms                                                                | 103 ms: 1.06x slower                                                    |
| genshi_xml                 | 46.3 ms                                                                | 49.4 ms: 1.07x slower                                                   |
| subparsers                 | 44.7 ms                                                                | 48.1 ms: 1.08x slower                                                   |
| nqueens                    | 74.7 ms                                                                | 80.9 ms: 1.08x slower                                                   |
| dulwich_log                | 68.1 ms                                                                | 73.9 ms: 1.08x slower                                                   |
| regex_effbot               | 2.82 ms                                                                | 3.11 ms: 1.10x slower                                                   |
| html5lib                   | 57.8 ms                                                                | 63.8 ms: 1.10x slower                                                   |
| nbody                      | 86.9 ms                                                                | 97.2 ms: 1.12x slower                                                   |
| pycparser                  | 1.07 sec                                                               | 1.21 sec: 1.13x slower                                                  |
| regex_compile              | 121 ms                                                                 | 139 ms: 1.15x slower                                                    |
| raytrace                   | 233 ms                                                                 | 268 ms: 1.15x slower                                                    |
| pathlib                    | 16.8 ms                                                                | 19.5 ms: 1.16x slower                                                   |
| tomli_loads                | 1.69 sec                                                               | 1.99 sec: 1.17x slower                                                  |
| go                         | 101 ms                                                                 | 121 ms: 1.20x slower                                                    |
| mdp                        | 1.11 sec                                                               | 1.63 sec: 1.47x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (19): json_dumps, sqlite_synth, create_gc_cycles, gc_traversal, pickle_pure_python, fannkuch, k_core, json_loads, bench_thread_pool, asyncio_websockets, bpe_tokeniser, bench_mp_pool, coverage, xml_etree_parse, async_tree_io, async_tree_io_tg, async_tree_none, async_tree_memoization_tg, pylint

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x