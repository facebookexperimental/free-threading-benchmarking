# Results vs. 3.13.0rc2

- fork: python
- ref: v3.14.0a6
- machine: darwin-arm64
- commit hash: 77b2c93
- commit date: 2025-03-14
- overall geometric mean: 1.014x slower
- HPT reliability: 96.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                         |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                       |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                        |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                          | 1.02x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 268 ms: 1.94x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 266 ms: 1.52x faster                                         |
| async_tree_io                    | 386 ms                                                         | 266 ms: 1.45x faster                                         |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                         |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                         |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                        |
| async_tree_eager                 | 43.2 ms                                                        | 43.8 ms: 1.01x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                 |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                         |
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                        |
| nbody          | 42.5 ms                                                        | 51.0 ms: 1.20x slower                                        |
| Geometric mean | (ref)                                                          | 1.07x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                        |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                        |
| regex_v8       | 10.7 ms                                                        | 10.9 ms: 1.02x slower                                        |
| regex_compile  | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                          | 1.02x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 862 ms: 1.16x faster                                         |
| xml_etree_iterparse  | 46.1 ms                                                        | 46.6 ms: 1.01x slower                                        |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                        |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                         |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                        |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                        |
| json_dumps           | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                        |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                         |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                        |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                        |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                        |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                        |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                        |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                         |
| async_tree_eager_io_tg           | 521 ms                                                         | 268 ms: 1.94x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 266 ms: 1.52x faster                                         |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                         |
| async_tree_io                    | 386 ms                                                         | 266 ms: 1.45x faster                                         |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                         |
| deepcopy_memo                    | 16.5 us                                                        | 12.9 us: 1.28x faster                                        |
| go                               | 72.6 ms                                                        | 58.9 ms: 1.23x faster                                        |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                         |
| scimark_sor                      | 64.0 ms                                                        | 54.9 ms: 1.17x faster                                        |
| tomli_loads                      | 1000 ms                                                        | 862 ms: 1.16x faster                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                         |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                        |
| create_gc_cycles                 | 993 us                                                         | 900 us: 1.10x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 270 ms: 1.09x faster                                         |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                         |
| pyflate                          | 222 ms                                                         | 207 ms: 1.07x faster                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 117 ms: 1.04x faster                                         |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.09 sec: 1.02x faster                                       |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                         |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                         |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                        |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                         |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 37.7 ms: 1.00x faster                                        |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                         |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                        |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                        |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 46.6 ms: 1.01x slower                                        |
| async_tree_eager                 | 43.2 ms                                                        | 43.8 ms: 1.01x slower                                        |
| regex_v8                         | 10.7 ms                                                        | 10.9 ms: 1.02x slower                                        |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                        |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.3 ms: 1.02x slower                                        |
| pprint_safe_repr                 | 322 ms                                                         | 329 ms: 1.02x slower                                         |
| regex_compile                    | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                        |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                       |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                         |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.03x slower                                         |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.03x slower                                        |
| pathlib                          | 11.1 ms                                                        | 11.4 ms: 1.03x slower                                        |
| telco                            | 3.07 ms                                                        | 3.16 ms: 1.03x slower                                        |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                         |
| richards_super                   | 24.7 ms                                                        | 25.5 ms: 1.03x slower                                        |
| meteor_contest                   | 47.9 ms                                                        | 49.5 ms: 1.03x slower                                        |
| thrift                           | 309 us                                                         | 320 us: 1.04x slower                                         |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                        |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                        |
| gc_traversal                     | 2.04 ms                                                        | 2.13 ms: 1.04x slower                                        |
| mdp                              | 1.06 sec                                                       | 1.11 sec: 1.05x slower                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 67.7 us: 1.05x slower                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.3 ms: 1.05x slower                                        |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                        |
| bench_thread_pool                | 412 us                                                         | 432 us: 1.05x slower                                         |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                        |
| hexiom                           | 2.85 ms                                                        | 3.00 ms: 1.05x slower                                        |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                         |
| pycparser                        | 470 ms                                                         | 498 ms: 1.06x slower                                         |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                        |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                        |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.33 ms: 1.07x slower                                        |
| fannkuch                         | 179 ms                                                         | 191 ms: 1.07x slower                                         |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                        |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                         |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                        |
| sqlglot_optimize                 | 22.2 ms                                                        | 23.9 ms: 1.08x slower                                        |
| logging_silent                   | 40.6 ns                                                        | 43.8 ns: 1.08x slower                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                        |
| sympy_expand                     | 159 ms                                                         | 172 ms: 1.08x slower                                         |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                         |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                        |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                        |
| json_dumps                       | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                        |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.23 ms: 1.09x slower                                        |
| sqlglot_transpile                | 637 us                                                         | 697 us: 1.09x slower                                         |
| sqlglot_normalize                | 116 ms                                                         | 128 ms: 1.10x slower                                         |
| deltablue                        | 1.45 ms                                                        | 1.60 ms: 1.10x slower                                        |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                         |
| sqlglot_parse                    | 519 us                                                         | 575 us: 1.11x slower                                         |
| spectral_norm                    | 43.7 ms                                                        | 49.2 ms: 1.12x slower                                        |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                         |
| comprehensions                   | 6.80 us                                                        | 7.79 us: 1.14x slower                                        |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                         |
| scimark_lu                       | 42.8 ms                                                        | 49.9 ms: 1.17x slower                                        |
| chaos                            | 24.3 ms                                                        | 28.4 ms: 1.17x slower                                        |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                        |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                        |
| many_optionals                   | 200 us                                                         | 238 us: 1.19x slower                                         |
| nbody                            | 42.5 ms                                                        | 51.0 ms: 1.20x slower                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                         |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                         |
| subparsers                       | 6.26 ms                                                        | 8.80 ms: 1.40x slower                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                 |

Benchmark hidden because not significant (3): xml_etree_parse, async_tree_eager_cpu_io_mixed, sqlite_synth
Ignored benchmarks (4) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 96.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x