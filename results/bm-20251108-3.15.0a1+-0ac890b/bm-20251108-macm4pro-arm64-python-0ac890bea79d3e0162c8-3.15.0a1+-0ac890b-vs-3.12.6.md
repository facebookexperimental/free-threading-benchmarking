# Results vs. 3.12.6

- fork: python
- ref: 0ac890bea79d3e0162c8
- machine: darwin-arm64
- commit hash: 0ac890b
- commit date: 2025-11-08
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.3 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.9 ms: 1.11x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.5 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                    |
| tomli_loads          | 957 ms                                                   | 893 ms: 1.07x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.5 us: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.19x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.14x faster                                                     |
| mdp                              | 1.09 sec                                                 | 533 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.53x faster                                                    |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                     |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| go                               | 70.0 ms                                                  | 54.6 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 896 ms: 1.25x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.8 ms: 1.24x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.5 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.15x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.5 ms: 1.13x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.28 us: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.49 us: 1.12x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.2 ms: 1.11x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.9 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 395 ms: 1.10x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.7 us: 1.08x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.7 ms: 1.07x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.9 ms: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 893 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 93.5 ms: 1.07x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.3 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.5 us: 1.04x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 316 us: 1.02x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                    |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                     |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 416 us: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.00x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                     |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.5 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 899 us: 1.08x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.75 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 236 ms: 1.11x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 351 us: 1.80x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.3 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (4): genshi_xml, pprint_pformat, docutils, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251108-3.15.0a1+-0ac890b/bm-20251108-macm4pro-arm64-python-0ac890bea79d3e0162c8-3.15.0a1+-0ac890b.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.20x