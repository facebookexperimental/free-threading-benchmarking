# Results vs. 3.12.6

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.142x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.04x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                   |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.5 ms: 1.15x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate   | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                   |
| tomli_loads          | 957 ms                                                   | 816 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.9 us: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.32 ms: 1.01x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.2 ms: 1.13x faster                                                   |
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.28 ms: 2.24x faster                                                   |
| mdp                              | 1.09 sec                                                 | 507 ms: 2.15x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 242 ms: 2.05x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.64x faster                                                   |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.99 us: 1.41x faster                                                   |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                   |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.4 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.26x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.2 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 58.9 us: 1.20x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.52 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.3 ms: 1.19x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 816 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 957 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.5 ms: 1.15x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.13x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.2 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.0 ms: 1.13x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| thrift                           | 322 us                                                   | 286 us: 1.13x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 48.5 ms: 1.12x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.12x faster                                                   |
| sympy_str                        | 104 ms                                                   | 93.9 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.27 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.9 us: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.0 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.1 ms: 1.08x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 157 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 109 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 945 ns: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 329 ms: 1.00x slower                                                    |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.32 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.05x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.21 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 949 us: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.2 ms: 1.20x slower                                                   |
| many_optionals                   | 195 us                                                   | 237 us: 1.21x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 193 ns: 3.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmark hidden because not significant (1): pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250601-3.15.0a0-cebae97-CLANG/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.142x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.14x