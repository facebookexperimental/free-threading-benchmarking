# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.073x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib       | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                   |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 258 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 261 ms: 1.76x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 263 ms: 1.70x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 192 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.7 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 135 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 256 ms: 1.20x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.84x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.7 ms: 1.13x faster                                                   |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| pidigits       | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.8 ms: 1.10x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                   |
| tomli_loads          | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.54 ms: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.3 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 10.2 ms: 2.05x faster                                                   |
| mdp                              | 1.09 sec                                                 | 537 ms: 2.03x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 258 ms: 1.86x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 261 ms: 1.76x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 263 ms: 1.70x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                    |
| deepcopy                         | 161 us                                                   | 114 us: 1.41x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.5 us: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.51 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 274 ms: 1.22x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.7 ms: 1.19x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.8 ms: 1.18x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.0 ns: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| float                            | 37.9 ms                                                  | 33.7 ms: 1.13x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 857 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.8 ms: 1.10x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 65.1 us: 1.09x faster                                                   |
| go                               | 70.0 ms                                                  | 64.7 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.3 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| async_generators                 | 206 ms                                                   | 192 ms: 1.08x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 628 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.5 ms: 1.06x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.7 ms: 1.04x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 43.7 ms: 1.04x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.7 ms: 1.03x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.83 ms: 1.02x faster                                                   |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.70 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                    |
| sympy_str                        | 104 ms                                                   | 104 ms: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 58.1 ms: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.3 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.03x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.3 ms: 1.05x slower                                                   |
| pycparser                        | 497 ms                                                   | 525 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| pidigits                         | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.14 ms: 1.06x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.54 ms: 1.06x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| connected_components             | 201 ms                                                   | 216 ms: 1.08x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.08x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 25.4 ms: 1.10x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.1 ms: 1.18x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 982 us: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 135 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 256 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.5 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 264 us: 1.35x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.84x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (4): json, crypto_pyaes, sqlite_synth, regex_dna
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da-JIT/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x