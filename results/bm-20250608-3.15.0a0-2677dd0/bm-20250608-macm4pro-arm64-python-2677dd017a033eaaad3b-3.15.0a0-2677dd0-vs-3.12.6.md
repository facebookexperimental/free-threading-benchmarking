# Results vs. 3.12.6

- fork: python
- ref: 2677dd017a033eaaad3b
- machine: darwin-arm64
- commit hash: 2677dd0
- commit date: 2025-06-08
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.6 ms: 2.66x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| nbody          | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.5 us: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 902 ms: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.37 ms: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.13 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                   |
| mako            | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                   |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.37 ms: 2.22x faster                                                   |
| mdp                              | 1.09 sec                                                 | 503 ms: 2.17x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.06x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 244 ms: 1.88x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.52x faster                                                   |
| deepcopy                         | 161 us                                                   | 107 us: 1.52x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.18 us: 1.37x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.0 ms: 1.29x faster                                                   |
| go                               | 70.0 ms                                                  | 54.3 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 167 ms: 1.24x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.3 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.7 ms: 1.21x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 46.1 ms: 1.18x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 46.8 ms: 1.17x faster                                                   |
| nbody                            | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.16x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.1 us: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.81 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.5 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.9 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.11x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.31 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 46.9 ms: 1.09x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.65 ms: 1.09x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.2 ms: 1.07x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 96.5 us: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 902 ms: 1.06x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.8 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.69 us: 1.04x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.48 us: 1.04x faster                                                   |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                    |
| json                             | 1.93 ms                                                  | 1.87 ms: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 483 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 46.7 ms: 1.02x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.74 ms: 1.01x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.53 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.37 ms: 1.02x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 695 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 344 ms: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.54 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.13 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.4 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.4 ms: 1.20x slower                                                   |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.6 ms: 2.66x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 195 ns: 3.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): shortest_path, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250608-3.15.0a0-2677dd0/bm-20250608-macm4pro-arm64-python-2677dd017a033eaaad3b-3.15.0a0-2677dd0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x