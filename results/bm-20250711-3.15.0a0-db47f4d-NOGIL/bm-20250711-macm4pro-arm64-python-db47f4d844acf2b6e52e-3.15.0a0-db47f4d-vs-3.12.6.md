# Results vs. 3.12.6

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: darwin-arm64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.096x faster
- HPT reliability: 97.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.0 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.0 ms: 1.01x slower                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 972 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.59 ms: 1.08x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 791 us: 2.54x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.98 ms: 2.08x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.0 ms: 1.98x faster                                                   |
| mdp                              | 1.09 sec                                                 | 574 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| deepcopy                         | 161 us                                                   | 120 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.94 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 815 ns: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| go                               | 70.0 ms                                                  | 60.5 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.7 ns: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.1 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 411 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.04x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.4 ms: 1.03x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.6 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| hexiom                           | 3.04 ms                                                  | 3.03 ms: 1.00x faster                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.0 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 972 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.61 us: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.6 us: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 330 us: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.91 us: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.4 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 700 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.7 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.7 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 55.3 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.59 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.7 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.65 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): sympy_integrate
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 97.13% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x