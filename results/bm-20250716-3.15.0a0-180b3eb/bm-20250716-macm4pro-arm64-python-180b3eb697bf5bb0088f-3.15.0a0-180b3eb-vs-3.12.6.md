# Results vs. 3.12.6

- fork: python
- ref: 180b3eb697bf5bb0088f
- machine: darwin-arm64
- commit hash: 180b3eb
- commit date: 2025-07-16
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.9 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                   |
| tomli_loads          | 957 ms                                                   | 905 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 64.7 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.9 us: 1.03x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 518 ms: 2.11x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.92 ms: 2.09x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 254 ms: 1.89x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| go                               | 70.0 ms                                                  | 56.3 ms: 1.24x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.8 ns: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                   |
| float                            | 37.9 ms                                                  | 31.3 ms: 1.21x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 45.1 ms: 1.20x faster                                                   |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.8 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.9 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.4 us: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.6 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 905 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 64.7 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.04x faster                                                   |
| sympy_str                        | 104 ms                                                   | 99.9 ms: 1.04x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.9 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.2 ms: 1.02x faster                                                   |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 50.5 ms: 1.01x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.8 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 670 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.02x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| json_dumps                       | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 439 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.3 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 938 us: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.16x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.4 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.6 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (4): pycparser, meteor_contest, genshi_xml, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x