# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.012x slower
- HPT reliability: 94.06%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                          |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                        |
| html5lib       | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                         |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 259 ms: 2.03x faster                                                          |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                          |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                          |
| async_tree_io                    | 386 ms                                                         | 274 ms: 1.41x faster                                                          |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                          |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                          |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                          |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                          |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                          |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                          |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.07x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                          |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                          |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                         |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                          |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                          |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                         |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                         |
| nbody          | 42.5 ms                                                        | 51.5 ms: 1.21x slower                                                         |
| Geometric mean | (ref)                                                          | 1.07x slower                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                         |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                         |
| regex_compile  | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                         |
| regex_dna      | 94.6 ms                                                        | 100 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                          | 1.00x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 941 ms: 1.06x faster                                                          |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                         |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                         |
| xml_etree_process    | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                         |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                                          |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                         |
| xml_etree_parse      | 62.4 ms                                                        | 67.1 ms: 1.08x slower                                                         |
| json_dumps           | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                         |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.15x slower                                                          |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.03 ms: 1.05x slower                                                         |
| python_startup_no_site | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                         |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                         |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                         |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                         |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 259 ms: 2.03x faster                                                          |
| async_tree_eager_io_tg           | 521 ms                                                         | 263 ms: 1.98x faster                                                          |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                          |
| k_core                           | 1.46 sec                                                       | 964 ms: 1.52x faster                                                          |
| async_tree_io                    | 386 ms                                                         | 274 ms: 1.41x faster                                                          |
| deepcopy                         | 145 us                                                         | 114 us: 1.27x faster                                                          |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                         |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                          |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                          |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.21x faster                                                          |
| scimark_sor                      | 64.0 ms                                                        | 52.9 ms: 1.21x faster                                                         |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                          |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                          |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                          |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                          |
| create_gc_cycles                 | 993 us                                                         | 905 us: 1.10x faster                                                          |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                         |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.08x faster                                                         |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.07x faster                                                          |
| tomli_loads                      | 1000 ms                                                        | 941 ms: 1.06x faster                                                          |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.8 ms: 1.05x faster                                                         |
| pyflate                          | 222 ms                                                         | 212 ms: 1.05x faster                                                          |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.04x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                         |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.03x faster                                                          |
| connected_components             | 208 ms                                                         | 203 ms: 1.02x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                          |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.00x faster                                                          |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                          |
| gc_traversal                     | 2.04 ms                                                        | 2.06 ms: 1.01x slower                                                         |
| async_tree_eager                 | 43.2 ms                                                        | 43.7 ms: 1.01x slower                                                         |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 65.5 us: 1.01x slower                                                         |
| thrift                           | 309 us                                                         | 314 us: 1.01x slower                                                          |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.02x slower                                                         |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                         |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                          |
| float                            | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                         |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                          |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.6 ms: 1.03x slower                                                         |
| richards                         | 22.1 ms                                                        | 22.7 ms: 1.03x slower                                                         |
| richards_super                   | 24.7 ms                                                        | 25.5 ms: 1.03x slower                                                         |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                         |
| sympy_integrate                  | 7.53 ms                                                        | 7.77 ms: 1.03x slower                                                         |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                         |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                          |
| mdp                              | 1.06 sec                                                       | 1.10 sec: 1.04x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 2.96 ms: 1.04x slower                                                         |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.1 ms: 1.04x slower                                                         |
| xml_etree_process                | 25.4 ms                                                        | 26.4 ms: 1.04x slower                                                         |
| regex_compile                    | 47.9 ms                                                        | 50.0 ms: 1.04x slower                                                         |
| python_startup                   | 8.63 ms                                                        | 9.03 ms: 1.05x slower                                                         |
| pprint_safe_repr                 | 322 ms                                                         | 337 ms: 1.05x slower                                                          |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                         |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                          |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                          |
| coverage                         | 31.2 ms                                                        | 32.9 ms: 1.05x slower                                                         |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                                          |
| regex_dna                        | 94.6 ms                                                        | 100 ms: 1.06x slower                                                          |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                         |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                         |
| html5lib                         | 23.1 ms                                                        | 24.6 ms: 1.06x slower                                                         |
| pycparser                        | 470 ms                                                         | 499 ms: 1.06x slower                                                          |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                          |
| sympy_str                        | 95.5 ms                                                        | 102 ms: 1.06x slower                                                          |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.06x slower                                                          |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                         |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                         |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                          |
| spectral_norm                    | 43.7 ms                                                        | 47.0 ms: 1.07x slower                                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 67.1 ms: 1.08x slower                                                         |
| bench_mp_pool                    | 37.8 ms                                                        | 41.2 ms: 1.09x slower                                                         |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.46 ms: 1.09x slower                                                         |
| sympy_sum                        | 52.3 ms                                                        | 57.4 ms: 1.10x slower                                                         |
| pylint                           | 106 ms                                                         | 116 ms: 1.10x slower                                                          |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                         |
| json_dumps                       | 4.65 ms                                                        | 5.12 ms: 1.10x slower                                                         |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                         |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.10x slower                                                         |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                         |
| nqueens                          | 37.2 ms                                                        | 41.5 ms: 1.11x slower                                                         |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.01 ms: 1.13x slower                                                         |
| python_startup_no_site           | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                         |
| comprehensions                   | 6.80 us                                                        | 7.77 us: 1.14x slower                                                         |
| crypto_pyaes                     | 33.6 ms                                                        | 38.5 ms: 1.14x slower                                                         |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                         |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                         |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.15x slower                                                          |
| chaos                            | 24.3 ms                                                        | 28.4 ms: 1.17x slower                                                         |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                          |
| many_optionals                   | 200 us                                                         | 240 us: 1.20x slower                                                          |
| nbody                            | 42.5 ms                                                        | 51.5 ms: 1.21x slower                                                         |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.27x slower                                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                          |
| subparsers                       | 6.26 ms                                                        | 9.01 ms: 1.44x slower                                                         |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.1 ms: 3.15x slower                                                         |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): pidigits, pathlib
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250330-3.14.0a6+-579bd08/bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 94.06% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x