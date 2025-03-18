# Results vs. 3.13.0rc2

- fork: python
- ref: v3.14.0a6
- machine: darwin-arm64
- commit hash: 77b2c93
- commit date: 2025-03-14
- overall geometric mean: 1.095x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 132 ms: 1.18x slower                                         |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                       |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                        |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                         |
| Geometric mean | (ref)                                                          | 1.08x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                         |
| async_tree_eager_io              | 525 ms                                                         | 234 ms: 2.25x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                         |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.33x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                         |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                         |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                         |
| async_tree_eager                 | 43.2 ms                                                        | 56.9 ms: 1.32x slower                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                 |

Benchmark hidden because not significant (2): async_generators, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                         |
| float          | 31.4 ms                                                        | 35.9 ms: 1.14x slower                                        |
| nbody          | 42.5 ms                                                        | 77.9 ms: 1.83x slower                                        |
| Geometric mean | (ref)                                                          | 1.27x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                        |
| regex_dna      | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                        |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                        |
| regex_compile  | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                        |
| Geometric mean | (ref)                                                          | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                        |
| xml_etree_parse      | 62.4 ms                                                        | 59.7 ms: 1.04x faster                                        |
| tomli_loads          | 1000 ms                                                        | 1.07 sec: 1.08x slower                                       |
| json_loads           | 10.8 us                                                        | 12.0 us: 1.11x slower                                        |
| json_dumps           | 4.65 ms                                                        | 5.30 ms: 1.14x slower                                        |
| xml_etree_generate   | 35.8 ms                                                        | 41.2 ms: 1.15x slower                                        |
| xml_etree_process    | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                        |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                         |
| pickle_pure_python   | 130 us                                                         | 171 us: 1.32x slower                                         |
| Geometric mean       | (ref)                                                          | 1.12x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                        |
| python_startup_no_site | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                        |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.1 ms: 1.22x slower                                        |
| genshi_text     | 9.97 ms                                                        | 13.0 ms: 1.30x slower                                        |
| mako            | 4.41 ms                                                        | 6.19 ms: 1.40x slower                                        |
| django_template | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                        |
| Geometric mean  | (ref)                                                          | 1.35x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                         |
| async_tree_eager_io              | 525 ms                                                         | 234 ms: 2.25x faster                                         |
| gc_traversal                     | 2.04 ms                                                        | 908 us: 2.25x faster                                         |
| create_gc_cycles                 | 993 us                                                         | 480 us: 2.07x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                         |
| async_tree_io                    | 386 ms                                                         | 240 ms: 1.61x faster                                         |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.37x faster                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.33x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                         |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 247 ms: 1.22x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                         |
| sqlite_synth                     | 948 ns                                                         | 841 ns: 1.13x faster                                         |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                        |
| deepcopy                         | 145 us                                                         | 130 us: 1.12x faster                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 59.7 ms: 1.04x faster                                        |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                         |
| regex_dna                        | 94.6 ms                                                        | 91.8 ms: 1.03x faster                                        |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                        |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                         |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                        |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 38.7 ms: 1.02x slower                                        |
| go                               | 72.6 ms                                                        | 74.6 ms: 1.03x slower                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                         |
| json                             | 1.94 ms                                                        | 2.02 ms: 1.04x slower                                        |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.04x slower                                        |
| deepcopy_memo                    | 16.5 us                                                        | 17.2 us: 1.05x slower                                        |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                        |
| pyflate                          | 222 ms                                                         | 236 ms: 1.06x slower                                         |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.26 sec: 1.06x slower                                       |
| python_startup                   | 8.63 ms                                                        | 9.20 ms: 1.07x slower                                        |
| tomli_loads                      | 1000 ms                                                        | 1.07 sec: 1.08x slower                                       |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.40 us: 1.08x slower                                        |
| pycparser                        | 470 ms                                                         | 510 ms: 1.09x slower                                         |
| scimark_sor                      | 64.0 ms                                                        | 69.8 ms: 1.09x slower                                        |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                         |
| json_loads                       | 10.8 us                                                        | 12.0 us: 1.11x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                         |
| connected_components             | 208 ms                                                         | 235 ms: 1.13x slower                                         |
| mdp                              | 1.06 sec                                                       | 1.20 sec: 1.13x slower                                       |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.14x slower                                        |
| json_dumps                       | 4.65 ms                                                        | 5.30 ms: 1.14x slower                                        |
| float                            | 31.4 ms                                                        | 35.9 ms: 1.14x slower                                        |
| thrift                           | 309 us                                                         | 353 us: 1.14x slower                                         |
| xml_etree_generate               | 35.8 ms                                                        | 41.2 ms: 1.15x slower                                        |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.4 ms: 1.16x slower                                        |
| telco                            | 3.07 ms                                                        | 3.57 ms: 1.16x slower                                        |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.85 ms: 1.17x slower                                        |
| 2to3                             | 112 ms                                                         | 132 ms: 1.18x slower                                         |
| sqlglot_optimize                 | 22.2 ms                                                        | 26.2 ms: 1.18x slower                                        |
| pylint                           | 106 ms                                                         | 125 ms: 1.18x slower                                         |
| xml_etree_process                | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                        |
| python_startup_no_site           | 5.95 ms                                                        | 7.24 ms: 1.22x slower                                        |
| sympy_sum                        | 52.3 ms                                                        | 63.7 ms: 1.22x slower                                        |
| genshi_xml                       | 21.4 ms                                                        | 26.1 ms: 1.22x slower                                        |
| sqlglot_normalize                | 116 ms                                                         | 142 ms: 1.22x slower                                         |
| coverage                         | 31.2 ms                                                        | 38.4 ms: 1.23x slower                                        |
| richards                         | 22.1 ms                                                        | 27.3 ms: 1.24x slower                                        |
| sympy_integrate                  | 7.53 ms                                                        | 9.33 ms: 1.24x slower                                        |
| regex_compile                    | 47.9 ms                                                        | 59.5 ms: 1.24x slower                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                         |
| typing_runtime_protocols         | 64.6 us                                                        | 80.7 us: 1.25x slower                                        |
| meteor_contest                   | 47.9 ms                                                        | 59.9 ms: 1.25x slower                                        |
| fannkuch                         | 179 ms                                                         | 225 ms: 1.26x slower                                         |
| sympy_str                        | 95.5 ms                                                        | 120 ms: 1.26x slower                                         |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                         |
| richards_super                   | 24.7 ms                                                        | 31.4 ms: 1.27x slower                                        |
| sympy_expand                     | 159 ms                                                         | 203 ms: 1.28x slower                                         |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                        |
| pprint_safe_repr                 | 322 ms                                                         | 412 ms: 1.28x slower                                         |
| logging_simple                   | 2.24 us                                                        | 2.87 us: 1.28x slower                                        |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                         |
| pprint_pformat                   | 650 ms                                                         | 839 ms: 1.29x slower                                         |
| sqlglot_transpile                | 637 us                                                         | 825 us: 1.30x slower                                         |
| genshi_text                      | 9.97 ms                                                        | 13.0 ms: 1.30x slower                                        |
| pickle_pure_python               | 130 us                                                         | 171 us: 1.32x slower                                         |
| async_tree_eager                 | 43.2 ms                                                        | 56.9 ms: 1.32x slower                                        |
| scimark_fft                      | 124 ms                                                         | 163 ms: 1.32x slower                                         |
| sqlglot_parse                    | 519 us                                                         | 688 us: 1.33x slower                                         |
| nqueens                          | 37.2 ms                                                        | 50.1 ms: 1.35x slower                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.3 ms: 1.35x slower                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 45.4 ms: 1.35x slower                                        |
| spectral_norm                    | 43.7 ms                                                        | 59.5 ms: 1.36x slower                                        |
| deltablue                        | 1.45 ms                                                        | 2.00 ms: 1.38x slower                                        |
| logging_silent                   | 40.6 ns                                                        | 56.1 ns: 1.38x slower                                        |
| chaos                            | 24.3 ms                                                        | 33.7 ms: 1.39x slower                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.48 ms: 1.39x slower                                        |
| hexiom                           | 2.85 ms                                                        | 3.98 ms: 1.40x slower                                        |
| mako                             | 4.41 ms                                                        | 6.19 ms: 1.40x slower                                        |
| generators                       | 15.7 ms                                                        | 22.1 ms: 1.41x slower                                        |
| raytrace                         | 109 ms                                                         | 159 ms: 1.46x slower                                         |
| django_template                  | 12.5 ms                                                        | 18.4 ms: 1.47x slower                                        |
| bench_thread_pool                | 412 us                                                         | 613 us: 1.49x slower                                         |
| comprehensions                   | 6.80 us                                                        | 10.2 us: 1.49x slower                                        |
| subparsers                       | 6.26 ms                                                        | 9.41 ms: 1.50x slower                                        |
| scimark_lu                       | 42.8 ms                                                        | 67.1 ms: 1.57x slower                                        |
| nbody                            | 42.5 ms                                                        | 77.9 ms: 1.83x slower                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.6 ms: 3.06x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                                 |

Benchmark hidden because not significant (2): async_generators, async_tree_eager_memoization
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.095x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.16x