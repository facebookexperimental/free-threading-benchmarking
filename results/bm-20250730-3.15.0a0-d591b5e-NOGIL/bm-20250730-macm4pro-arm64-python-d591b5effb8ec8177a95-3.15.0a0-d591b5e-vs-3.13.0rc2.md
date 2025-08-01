# Results vs. 3.13.0rc2

- fork: python
- ref: d591b5effb8ec8177a95
- machine: darwin-arm64
- commit hash: d591b5e
- commit date: 2025-07-30
- overall geometric mean: 1.007x faster
- HPT reliability: 76.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 989 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.5 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.26x faster                                                            |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 60.7 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.54 ms: 1.02x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                  |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| mako            | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                   |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 774 us: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 604 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 85.5 ms: 1.55x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 988 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.1 ms: 1.44x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                    |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.7 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.9 ms: 1.17x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.13 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.1 us: 1.17x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.8 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 29.0 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.0 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                  |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 989 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.54 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.01 sec: 1.01x slower                                                  |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.24 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.11 ms: 1.09x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 711 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 47.6 ms: 1.10x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.7 ms: 1.11x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 45.2 ns: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.61 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.4 us: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.1 ms: 1.14x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.15x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.1 ms: 1.16x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.84 us: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.96 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 145 ms: 1.17x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.3 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.34 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 39.7 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.28 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.73 ms: 1.30x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.6 ms: 1.35x slower                                                   |
| nbody                            | 42.5 ms                                                        | 60.7 ms: 1.43x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 601 us: 1.46x slower                                                    |
| many_optionals                   | 200 us                                                         | 325 us: 1.62x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 76.7 ms: 2.65x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.0 ms: 2.88x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                            |

Benchmark hidden because not significant (3): sphinx, coroutines, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 76.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x