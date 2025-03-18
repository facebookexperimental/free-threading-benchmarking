# Results vs. base

- fork: python
- ref: v3.13.0rc2
- machine: darwin-arm64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.265x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                                                                    | 161 ms: 1.45x slower                                                                                            |
| chameleon      | 2.99 ms                                                                                                   | 5.56 ms: 1.86x slower                                                                                           |
| docutils       | 1.05 sec                                                                                                  | 1.20 sec: 1.14x slower                                                                                          |
| html5lib       | 23.1 ms                                                                                                   | 34.1 ms: 1.47x slower                                                                                           |
| sphinx         | 409 ms                                                                                                    | 510 ms: 1.25x slower                                                                                            |
| tornado_http   | 43.2 ms                                                                                                   | 50.6 ms: 1.17x slower                                                                                           |
| Geometric mean | (ref)                                                                                                     | 1.37x slower                                                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                                                                    | 323 ms: 1.61x faster                                                                                            |
| async_tree_eager_io              | 525 ms                                                                                                    | 335 ms: 1.57x faster                                                                                            |
| async_tree_io_tg                 | 405 ms                                                                                                    | 336 ms: 1.21x faster                                                                                            |
| async_tree_io                    | 386 ms                                                                                                    | 355 ms: 1.09x faster                                                                                            |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                                                                    | 288 ms: 1.05x faster                                                                                            |
| asyncio_websockets               | 194 ms                                                                                                    | 189 ms: 1.02x faster                                                                                            |
| async_tree_cpu_io_mixed          | 294 ms                                                                                                    | 307 ms: 1.04x slower                                                                                            |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                                                                    | 229 ms: 1.10x slower                                                                                            |
| async_tree_none_tg               | 133 ms                                                                                                    | 147 ms: 1.11x slower                                                                                            |
| async_tree_memoization           | 184 ms                                                                                                    | 205 ms: 1.11x slower                                                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                    | 250 ms: 1.11x slower                                                                                            |
| async_generators                 | 193 ms                                                                                                    | 225 ms: 1.16x slower                                                                                            |
| async_tree_eager_memoization     | 122 ms                                                                                                    | 142 ms: 1.17x slower                                                                                            |
| async_tree_none                  | 142 ms                                                                                                    | 167 ms: 1.17x slower                                                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                                                                    | 123 ms: 1.20x slower                                                                                            |
| coroutines                       | 10.8 ms                                                                                                   | 17.1 ms: 1.59x slower                                                                                           |
| async_tree_eager                 | 43.2 ms                                                                                                   | 69.0 ms: 1.60x slower                                                                                           |
| async_tree_eager_tg              | 28.9 ms                                                                                                   | 47.1 ms: 1.63x slower                                                                                           |
| Geometric mean                   | (ref)                                                                                                     | 1.07x slower                                                                                                    |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                                                                    | 163 ms: 1.02x faster                                                                                            |
| float          | 31.4 ms                                                                                                   | 59.6 ms: 1.90x slower                                                                                           |
| nbody          | 42.5 ms                                                                                                   | 106 ms: 2.49x slower                                                                                            |
| Geometric mean | (ref)                                                                                                     | 1.67x slower                                                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                                                                   | 1.55 ms: 1.04x faster                                                                                           |
| regex_dna      | 94.6 ms                                                                                                   | 92.5 ms: 1.02x faster                                                                                           |
| regex_v8       | 10.7 ms                                                                                                   | 10.5 ms: 1.02x faster                                                                                           |
| regex_compile  | 47.9 ms                                                                                                   | 82.1 ms: 1.71x slower                                                                                           |
| Geometric mean | (ref)                                                                                                     | 1.12x slower                                                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 62.4 ms                                                                                                   | 57.9 ms: 1.08x faster                                                                                           |
| xml_etree_iterparse  | 46.1 ms                                                                                                   | 47.7 ms: 1.04x slower                                                                                           |
| json_loads           | 10.8 us                                                                                                   | 12.0 us: 1.11x slower                                                                                           |
| json_dumps           | 4.65 ms                                                                                                   | 5.31 ms: 1.14x slower                                                                                           |
| xml_etree_generate   | 35.8 ms                                                                                                   | 44.9 ms: 1.26x slower                                                                                           |
| tomli_loads          | 1000 ms                                                                                                   | 1.33 sec: 1.33x slower                                                                                          |
| xml_etree_process    | 25.4 ms                                                                                                   | 38.7 ms: 1.52x slower                                                                                           |
| unpickle_pure_python | 99.5 us                                                                                                   | 167 us: 1.68x slower                                                                                            |
| pickle_pure_python   | 130 us                                                                                                    | 224 us: 1.72x slower                                                                                            |
| Geometric mean       | (ref)                                                                                                     | 1.28x slower                                                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|------------------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                                                                   | 9.29 ms: 1.08x slower                                                                                           |
| python_startup_no_site | 5.95 ms                                                                                                   | 6.61 ms: 1.11x slower                                                                                           |
| Geometric mean         | (ref)                                                                                                     | 1.09x slower                                                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|-----------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                                                                   | 34.4 ms: 1.61x slower                                                                                           |
| genshi_text     | 9.97 ms                                                                                                   | 16.8 ms: 1.68x slower                                                                                           |
| mako            | 4.41 ms                                                                                                   | 7.44 ms: 1.69x slower                                                                                           |
| django_template | 12.5 ms                                                                                                   | 23.5 ms: 1.88x slower                                                                                           |
| Geometric mean  | (ref)                                                                                                     | 1.71x slower                                                                                                    |

