# Results vs. 3.12.6

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.148x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.06x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                                   |
| sphinx         | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 245 ms: 1.96x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 244 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.2 ms: 2.62x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.74 ms: 1.04x slower                                                   |
| regex_v8       | 9.59 ms                                                  | 11.0 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 783 ms: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 91.7 us: 1.12x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                   |
| mako            | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 517 ms: 2.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 245 ms: 1.96x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 244 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| deepcopy                         | 161 us                                                   | 96.0 us: 1.68x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.44x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.88 us: 1.43x faster                                                   |
| go                               | 70.0 ms                                                  | 50.5 ms: 1.39x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 38.8 ns: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.0 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 783 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.22x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.7 ms: 1.22x faster                                                   |
| async_generators                 | 206 ms                                                   | 170 ms: 1.22x faster                                                    |
| pylint                           | 128 ms                                                   | 105 ms: 1.22x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.1 ms: 1.22x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.2 ms: 1.21x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.56 ms: 1.19x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 949 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 21.7 ms: 1.17x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 60.8 us: 1.17x faster                                                   |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 123 ms: 1.15x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 44.8 ms: 1.14x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.7 ms: 1.14x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 91.7 us: 1.12x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.16 ms: 1.12x faster                                                   |
| sympy_str                        | 104 ms                                                   | 93.9 ms: 1.11x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 398 ms: 1.09x faster                                                    |
| thrift                           | 322 us                                                   | 296 us: 1.09x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 52.9 ms: 1.09x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 620 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 467 ms: 1.06x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 157 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                    |
| 2to3                             | 114 ms                                                   | 108 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.8 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.1 ms: 1.04x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 403 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 933 ns: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.74 ms: 1.04x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 911 us: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 243 ms: 1.15x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 11.0 ms: 1.15x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 309 us: 1.58x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.2 ms: 2.62x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, shortest_path
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250926-3.15.0a0-48d0d0d-CLANG/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.148x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.14x