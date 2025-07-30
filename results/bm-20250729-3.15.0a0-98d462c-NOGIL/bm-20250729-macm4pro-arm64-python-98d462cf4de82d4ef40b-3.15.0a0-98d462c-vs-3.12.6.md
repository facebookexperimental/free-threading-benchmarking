# Results vs. 3.12.6

- fork: python
- ref: 98d462cf4de82d4ef40b
- machine: darwin-arm64
- commit hash: 98d462c
- commit date: 2025-07-29
- overall geometric mean: 1.084x faster
- HPT reliability: 96.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 201 ms: 2.22x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 59.5 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| tomli_loads          | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.53 ms: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.63 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.99 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.1 ms: 1.11x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 769 us: 2.61x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 201 ms: 2.22x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 601 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 484 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 119 us: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.27 us: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 815 ns: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.18x faster                                                   |
| go                               | 70.0 ms                                                  | 60.9 ms: 1.15x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.1 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.3 ns: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.19 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 43.2 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.85 us: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.05x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 703 ms: 1.06x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.53 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.1 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.9 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| nbody                            | 54.2 ms                                                  | 59.5 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.1 ms: 1.11x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.33 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.63 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.99 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.24 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 600 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.5 ms: 1.47x slower                                                   |
| many_optionals                   | 195 us                                                   | 328 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.8 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (3): scimark_fft, async_tree_eager_memoization_tg, logging_simple
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 96.38% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x