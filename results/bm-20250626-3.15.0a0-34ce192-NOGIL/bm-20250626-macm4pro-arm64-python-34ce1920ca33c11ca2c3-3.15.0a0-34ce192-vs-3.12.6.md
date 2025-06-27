# Results vs. 3.12.6

- fork: python
- ref: 34ce1920ca33c11ca2c3
- machine: darwin-arm64
- commit hash: 34ce192
- commit date: 2025-06-26
- overall geometric mean: 1.100x faster
- HPT reliability: 98.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.00 ms: 1.36x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.2 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| tomli_loads          | 957 ms                                                   | 989 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.09x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.66 ms: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| django_template | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| mako            | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.58x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.75 ms: 2.13x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 562 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 484 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.00 ms: 1.36x faster                                                  |
| deepcopy                         | 161 us                                                   | 120 us: 1.35x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 29.4 ms: 1.29x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.89 us: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.4 ms: 1.18x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 836 ns: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 44.9 ns: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                    |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.60 ms: 1.08x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 40.9 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.2 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.2 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.33 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.94 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.02 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.59 us: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 330 us: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.1 us: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.89 us: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 989 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.04x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 347 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 706 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.2 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.6 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.66 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.4 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.3 ms: 1.20x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.74 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 98.07% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x