# Results vs. 3.12.6

- fork: python
- ref: 1cdd590cb547597ab64b
- machine: darwin-arm64
- commit hash: 1cdd590
- commit date: 2026-09-24
- overall geometric mean: 1.134x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| docutils       | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 343 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.9 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.3 ms: 1.22x faster                                                   |
| tomli_loads          | 957 ms                                                   | 795 ms: 1.20x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 96.8 us: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.28 ms: 1.16x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.17x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.04x faster                                                   |
| pylint                           | 128 ms                                                   | 56.1 ms: 2.28x faster                                                   |
| mdp                              | 1.09 sec                                                 | 510 ms: 2.14x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.0 us: 1.68x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.67 us: 1.48x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.35 ms: 1.45x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 345 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 144 ms: 1.43x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.8 us: 1.43x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| go                               | 70.0 ms                                                  | 52.1 ms: 1.34x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 343 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 342 ms: 1.30x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 137 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.2 ms: 1.29x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.27x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.0 ms: 1.26x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.4 ns: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.25x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 34.9 ms: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.3 ms: 1.22x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 117 ms: 1.21x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 795 ms: 1.20x faster                                                    |
| pyflate                          | 216 ms                                                   | 180 ms: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.9 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.66 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 983 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                   |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.8 ms: 1.09x faster                                                   |
| fannkuch                         | 176 ms                                                   | 162 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 304 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.43 ms: 1.08x faster                                                   |
| docutils                         | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.4 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.07x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 625 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 96.8 us: 1.06x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.0 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.0 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 489 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.8 ms: 1.02x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 417 us: 1.00x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 837 us: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 135 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                    |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 251 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.28 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.75 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 267 ms: 1.25x slower                                                    |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.37x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 64.9 ms: 1.42x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 104 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.134x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x