# Results vs. 3.12.6

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.146x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.04x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.88x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.87 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.9 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| nbody          | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.53 ms: 1.09x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                   |
| tomli_loads          | 957 ms                                                   | 805 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 33.2 ms: 1.17x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 135 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.47 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.07 ms: 1.06x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.48 ms: 1.11x faster                                                   |
| mako            | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                   |
| django_template | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.00 ms: 2.31x faster                                                   |
| mdp                              | 1.09 sec                                                 | 513 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 243 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.88x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                    |
| deepcopy                         | 161 us                                                   | 99.3 us: 1.63x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.1 ms: 1.56x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.55x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.87 ms: 1.38x faster                                                   |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.37x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.25 us: 1.36x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                   |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.1 ms: 1.24x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.8 ms: 1.23x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.40 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 805 ms: 1.19x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.4 ms: 1.19x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.56 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 952 ms: 1.17x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.2 ms: 1.17x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.5 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.1 ms: 1.13x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.9 us: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.12x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 48.8 ms: 1.11x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.7 ms: 1.11x faster                                                   |
| thrift                           | 322 us                                                   | 291 us: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.48 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| nbody                            | 54.2 ms                                                  | 49.2 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| sympy_str                        | 104 ms                                                   | 94.8 ms: 1.10x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 52.8 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.53 ms: 1.09x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.98 ms: 1.05x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                    |
| 2to3                             | 114 ms                                                   | 109 ms: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.03x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 937 ns: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 135 us: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 201 ms: 1.00x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 421 us: 1.00x slower                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| django_template                  | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.47 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.07 ms: 1.06x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.6 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                   |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.9 ms: 2.64x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 194 ns: 3.82x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250510-3.15.0a0-1a87b6e-CLANG/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.146x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.14x