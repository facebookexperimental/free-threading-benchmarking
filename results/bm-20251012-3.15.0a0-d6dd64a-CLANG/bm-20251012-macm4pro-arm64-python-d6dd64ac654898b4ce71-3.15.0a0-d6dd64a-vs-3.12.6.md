# Results vs. 3.12.6

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 396 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 244 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.5 ms: 1.15x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.7 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.4 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 778 ms: 1.23x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 42.2 ms: 1.22x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 91.2 us: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.08 ms: 1.15x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.7 ms: 1.10x faster                                                   |
| mako            | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 238 ms: 2.08x faster                                                    |
| mdp                              | 1.09 sec                                                 | 527 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 244 ms: 1.97x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.87x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 244 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 102 ms: 1.69x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                    |
| deepcopy                         | 161 us                                                   | 98.5 us: 1.64x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.56x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.90 us: 1.43x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                   |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.38x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 39.3 ns: 1.30x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 778 ms: 1.23x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.2 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.2 ms: 1.21x faster                                                   |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.4 ms: 1.20x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.38 us: 1.18x faster                                                   |
| pyflate                          | 216 ms                                                   | 184 ms: 1.18x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.1 ms: 1.17x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 60.6 us: 1.17x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| pylint                           | 128 ms                                                   | 110 ms: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.5 ms: 1.15x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.08 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.7 ms: 1.15x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 981 ms: 1.14x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.1 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 91.2 us: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.7 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.11x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.7 ms: 1.10x faster                                                   |
| sympy_str                        | 104 ms                                                   | 94.9 ms: 1.10x faster                                                   |
| sphinx                           | 434 ms                                                   | 396 ms: 1.09x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.90 ms: 1.09x faster                                                   |
| thrift                           | 322 us                                                   | 295 us: 1.09x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.2 ms: 1.08x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 616 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                   |
| pycparser                        | 497 ms                                                   | 463 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 397 us: 1.06x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 158 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                    |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 941 ns: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.03x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.4 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                    |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                   |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.09x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.34 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                   |
| many_optionals                   | 195 us                                                   | 358 us: 1.83x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.7 ms: 2.64x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.19x