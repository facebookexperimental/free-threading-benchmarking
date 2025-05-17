# Results vs. 3.13.0rc2

- fork: python
- ref: 71cf4dd622832848cace
- machine: darwin-arm64
- commit hash: 71cf4dd
- commit date: 2025-05-16
- overall geometric mean: 1.011x faster
- HPT reliability: 66.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 25.5 ms: 1.10x slower                                                   |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 55.6 ms: 1.12x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 969 ms: 1.03x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.86 ms: 1.05x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| json_loads           | 10.8 us                                                        | 12.7 us: 1.17x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 766 us: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 477 us: 2.08x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 197 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 576 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.2 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 243 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.1 ms: 1.21x faster                                                   |
| deepcopy                         | 145 us                                                         | 123 us: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.16 ms: 1.17x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                    |
| go                               | 72.6 ms                                                        | 63.4 ms: 1.14x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 56.1 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 55.6 ms: 1.12x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.3 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.04x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 969 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                    |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                   |
| shortest_path                    | 225 ms                                                         | 230 ms: 1.03x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.86 ms: 1.05x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.7 ms: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 219 ms: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.98 ms: 1.06x slower                                                   |
| json                             | 1.94 ms                                                        | 2.08 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.08x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.4 ms: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.39 ms: 1.09x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.35 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.4 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.10x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 716 ms: 1.10x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 25.5 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.8 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.85 ms: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.7 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.4 ms: 1.15x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.5 ms: 1.16x slower                                                   |
| json_loads                       | 10.8 us                                                        | 12.7 us: 1.17x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 75.8 us: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.8 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 131 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.3 ms: 1.26x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.83 us: 1.27x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                   |
| many_optionals                   | 200 us                                                         | 256 us: 1.27x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.12 us: 1.28x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.75 us: 1.29x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                   |
| nbody                            | 42.5 ms                                                        | 55.7 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 603 us: 1.46x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.2 ms: 1.50x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.90 ms: 1.58x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.1 ms: 2.70x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 215 ns: 5.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): pathlib, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250516-3.15.0a0-71cf4dd-NOGIL/bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 66.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x