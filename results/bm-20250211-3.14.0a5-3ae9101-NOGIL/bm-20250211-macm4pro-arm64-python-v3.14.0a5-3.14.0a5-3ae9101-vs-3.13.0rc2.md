# Results vs. 3.13.0rc2

- fork: python
- ref: v3.14.0a5
- machine: darwin-arm64
- commit hash: 3ae9101
- commit date: 2025-02-11
- overall geometric mean: 1.081x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 128 ms: 1.15x slower                                         |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                       |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.04x slower                                        |
| sphinx         | 409 ms                                                         | 437 ms: 1.07x slower                                         |
| Geometric mean | (ref)                                                          | 1.06x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                         |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.29x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                         |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.62x faster                                         |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 99.9 ms: 1.33x faster                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.24x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                         |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                         |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                         |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                         |
| coroutines                       | 10.8 ms                                                        | 11.3 ms: 1.05x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                         |
| async_tree_eager                 | 43.2 ms                                                        | 57.7 ms: 1.34x slower                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.6 ms: 3.10x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                         |
| float          | 31.4 ms                                                        | 34.2 ms: 1.09x slower                                        |
| nbody          | 42.5 ms                                                        | 72.6 ms: 1.71x slower                                        |
| Geometric mean | (ref)                                                          | 1.21x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                        |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.03x faster                                        |
| regex_dna      | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                        |
| regex_compile  | 47.9 ms                                                        | 57.3 ms: 1.20x slower                                        |
| Geometric mean | (ref)                                                          | 1.00x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                        |
| xml_etree_parse      | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                        |
| tomli_loads          | 1000 ms                                                        | 1.07 sec: 1.07x slower                                       |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                        |
| json_dumps           | 4.65 ms                                                        | 5.13 ms: 1.10x slower                                        |
| xml_etree_generate   | 35.8 ms                                                        | 40.5 ms: 1.13x slower                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.7 ms: 1.17x slower                                        |
| unpickle_pure_python | 99.5 us                                                        | 127 us: 1.28x slower                                         |
| pickle_pure_python   | 130 us                                                         | 173 us: 1.33x slower                                         |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.26 ms: 1.07x slower                                        |
| python_startup_no_site | 5.95 ms                                                        | 6.68 ms: 1.12x slower                                        |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                        |
| genshi_text     | 9.97 ms                                                        | 12.7 ms: 1.28x slower                                        |
| mako            | 4.41 ms                                                        | 6.22 ms: 1.41x slower                                        |
| django_template | 12.5 ms                                                        | 17.9 ms: 1.44x slower                                        |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.37x faster                                         |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.29x faster                                         |
| gc_traversal                     | 2.04 ms                                                        | 906 us: 2.25x faster                                         |
| create_gc_cycles                 | 993 us                                                         | 494 us: 2.01x faster                                         |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                         |
| async_tree_io                    | 386 ms                                                         | 238 ms: 1.62x faster                                         |
| k_core                           | 1.46 sec                                                       | 1.03 sec: 1.42x faster                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 140 ms: 1.33x faster                                         |
| async_tree_none_tg               | 133 ms                                                         | 99.9 ms: 1.33x faster                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.24x faster                                         |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                         |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.16x faster                                         |
| deepcopy                         | 145 us                                                         | 125 us: 1.16x faster                                         |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.14x faster                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.2 ms: 1.12x faster                                        |
| sqlite_synth                     | 948 ns                                                         | 848 ns: 1.12x faster                                         |
| xml_etree_parse                  | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                        |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                         |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                         |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                         |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.03x faster                                        |
| regex_dna                        | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                        |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                       |
| deepcopy_memo                    | 16.5 us                                                        | 16.3 us: 1.01x faster                                        |
| go                               | 72.6 ms                                                        | 72.2 ms: 1.01x faster                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 38.0 ms: 1.01x slower                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.16 sec: 1.02x slower                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                         |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                         |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                        |
| pathlib                          | 11.1 ms                                                        | 11.4 ms: 1.03x slower                                        |
| pyflate                          | 222 ms                                                         | 230 ms: 1.03x slower                                         |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.04x slower                                        |
| coroutines                       | 10.8 ms                                                        | 11.3 ms: 1.05x slower                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.36 us: 1.05x slower                                        |
| tomli_loads                      | 1000 ms                                                        | 1.07 sec: 1.07x slower                                       |
| pycparser                        | 470 ms                                                         | 502 ms: 1.07x slower                                         |
| sphinx                           | 409 ms                                                         | 437 ms: 1.07x slower                                         |
| python_startup                   | 8.63 ms                                                        | 9.26 ms: 1.07x slower                                        |
| scimark_sor                      | 64.0 ms                                                        | 69.7 ms: 1.09x slower                                        |
| float                            | 31.4 ms                                                        | 34.2 ms: 1.09x slower                                        |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                        |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                         |
| dulwich_log                      | 19.8 ms                                                        | 21.9 ms: 1.10x slower                                        |
| json_dumps                       | 4.65 ms                                                        | 5.13 ms: 1.10x slower                                        |
| mdp                              | 1.06 sec                                                       | 1.17 sec: 1.11x slower                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                         |
| connected_components             | 208 ms                                                         | 233 ms: 1.12x slower                                         |
| python_startup_no_site           | 5.95 ms                                                        | 6.68 ms: 1.12x slower                                        |
| xml_etree_generate               | 35.8 ms                                                        | 40.5 ms: 1.13x slower                                        |
| thrift                           | 309 us                                                         | 352 us: 1.14x slower                                         |
| 2to3                             | 112 ms                                                         | 128 ms: 1.15x slower                                         |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.1 ms: 1.15x slower                                        |
| telco                            | 3.07 ms                                                        | 3.56 ms: 1.16x slower                                        |
| sqlglot_optimize                 | 22.2 ms                                                        | 25.8 ms: 1.16x slower                                        |
| pylint                           | 106 ms                                                         | 123 ms: 1.17x slower                                         |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                        |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.85 ms: 1.17x slower                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.7 ms: 1.17x slower                                        |
| fannkuch                         | 179 ms                                                         | 213 ms: 1.19x slower                                         |
| regex_compile                    | 47.9 ms                                                        | 57.3 ms: 1.20x slower                                        |
| sqlglot_normalize                | 116 ms                                                         | 140 ms: 1.20x slower                                         |
| sympy_sum                        | 52.3 ms                                                        | 63.1 ms: 1.21x slower                                        |
| genshi_xml                       | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                        |
| coverage                         | 31.2 ms                                                        | 38.0 ms: 1.22x slower                                        |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                         |
| richards                         | 22.1 ms                                                        | 27.1 ms: 1.23x slower                                        |
| sympy_integrate                  | 7.53 ms                                                        | 9.29 ms: 1.23x slower                                        |
| sympy_expand                     | 159 ms                                                         | 197 ms: 1.24x slower                                         |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                         |
| sympy_str                        | 95.5 ms                                                        | 119 ms: 1.24x slower                                         |
| richards_super                   | 24.7 ms                                                        | 31.0 ms: 1.25x slower                                        |
| pprint_safe_repr                 | 322 ms                                                         | 409 ms: 1.27x slower                                         |
| sqlglot_transpile                | 637 us                                                         | 812 us: 1.27x slower                                         |
| unpickle_pure_python             | 99.5 us                                                        | 127 us: 1.28x slower                                         |
| genshi_text                      | 9.97 ms                                                        | 12.7 ms: 1.28x slower                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 82.6 us: 1.28x slower                                        |
| nqueens                          | 37.2 ms                                                        | 47.8 ms: 1.28x slower                                        |
| logging_format                   | 2.45 us                                                        | 3.14 us: 1.28x slower                                        |
| logging_simple                   | 2.24 us                                                        | 2.87 us: 1.28x slower                                        |
| pprint_pformat                   | 650 ms                                                         | 836 ms: 1.29x slower                                         |
| spectral_norm                    | 43.7 ms                                                        | 56.7 ms: 1.30x slower                                        |
| sqlglot_parse                    | 519 us                                                         | 675 us: 1.30x slower                                         |
| scimark_fft                      | 124 ms                                                         | 161 ms: 1.30x slower                                         |
| crypto_pyaes                     | 33.6 ms                                                        | 44.2 ms: 1.31x slower                                        |
| pickle_pure_python               | 130 us                                                         | 173 us: 1.33x slower                                         |
| async_tree_eager                 | 43.2 ms                                                        | 57.7 ms: 1.34x slower                                        |
| chaos                            | 24.3 ms                                                        | 32.7 ms: 1.35x slower                                        |
| logging_silent                   | 40.6 ns                                                        | 55.0 ns: 1.35x slower                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.6 ms: 1.36x slower                                        |
| hexiom                           | 2.85 ms                                                        | 3.92 ms: 1.38x slower                                        |
| comprehensions                   | 6.80 us                                                        | 9.58 us: 1.41x slower                                        |
| mako                             | 4.41 ms                                                        | 6.22 ms: 1.41x slower                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.53 ms: 1.42x slower                                        |
| deltablue                        | 1.45 ms                                                        | 2.08 ms: 1.43x slower                                        |
| django_template                  | 12.5 ms                                                        | 17.9 ms: 1.44x slower                                        |
| generators                       | 15.7 ms                                                        | 22.6 ms: 1.44x slower                                        |
| subparsers                       | 6.26 ms                                                        | 9.05 ms: 1.45x slower                                        |
| raytrace                         | 109 ms                                                         | 158 ms: 1.45x slower                                         |
| bench_thread_pool                | 412 us                                                         | 626 us: 1.52x slower                                         |
| scimark_lu                       | 42.8 ms                                                        | 65.4 ms: 1.53x slower                                        |
| nbody                            | 42.5 ms                                                        | 72.6 ms: 1.71x slower                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.6 ms: 3.10x slower                                        |
| Geometric mean                   | (ref)                                                          | 1.09x slower                                                 |
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.16x