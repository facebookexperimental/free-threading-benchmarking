# Results vs. 3.13.0rc2

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: darwin-arm64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.001x slower
- HPT reliability: 90.59%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 128 ms: 1.15x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| sphinx         | 409 ms                                                         | 439 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 289 ms: 1.80x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 298 ms: 1.30x faster                                                    |
| async_generators                 | 193 ms                                                         | 155 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.04x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 306 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 153 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 259 ms: 1.15x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 145 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.0 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 112 ms: 3.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 31.2 ms: 1.01x faster                                                   |
| pidigits       | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 51.0 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 60.0 ms: 1.25x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 838 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 105 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.0 ms: 1.10x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 150 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.8 ms: 1.25x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.81 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.28x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.54 ms: 1.25x slower                                                   |
| django_template | 12.5 ms                                                        | 16.3 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.28x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 808 us: 2.53x faster                                                    |
| pylint                           | 106 ms                                                         | 53.0 ms: 1.99x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 506 us: 1.96x faster                                                    |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 289 ms: 1.80x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.15 ms: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                    |
| deepcopy                         | 145 us                                                         | 104 us: 1.39x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 298 ms: 1.30x faster                                                    |
| go                               | 72.6 ms                                                        | 57.6 ms: 1.26x faster                                                   |
| async_generators                 | 193 ms                                                         | 155 ms: 1.25x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.74 ms: 1.24x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.6 us: 1.21x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 53.6 us: 1.21x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 838 ms: 1.19x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 798 ns: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                  |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 295 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.5 ms: 1.01x faster                                                   |
| float                            | 31.4 ms                                                        | 31.2 ms: 1.01x faster                                                   |
| pycparser                        | 470 ms                                                         | 473 ms: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                  |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.02x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 37.8 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| pidigits                         | 166 ms                                                         | 171 ms: 1.03x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.04x slower                                                    |
| async_tree_memoization           | 184 ms                                                         | 191 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 45.4 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 306 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 340 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 105 us: 1.06x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 31.6 ms: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.06x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.04 ms: 1.07x slower                                                   |
| sphinx                           | 409 ms                                                         | 439 ms: 1.07x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 153 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.64 us: 1.08x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 703 ms: 1.08x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 28.0 ms: 1.10x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.53 us: 1.11x slower                                                   |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.2 ns: 1.11x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.5 ms: 1.13x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 181 ms: 1.14x slower                                                    |
| shortest_path                    | 225 ms                                                         | 256 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.9 ms: 1.14x slower                                                   |
| 2to3                             | 112 ms                                                         | 128 ms: 1.15x slower                                                    |
| raytrace                         | 109 ms                                                         | 125 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 259 ms: 1.15x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.68 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 150 us: 1.16x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.06 ms: 1.16x slower                                                   |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.0 ms: 1.19x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 145 ms: 1.19x slower                                                    |
| nbody                            | 42.5 ms                                                        | 51.0 ms: 1.20x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 10.8 ms: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.0 ms: 1.25x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 60.0 ms: 1.25x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.54 ms: 1.25x slower                                                   |
| generators                       | 15.7 ms                                                        | 20.0 ms: 1.27x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.3 ms: 1.30x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.81 ms: 1.31x slower                                                   |
| many_optionals                   | 200 us                                                         | 265 us: 1.32x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 567 us: 1.38x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.0 ms: 1.50x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 65.0 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 161 ms: 1.57x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 112 ms: 3.86x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 90.59% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x