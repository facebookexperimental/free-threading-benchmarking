# Results vs. 3.12.6

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: darwin-arm64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.5 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.02x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.95 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 539 ms: 2.02x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.55 us: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| go                               | 70.0 ms                                                  | 55.9 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.4 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.5 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 954 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| nbody                            | 54.2 ms                                                  | 48.2 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.9 us: 1.11x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.79 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.57 us: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.8 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.0 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.95 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.6 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 952 ns: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 658 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                   |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.6 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.74 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.3 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.12x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 948 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 323 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): pycparser, connected_components, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.14x