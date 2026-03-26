# Results vs. 3.12.6

- fork: python
- ref: 8e1469c952fb9db57efd
- machine: darwin-arm64
- commit hash: 8e1469c
- commit date: 2026-03-26
- overall geometric mean: 1.098x faster
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.7 ms: 1.20x faster                                                    |
| tomli_loads          | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.12 ms: 5.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 794 us: 2.53x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.85x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 599 ms: 1.82x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 508 us: 1.63x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.1 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 792 ns: 1.22x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.7 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.32 us: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 59.7 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 850 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.9 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.94 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.4 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.2 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 995 ms: 1.03x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.5 us: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.7 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| thrift                           | 322 us                                                   | 341 us: 1.06x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.7 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.2 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.7 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.53 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.6 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.6 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.75 ms: 1.22x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.07 ms: 1.24x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 569 us: 1.36x slower                                                     |
| many_optionals                   | 195 us                                                   | 269 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (4): html5lib, json, pprint_pformat, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260326-3.15.0a7+-8e1469c-NOGIL/bm-20260326-macm4pro-arm64-python-8e1469c952fb9db57efd-3.15.0a7+-8e1469c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 99.70% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.39x