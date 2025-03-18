# Results vs. 3.12.6

- fork: python
- ref: a936af924efc6e2fb59e
- machine: darwin-arm64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.009x slower
- HPT reliability: 98.35%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| sphinx         | 434 ms                                                   | 431 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.13x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.11x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 56.1 ms: 1.23x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 78.2 ms: 1.44x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 90.4 ms: 1.10x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 58.4 ms: 1.07x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 10.5 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 40.5 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.06 sec: 1.10x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 168 us: 1.21x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 127 us: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.20 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.8 ms: 1.22x slower                                                    |
| mako            | 4.77 ms                                                  | 6.17 ms: 1.29x slower                                                    |
| django_template | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.28 ms: 2.24x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 901 us: 2.23x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 229 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 220 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 237 ms: 1.94x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 476 us: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.0 ms: 1.74x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 243 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| deepcopy                         | 161 us                                                   | 128 us: 1.26x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 830 ns: 1.17x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.13x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 90.4 ms: 1.10x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.4 ms: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 190 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 122 ms: 1.08x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.5 ms: 1.07x faster                                                    |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.37 us: 1.07x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 17.2 us: 1.06x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.06x faster                                                   |
| pylint                           | 128 ms                                                   | 123 ms: 1.04x faster                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 38.1 ms: 1.04x faster                                                    |
| pidigits                         | 161 ms                                                   | 157 ms: 1.02x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.6 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| sphinx                           | 434 ms                                                   | 431 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| comprehensions                   | 9.84 us                                                  | 10.0 us: 1.02x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 40.5 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| go                               | 70.0 ms                                                  | 73.4 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| pyflate                          | 216 ms                                                   | 231 ms: 1.07x slower                                                     |
| regex_compile                    | 54.6 ms                                                  | 58.4 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 345 us: 1.07x slower                                                     |
| raytrace                         | 145 ms                                                   | 157 ms: 1.08x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 58.9 ms: 1.08x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.18 sec: 1.09x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 62.6 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.5 ms: 1.09x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 55.7 ns: 1.09x slower                                                    |
| sqlglot_optimize                 | 23.4 ms                                                  | 25.8 ms: 1.10x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.06 sec: 1.10x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.09 us: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.84 us: 1.10x slower                                                    |
| sqlglot_normalize                | 126 ms                                                   | 139 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 79.1 us: 1.12x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 49.0 ms: 1.13x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 1.95 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.12 ms: 1.14x slower                                                    |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                     |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 69.6 ms: 1.14x slower                                                    |
| sympy_str                        | 104 ms                                                   | 119 ms: 1.15x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 9.25 ms: 1.15x slower                                                    |
| chaos                            | 28.9 ms                                                  | 33.6 ms: 1.16x slower                                                    |
| sqlglot_transpile                | 696 us                                                   | 814 us: 1.17x slower                                                     |
| connected_components             | 201 ms                                                   | 236 ms: 1.17x slower                                                     |
| sqlglot_parse                    | 577 us                                                   | 680 us: 1.18x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 46.0 ms: 1.18x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 25.9 ms: 1.19x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 200 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.49 ms: 1.20x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.11 ms: 1.20x slower                                                    |
| richards                         | 22.4 ms                                                  | 26.9 ms: 1.20x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 168 us: 1.21x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 30.8 ms: 1.21x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.8 ms: 1.22x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 56.1 ms: 1.23x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 127 us: 1.23x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 408 ms: 1.24x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.0 ms: 1.24x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 59.6 ms: 1.25x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 833 ms: 1.25x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.20 ms: 1.26x slower                                                    |
| fannkuch                         | 176 ms                                                   | 222 ms: 1.27x slower                                                     |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 65.7 ms: 1.28x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.17 ms: 1.29x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.94 ms: 1.30x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.0 ms: 1.32x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.53 ms: 1.35x slower                                                    |
| coverage                         | 26.9 ms                                                  | 37.9 ms: 1.41x slower                                                    |
| nbody                            | 54.2 ms                                                  | 78.2 ms: 1.44x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 618 us: 1.48x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.6 ms: 2.73x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (2): bpe_tokeniser, pycparser
Ignored benchmarks (7) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 98.35% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x