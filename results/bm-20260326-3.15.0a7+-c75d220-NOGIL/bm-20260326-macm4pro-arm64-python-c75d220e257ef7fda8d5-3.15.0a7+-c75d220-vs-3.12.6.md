# Results vs. 3.12.6

- fork: python
- ref: c75d220e257ef7fda8d5
- machine: darwin-arm64
- commit hash: c75d220
- commit date: 2026-03-26
- overall geometric mean: 1.101x faster
- HPT reliability: 99.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.8 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| tomli_loads          | 957 ms                                                   | 858 ms: 1.12x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.77 ms: 1.22x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.10x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 797 us: 2.52x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 604 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 504 us: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.26x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 796 ns: 1.21x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.0 ms: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 59.5 ms: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.37 us: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 858 ms: 1.12x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.11x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.36 us: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                     |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.09x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.5 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.7 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.7 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.9 ms: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.9 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.7 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.8 ms: 1.00x slower                                                    |
| fannkuch                         | 176 ms                                                   | 176 ms: 1.00x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 72.4 us: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.0 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.4 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.3 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.2 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.21x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.77 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.10 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 262 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 568 us: 1.36x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.8 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.8 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (3): json, pprint_safe_repr, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260326-3.15.0a7+-c75d220-NOGIL/bm-20260326-macm4pro-arm64-python-c75d220e257ef7fda8d5-3.15.0a7+-c75d220.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 99.65% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.37x