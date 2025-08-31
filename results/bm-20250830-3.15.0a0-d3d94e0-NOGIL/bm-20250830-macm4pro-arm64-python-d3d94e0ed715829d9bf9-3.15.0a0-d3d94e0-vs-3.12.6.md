# Results vs. 3.12.6

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.078x faster
- HPT reliability: 91.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 972 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.06 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.86 ms: 1.23x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 793 us: 2.53x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.2 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 594 ms: 1.84x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 499 us: 1.66x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 122 us: 1.32x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.38 us: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 827 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.4 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 62.8 ms: 1.11x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 46.1 ns: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.6 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.26 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.7 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 53.8 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 533 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.12 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.01x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 972 ms: 1.02x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.85 us: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.9 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 74.5 us: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 347 ms: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.5 ms: 1.12x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.4 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.6 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.86 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.06 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 592 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| many_optionals                   | 195 us                                                   | 334 us: 1.71x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (3): logging_simple, async_tree_eager_memoization_tg, nqueens
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0-NOGIL/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 91.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x