All benchmarks:
===============

| Benchmark                        | results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json | results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json |
|----------------------------------|:---------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                                                                    | 323 ms: 1.61x faster                                                                                            |
| create_gc_cycles                 | 993 us                                                                                                    | 617 us: 1.61x faster                                                                                            |
| async_tree_eager_io              | 525 ms                                                                                                    | 335 ms: 1.57x faster                                                                                            |
| k_core                           | 1.46 sec                                                                                                  | 1.13 sec: 1.29x faster                                                                                          |
| gc_traversal                     | 2.04 ms                                                                                                   | 1.65 ms: 1.24x faster                                                                                           |
| async_tree_io_tg                 | 405 ms                                                                                                    | 336 ms: 1.21x faster                                                                                            |
| async_tree_io                    | 386 ms                                                                                                    | 355 ms: 1.09x faster                                                                                            |
| xml_etree_parse                  | 62.4 ms                                                                                                   | 57.9 ms: 1.08x faster                                                                                           |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                                                                    | 288 ms: 1.05x faster                                                                                            |
| regex_effbot                     | 1.61 ms                                                                                                   | 1.55 ms: 1.04x faster                                                                                           |
| asyncio_websockets               | 194 ms                                                                                                    | 189 ms: 1.02x faster                                                                                            |
| regex_dna                        | 94.6 ms                                                                                                   | 92.5 ms: 1.02x faster                                                                                           |
| pidigits                         | 166 ms                                                                                                    | 163 ms: 1.02x faster                                                                                            |
| regex_v8                         | 10.7 ms                                                                                                   | 10.5 ms: 1.02x faster                                                                                           |
| xml_etree_iterparse              | 46.1 ms                                                                                                   | 47.7 ms: 1.04x slower                                                                                           |
| async_tree_cpu_io_mixed          | 294 ms                                                                                                    | 307 ms: 1.04x slower                                                                                            |
| python_startup                   | 8.63 ms                                                                                                   | 9.29 ms: 1.08x slower                                                                                           |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                                                                    | 229 ms: 1.10x slower                                                                                            |
| json                             | 1.94 ms                                                                                                   | 2.14 ms: 1.10x slower                                                                                           |
| json_loads                       | 10.8 us                                                                                                   | 12.0 us: 1.11x slower                                                                                           |
| async_tree_none_tg               | 133 ms                                                                                                    | 147 ms: 1.11x slower                                                                                            |
| python_startup_no_site           | 5.95 ms                                                                                                   | 6.61 ms: 1.11x slower                                                                                           |
| async_tree_memoization           | 184 ms                                                                                                    | 205 ms: 1.11x slower                                                                                            |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                    | 250 ms: 1.11x slower                                                                                            |
| bench_mp_pool                    | 37.8 ms                                                                                                   | 42.3 ms: 1.12x slower                                                                                           |
| pathlib                          | 11.1 ms                                                                                                   | 12.5 ms: 1.13x slower                                                                                           |
| json_dumps                       | 4.65 ms                                                                                                   | 5.31 ms: 1.14x slower                                                                                           |
| docutils                         | 1.05 sec                                                                                                  | 1.20 sec: 1.14x slower                                                                                          |
| shortest_path                    | 225 ms                                                                                                    | 260 ms: 1.16x slower                                                                                            |
| async_generators                 | 193 ms                                                                                                    | 225 ms: 1.16x slower                                                                                            |
| async_tree_eager_memoization     | 122 ms                                                                                                    | 142 ms: 1.17x slower                                                                                            |
| tornado_http                     | 43.2 ms                                                                                                   | 50.6 ms: 1.17x slower                                                                                           |
| async_tree_none                  | 142 ms                                                                                                    | 167 ms: 1.17x slower                                                                                            |
| connected_components             | 208 ms                                                                                                    | 247 ms: 1.19x slower                                                                                            |
| async_tree_eager_memoization_tg  | 103 ms                                                                                                    | 123 ms: 1.20x slower                                                                                            |
| coverage                         | 31.2 ms                                                                                                   | 37.7 ms: 1.21x slower                                                                                           |
| bpe_tokeniser                    | 2.13 sec                                                                                                  | 2.60 sec: 1.22x slower                                                                                          |
| mdp                              | 1.06 sec                                                                                                  | 1.30 sec: 1.23x slower                                                                                          |
| sphinx                           | 409 ms                                                                                                    | 510 ms: 1.25x slower                                                                                            |
| meteor_contest                   | 47.9 ms                                                                                                   | 59.8 ms: 1.25x slower                                                                                           |
| telco                            | 3.07 ms                                                                                                   | 3.83 ms: 1.25x slower                                                                                           |
| xml_etree_generate               | 35.8 ms                                                                                                   | 44.9 ms: 1.26x slower                                                                                           |
| many_optionals                   | 200 us                                                                                                    | 259 us: 1.29x slower                                                                                            |
| fannkuch                         | 179 ms                                                                                                    | 235 ms: 1.31x slower                                                                                            |
| tomli_loads                      | 1000 ms                                                                                                   | 1.33 sec: 1.33x slower                                                                                          |
| pycparser                        | 470 ms                                                                                                    | 644 ms: 1.37x slower                                                                                            |
| pyflate                          | 222 ms                                                                                                    | 307 ms: 1.38x slower                                                                                            |
| pylint                           | 106 ms                                                                                                    | 149 ms: 1.41x slower                                                                                            |
| scimark_fft                      | 124 ms                                                                                                    | 176 ms: 1.42x slower                                                                                            |
| sympy_integrate                  | 7.53 ms                                                                                                   | 10.7 ms: 1.42x slower                                                                                           |
| 2to3                             | 112 ms                                                                                                    | 161 ms: 1.45x slower                                                                                            |
| subparsers                       | 6.26 ms                                                                                                   | 9.07 ms: 1.45x slower                                                                                           |
| scimark_sparse_mat_mult          | 1.78 ms                                                                                                   | 2.58 ms: 1.45x slower                                                                                           |
| crypto_pyaes                     | 33.6 ms                                                                                                   | 48.8 ms: 1.45x slower                                                                                           |
| nqueens                          | 37.2 ms                                                                                                   | 54.5 ms: 1.46x slower                                                                                           |
| sqlalchemy_declarative           | 44.4 ms                                                                                                   | 65.1 ms: 1.47x slower                                                                                           |
| bench_thread_pool                | 412 us                                                                                                    | 606 us: 1.47x slower                                                                                            |
| html5lib                         | 23.1 ms                                                                                                   | 34.1 ms: 1.47x slower                                                                                           |
| sqlalchemy_imperative            | 5.00 ms                                                                                                   | 7.41 ms: 1.48x slower                                                                                           |
| dulwich_log                      | 19.8 ms                                                                                                   | 29.5 ms: 1.49x slower                                                                                           |
| typing_runtime_protocols         | 64.6 us                                                                                                   | 96.9 us: 1.50x slower                                                                                           |
| thrift                           | 309 us                                                                                                    | 464 us: 1.50x slower                                                                                            |
| xml_etree_process                | 25.4 ms                                                                                                   | 38.7 ms: 1.52x slower                                                                                           |
| scimark_sor                      | 64.0 ms                                                                                                   | 98.9 ms: 1.55x slower                                                                                           |
| richards                         | 22.1 ms                                                                                                   | 35.1 ms: 1.59x slower                                                                                           |
| coroutines                       | 10.8 ms                                                                                                   | 17.1 ms: 1.59x slower                                                                                           |
| async_tree_eager                 | 43.2 ms                                                                                                   | 69.0 ms: 1.60x slower                                                                                           |
| deepcopy_reduce                  | 1.30 us                                                                                                   | 2.08 us: 1.61x slower                                                                                           |
| genshi_xml                       | 21.4 ms                                                                                                   | 34.4 ms: 1.61x slower                                                                                           |
| async_tree_eager_tg              | 28.9 ms                                                                                                   | 47.1 ms: 1.63x slower                                                                                           |
| sqlglot_optimize                 | 22.2 ms                                                                                                   | 36.2 ms: 1.63x slower                                                                                           |
| deepcopy_memo                    | 16.5 us                                                                                                   | 26.9 us: 1.63x slower                                                                                           |
| sqlglot_normalize                | 116 ms                                                                                                    | 190 ms: 1.63x slower                                                                                            |
| deepcopy                         | 145 us                                                                                                    | 241 us: 1.66x slower                                                                                            |
| sympy_str                        | 95.5 ms                                                                                                   | 159 ms: 1.67x slower                                                                                            |
| unpickle_pure_python             | 99.5 us                                                                                                   | 167 us: 1.68x slower                                                                                            |
| genshi_text                      | 9.97 ms                                                                                                   | 16.8 ms: 1.68x slower                                                                                           |
| mako                             | 4.41 ms                                                                                                   | 7.44 ms: 1.69x slower                                                                                           |
| scimark_monte_carlo              | 29.9 ms                                                                                                   | 50.7 ms: 1.69x slower                                                                                           |
| richards_super                   | 24.7 ms                                                                                                   | 41.9 ms: 1.70x slower                                                                                           |
| regex_compile                    | 47.9 ms                                                                                                   | 82.1 ms: 1.71x slower                                                                                           |
| pprint_safe_repr                 | 322 ms                                                                                                    | 554 ms: 1.72x slower                                                                                            |
| pickle_pure_python               | 130 us                                                                                                    | 224 us: 1.72x slower                                                                                            |
| pprint_pformat                   | 650 ms                                                                                                    | 1.12 sec: 1.73x slower                                                                                          |
| comprehensions                   | 6.80 us                                                                                                   | 11.8 us: 1.73x slower                                                                                           |
| generators                       | 15.7 ms                                                                                                   | 27.5 ms: 1.75x slower                                                                                           |
| hexiom                           | 2.85 ms                                                                                                   | 5.02 ms: 1.76x slower                                                                                           |
| go                               | 72.6 ms                                                                                                   | 130 ms: 1.80x slower                                                                                            |
| spectral_norm                    | 43.7 ms                                                                                                   | 80.1 ms: 1.83x slower                                                                                           |
| sympy_sum                        | 52.3 ms                                                                                                   | 96.1 ms: 1.84x slower                                                                                           |
| sympy_expand                     | 159 ms                                                                                                    | 293 ms: 1.84x slower                                                                                            |
| logging_format                   | 2.45 us                                                                                                   | 4.54 us: 1.86x slower                                                                                           |
| chameleon                        | 2.99 ms                                                                                                   | 5.56 ms: 1.86x slower                                                                                           |
| logging_simple                   | 2.24 us                                                                                                   | 4.18 us: 1.87x slower                                                                                           |
| django_template                  | 12.5 ms                                                                                                   | 23.5 ms: 1.88x slower                                                                                           |
| float                            | 31.4 ms                                                                                                   | 59.6 ms: 1.90x slower                                                                                           |
| logging_silent                   | 40.6 ns                                                                                                   | 78.5 ns: 1.93x slower                                                                                           |
| chaos                            | 24.3 ms                                                                                                   | 47.7 ms: 1.97x slower                                                                                           |
| sqlglot_transpile                | 637 us                                                                                                    | 1.27 ms: 2.00x slower                                                                                           |
| sqlglot_parse                    | 519 us                                                                                                    | 1.10 ms: 2.12x slower                                                                                           |
| raytrace                         | 109 ms                                                                                                    | 237 ms: 2.18x slower                                                                                            |
| scimark_lu                       | 42.8 ms                                                                                                   | 95.9 ms: 2.24x slower                                                                                           |
| deltablue                        | 1.45 ms                                                                                                   | 3.36 ms: 2.32x slower                                                                                           |
| nbody                            | 42.5 ms                                                                                                   | 106 ms: 2.49x slower                                                                                            |
| Geometric mean                   | (ref)                                                                                                     | 1.37x slower                                                                                                    |

Benchmark hidden because not significant (2): sqlite_synth, async_tree_memoization_tg
Ignored benchmarks (3) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: dask, djangocms, gevent_hub

- Geometric mean (including insignificant results): 1.265x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.20x

# Memory
- memory change: 1.05x