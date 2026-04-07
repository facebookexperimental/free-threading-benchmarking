# Results vs. 3.12.6

- fork: python
- ref: 8a73478fedaee54a409f
- machine: darwin-arm64
- commit hash: 8a73478
- commit date: 2026-04-06
- overall geometric mean: 1.116x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| docutils       | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.7 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.0 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 55.9 ms: 1.22x faster                                                    |
| tomli_loads          | 957 ms                                                   | 858 ms: 1.12x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.00 ms: 5.19x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 774 us: 2.60x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.91x faster                                                     |
| mdp                              | 1.09 sec                                                 | 591 ms: 1.85x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 492 us: 1.69x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.1 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 259 ms: 1.29x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 776 ns: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 55.9 ms: 1.22x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.22 us: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.7 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.8 ns: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.30 us: 1.12x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 858 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                     |
| pycparser                        | 497 ms                                                   | 451 ms: 1.10x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.54 us: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.6 ms: 1.10x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.3 ms: 1.09x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.1 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 180 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| sphinx                           | 434 ms                                                   | 414 ms: 1.05x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 323 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.96 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 660 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.7 ms: 1.00x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.6 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.2 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 72.6 us: 1.02x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.5 ms: 1.02x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.4 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.0 ms: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.04x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 43.8 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.14x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 54.8 ms: 1.15x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.64 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 255 us: 1.30x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 565 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 37.6 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.0 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260406-3.15.0a7+-8a73478-NOGIL/bm-20260406-macm4pro-arm64-python-8a73478fedaee54a409f-3.15.0a7+-8a73478.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.38x