# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: darwin-arm64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.208x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 161 ms: 1.41x slower                                           |
| chameleon      | 3.13 ms                                                  | 5.56 ms: 1.78x slower                                          |
| docutils       | 1.02 sec                                                 | 1.20 sec: 1.17x slower                                         |
| html5lib       | 23.0 ms                                                  | 34.1 ms: 1.48x slower                                          |
| sphinx         | 434 ms                                                   | 510 ms: 1.18x slower                                           |
| tornado_http   | 45.1 ms                                                  | 50.6 ms: 1.12x slower                                          |
| Geometric mean | (ref)                                                    | 1.34x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 335 ms: 1.48x faster                                           |
| async_tree_io_tg                 | 480 ms                                                   | 336 ms: 1.43x faster                                           |
| async_tree_eager_io_tg           | 446 ms                                                   | 323 ms: 1.38x faster                                           |
| async_tree_io                    | 459 ms                                                   | 355 ms: 1.29x faster                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 188 ms: 1.23x faster                                           |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.17x faster                                           |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.09x faster                                           |
| async_tree_memoization           | 223 ms                                                   | 205 ms: 1.09x faster                                           |
| async_tree_none                  | 178 ms                                                   | 167 ms: 1.07x faster                                           |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                           |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 142 ms: 1.08x slower                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                           |
| async_generators                 | 206 ms                                                   | 225 ms: 1.09x slower                                           |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                           |
| coroutines                       | 13.6 ms                                                  | 17.1 ms: 1.26x slower                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 47.1 ms: 1.46x slower                                          |
| async_tree_eager                 | 45.6 ms                                                  | 69.0 ms: 1.51x slower                                          |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                           |
| float          | 37.9 ms                                                  | 59.6 ms: 1.57x slower                                          |
| nbody          | 54.2 ms                                                  | 106 ms: 1.95x slower                                           |
| Geometric mean | (ref)                                                    | 1.46x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                          |
| regex_effbot   | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                          |
| regex_v8       | 9.59 ms                                                  | 10.5 ms: 1.10x slower                                          |
| regex_compile  | 54.6 ms                                                  | 82.1 ms: 1.50x slower                                          |
| Geometric mean | (ref)                                                    | 1.09x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_parse      | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                          |
| xml_etree_iterparse  | 51.6 ms                                                  | 47.7 ms: 1.08x faster                                          |
| json_loads           | 10.9 us                                                  | 12.0 us: 1.10x slower                                          |
| xml_etree_generate   | 38.9 ms                                                  | 44.9 ms: 1.16x slower                                          |
| json_dumps           | 4.26 ms                                                  | 5.31 ms: 1.25x slower                                          |
| tomli_loads          | 957 ms                                                   | 1.33 sec: 1.39x slower                                         |
| xml_etree_process    | 26.7 ms                                                  | 38.7 ms: 1.45x slower                                          |
| pickle_pure_python   | 139 us                                                   | 224 us: 1.61x slower                                           |
| unpickle_pure_python | 103 us                                                   | 167 us: 1.62x slower                                           |
| Geometric mean       | (ref)                                                    | 1.23x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                          |
| python_startup_no_site | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                          |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 7.44 ms: 1.56x slower                                          |
| genshi_xml      | 21.8 ms                                                  | 34.4 ms: 1.58x slower                                          |
| genshi_text     | 10.5 ms                                                  | 16.8 ms: 1.60x slower                                          |
| django_template | 13.6 ms                                                  | 23.5 ms: 1.72x slower                                          |
| Geometric mean  | (ref)                                                    | 1.61x slower                                                   |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.07 ms: 2.29x faster                                          |
| async_tree_eager_io              | 496 ms                                                   | 335 ms: 1.48x faster                                           |
| async_tree_io_tg                 | 480 ms                                                   | 336 ms: 1.43x faster                                           |
| async_tree_eager_io_tg           | 446 ms                                                   | 323 ms: 1.38x faster                                           |
| create_gc_cycles                 | 830 us                                                   | 617 us: 1.34x faster                                           |
| async_tree_io                    | 459 ms                                                   | 355 ms: 1.29x faster                                           |
| async_tree_memoization_tg        | 231 ms                                                   | 188 ms: 1.23x faster                                           |
| gc_traversal                     | 2.01 ms                                                  | 1.65 ms: 1.22x faster                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 288 ms: 1.17x faster                                           |
| xml_etree_parse                  | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                          |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                           |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.09x faster                                           |
| async_tree_memoization           | 223 ms                                                   | 205 ms: 1.09x faster                                           |
| xml_etree_iterparse              | 51.6 ms                                                  | 47.7 ms: 1.08x faster                                          |
| regex_dna                        | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                          |
| regex_effbot                     | 1.67 ms                                                  | 1.55 ms: 1.08x faster                                          |
| async_tree_none                  | 178 ms                                                   | 167 ms: 1.07x faster                                           |
| sqlite_synth                     | 967 ns                                                   | 947 ns: 1.02x faster                                           |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                           |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                           |
| k_core                           | 1.12 sec                                                 | 1.13 sec: 1.01x slower                                         |
| pathlib                          | 12.4 ms                                                  | 12.5 ms: 1.02x slower                                          |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.06x slower                                          |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                           |
| async_tree_eager_memoization     | 132 ms                                                   | 142 ms: 1.08x slower                                           |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 250 ms: 1.08x slower                                           |
| async_generators                 | 206 ms                                                   | 225 ms: 1.09x slower                                           |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                           |
| regex_v8                         | 9.59 ms                                                  | 10.5 ms: 1.10x slower                                          |
| json_loads                       | 10.9 us                                                  | 12.0 us: 1.10x slower                                          |
| json                             | 1.93 ms                                                  | 2.14 ms: 1.11x slower                                          |
| tornado_http                     | 45.1 ms                                                  | 50.6 ms: 1.12x slower                                          |
| xml_etree_generate               | 38.9 ms                                                  | 44.9 ms: 1.16x slower                                          |
| python_startup                   | 8.01 ms                                                  | 9.29 ms: 1.16x slower                                          |
| python_startup_no_site           | 5.71 ms                                                  | 6.61 ms: 1.16x slower                                          |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.60 sec: 1.16x slower                                         |
| pylint                           | 128 ms                                                   | 149 ms: 1.16x slower                                           |
| docutils                         | 1.02 sec                                                 | 1.20 sec: 1.17x slower                                         |
| sphinx                           | 434 ms                                                   | 510 ms: 1.18x slower                                           |
| shortest_path                    | 219 ms                                                   | 260 ms: 1.19x slower                                           |
| mdp                              | 1.09 sec                                                 | 1.30 sec: 1.19x slower                                         |
| comprehensions                   | 9.84 us                                                  | 11.8 us: 1.20x slower                                          |
| connected_components             | 201 ms                                                   | 247 ms: 1.23x slower                                           |
| scimark_fft                      | 142 ms                                                   | 176 ms: 1.24x slower                                           |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.58 ms: 1.24x slower                                          |
| json_dumps                       | 4.26 ms                                                  | 5.31 ms: 1.25x slower                                          |
| meteor_contest                   | 47.7 ms                                                  | 59.8 ms: 1.25x slower                                          |
| nqueens                          | 43.5 ms                                                  | 54.5 ms: 1.25x slower                                          |
| generators                       | 21.9 ms                                                  | 27.5 ms: 1.25x slower                                          |
| crypto_pyaes                     | 38.8 ms                                                  | 48.8 ms: 1.26x slower                                          |
| coroutines                       | 13.6 ms                                                  | 17.1 ms: 1.26x slower                                          |
| pycparser                        | 497 ms                                                   | 644 ms: 1.29x slower                                           |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                           |
| sympy_integrate                  | 8.02 ms                                                  | 10.7 ms: 1.33x slower                                          |
| fannkuch                         | 176 ms                                                   | 235 ms: 1.34x slower                                           |
| typing_runtime_protocols         | 71.0 us                                                  | 96.9 us: 1.37x slower                                          |
| tomli_loads                      | 957 ms                                                   | 1.33 sec: 1.39x slower                                         |
| dulwich_log                      | 21.3 ms                                                  | 29.5 ms: 1.39x slower                                          |
| sqlalchemy_declarative           | 46.8 ms                                                  | 65.1 ms: 1.39x slower                                          |
| coverage                         | 26.9 ms                                                  | 37.7 ms: 1.40x slower                                          |
| 2to3                             | 114 ms                                                   | 161 ms: 1.41x slower                                           |
| pyflate                          | 216 ms                                                   | 307 ms: 1.42x slower                                           |
| deepcopy_reduce                  | 1.46 us                                                  | 2.08 us: 1.42x slower                                          |
| sqlalchemy_imperative            | 5.17 ms                                                  | 7.41 ms: 1.43x slower                                          |
| thrift                           | 322 us                                                   | 464 us: 1.44x slower                                           |
| xml_etree_process                | 26.7 ms                                                  | 38.7 ms: 1.45x slower                                          |
| bench_thread_pool                | 419 us                                                   | 606 us: 1.45x slower                                           |
| async_tree_eager_tg              | 32.1 ms                                                  | 47.1 ms: 1.46x slower                                          |
| telco                            | 2.61 ms                                                  | 3.83 ms: 1.47x slower                                          |
| deepcopy_memo                    | 18.3 us                                                  | 26.9 us: 1.47x slower                                          |
| spectral_norm                    | 54.4 ms                                                  | 80.1 ms: 1.47x slower                                          |
| html5lib                         | 23.0 ms                                                  | 34.1 ms: 1.48x slower                                          |
| deepcopy                         | 161 us                                                   | 241 us: 1.49x slower                                           |
| regex_compile                    | 54.6 ms                                                  | 82.1 ms: 1.50x slower                                          |
| sqlglot_normalize                | 126 ms                                                   | 190 ms: 1.51x slower                                           |
| async_tree_eager                 | 45.6 ms                                                  | 69.0 ms: 1.51x slower                                          |
| sympy_str                        | 104 ms                                                   | 159 ms: 1.53x slower                                           |
| logging_silent                   | 50.9 ns                                                  | 78.5 ns: 1.54x slower                                          |
| sqlglot_optimize                 | 23.4 ms                                                  | 36.2 ms: 1.54x slower                                          |
| mako                             | 4.77 ms                                                  | 7.44 ms: 1.56x slower                                          |
| richards                         | 22.4 ms                                                  | 35.1 ms: 1.57x slower                                          |
| float                            | 37.9 ms                                                  | 59.6 ms: 1.57x slower                                          |
| scimark_monte_carlo              | 32.2 ms                                                  | 50.7 ms: 1.57x slower                                          |
| genshi_xml                       | 21.8 ms                                                  | 34.4 ms: 1.58x slower                                          |
| genshi_text                      | 10.5 ms                                                  | 16.8 ms: 1.60x slower                                          |
| pickle_pure_python               | 139 us                                                   | 224 us: 1.61x slower                                           |
| logging_format                   | 2.80 us                                                  | 4.54 us: 1.62x slower                                          |
| unpickle_pure_python             | 103 us                                                   | 167 us: 1.62x slower                                           |
| scimark_sor                      | 61.0 ms                                                  | 98.9 ms: 1.62x slower                                          |
| logging_simple                   | 2.57 us                                                  | 4.18 us: 1.63x slower                                          |
| raytrace                         | 145 ms                                                   | 237 ms: 1.63x slower                                           |
| chaos                            | 28.9 ms                                                  | 47.7 ms: 1.65x slower                                          |
| richards_super                   | 25.4 ms                                                  | 41.9 ms: 1.65x slower                                          |
| hexiom                           | 3.04 ms                                                  | 5.02 ms: 1.65x slower                                          |
| sympy_sum                        | 57.6 ms                                                  | 96.1 ms: 1.67x slower                                          |
| pprint_safe_repr                 | 328 ms                                                   | 554 ms: 1.69x slower                                           |
| pprint_pformat                   | 665 ms                                                   | 1.12 sec: 1.69x slower                                         |
| django_template                  | 13.6 ms                                                  | 23.5 ms: 1.72x slower                                          |
| sympy_expand                     | 167 ms                                                   | 293 ms: 1.76x slower                                           |
| chameleon                        | 3.13 ms                                                  | 5.56 ms: 1.78x slower                                          |
| sqlglot_transpile                | 696 us                                                   | 1.27 ms: 1.83x slower                                          |
| go                               | 70.0 ms                                                  | 130 ms: 1.86x slower                                           |
| scimark_lu                       | 51.3 ms                                                  | 95.9 ms: 1.87x slower                                          |
| sqlglot_parse                    | 577 us                                                   | 1.10 ms: 1.91x slower                                          |
| deltablue                        | 1.73 ms                                                  | 3.36 ms: 1.95x slower                                          |
| nbody                            | 54.2 ms                                                  | 106 ms: 1.95x slower                                           |
| Geometric mean                   | (ref)                                                    | 1.27x slower                                                   |
Ignored benchmarks (3) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: dask, djangocms, gevent_hub

- Geometric mean (including insignificant results): 1.208x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.10x