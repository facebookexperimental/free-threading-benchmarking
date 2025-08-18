# Results vs. 3.12.6

- fork: python
- ref: bc2872445b2aee4bb4e0
- machine: darwin-arm64
- commit hash: bc28724
- commit date: 2025-08-18
- overall geometric mean: 1.080x faster
- HPT reliability: 93.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 993 ms: 1.03x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.04x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| mako            | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 767 us: 2.62x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 608 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 483 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.39 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 831 ns: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 18.3 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 62.0 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.5 ns: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.02 sec: 1.11x faster                                                  |
| scimark_sor                      | 61.0 ms                                                  | 56.0 ms: 1.09x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                   |
| raytrace                         | 145 ms                                                   | 135 ms: 1.07x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.3 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 993 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 53.4 ms: 1.02x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.53 us: 1.02x faster                                                   |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.12 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.0 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.04x slower                                                  |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.4 us: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.0 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.8 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.0 ms: 1.08x slower                                                   |
| shortest_path                    | 219 ms                                                   | 236 ms: 1.08x slower                                                    |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 354 ms: 1.08x slower                                                    |
| sympy_str                        | 104 ms                                                   | 113 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 722 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.1 ms: 1.11x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.31 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 224 ms: 1.12x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.8 ms: 1.13x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 193 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.08 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 57.7 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.95 ms: 1.22x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.87 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 599 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| many_optionals                   | 195 us                                                   | 330 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.0 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (3): async_tree_eager_memoization_tg, logging_format, scimark_fft
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250818-3.15.0a0-bc28724-NOGIL/bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 93.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x