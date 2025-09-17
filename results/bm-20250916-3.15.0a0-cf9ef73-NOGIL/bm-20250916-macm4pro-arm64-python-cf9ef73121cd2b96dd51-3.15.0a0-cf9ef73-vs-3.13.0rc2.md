# Results vs. 3.13.0rc2

- fork: python
- ref: cf9ef73121cd2b96dd51
- machine: darwin-arm64
- commit hash: cf9ef73
- commit date: 2025-09-16
- overall geometric mean: 1.014x faster
- HPT reliability: 56.49%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| docutils       | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 940 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| mako            | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                   |
| django_template | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 753 us: 2.71x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.58x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 470 us: 2.11x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 209 ms: 1.85x faster                                                    |
| mdp                              | 1.06 sec                                                       | 596 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 86.3 ms: 1.54x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 232 ms: 1.30x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                   |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 239 ms: 1.23x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.4 ms: 1.20x faster                                                   |
| go                               | 72.6 ms                                                        | 61.4 ms: 1.18x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.4 ms: 1.15x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 197 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.62 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                  |
| tomli_loads                      | 1000 ms                                                        | 940 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 986 ms: 1.06x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.52 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.97 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                   |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.7 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 184 ms: 1.03x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.05x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.99 ms: 1.06x slower                                                   |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.06x slower                                                   |
| thrift                           | 309 us                                                         | 331 us: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 224 ms: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.49 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 41.7 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.1 ns: 1.11x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 728 ms: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 139 ms: 1.12x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.6 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.2 ms: 1.13x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.7 us: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.89 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.16x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 56.2 ms: 1.17x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.1 ms: 1.19x slower                                                   |
| chaos                            | 24.3 ms                                                        | 29.0 ms: 1.19x slower                                                   |
| raytrace                         | 109 ms                                                         | 130 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.36 us: 1.23x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.81 ms: 1.32x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.5 ms: 1.32x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 580 us: 1.41x slower                                                    |
| many_optionals                   | 200 us                                                         | 332 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.9 ms: 3.02x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                            |

Benchmark hidden because not significant (2): sphinx, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-cf9ef73-NOGIL/bm-20250916-macm4pro-arm64-python-cf9ef73121cd2b96dd51-3.15.0a0-cf9ef73.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 56.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.21x