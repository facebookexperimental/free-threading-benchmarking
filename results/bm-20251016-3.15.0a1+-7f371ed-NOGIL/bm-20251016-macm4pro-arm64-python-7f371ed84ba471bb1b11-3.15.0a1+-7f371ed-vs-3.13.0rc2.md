# Results vs. 3.13.0rc2

- fork: python
- ref: 7f371ed84ba471bb1b11
- machine: darwin-arm64
- commit hash: 7f371ed
- commit date: 2025-10-16
- overall geometric mean: 1.008x faster
- HPT reliability: 64.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.0 ms: 1.13x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 967 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.13x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| mako            | 4.41 ms                                                        | 5.83 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.23x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.69x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 767 us: 2.66x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 203 ms: 2.59x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 477 us: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.04x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| mdp                              | 1.06 sec                                                       | 605 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.53x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 123 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.8 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 129 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.26x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.2 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 61.7 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.9 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.45 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| pyflate                          | 222 ms                                                         | 199 ms: 1.12x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.07x faster                                                   |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 993 ms: 1.05x faster                                                     |
| float                            | 31.4 ms                                                        | 29.9 ms: 1.05x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 967 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.26 us: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.0 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                     |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.08x slower                                                     |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.09x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 355 ms: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.8 ns: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.15 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 724 ms: 1.11x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.67 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.13x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.77 us: 1.13x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.0 ms: 1.13x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.3 ms: 1.14x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.0 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.4 ms: 1.15x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.6 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.04 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.1 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.37 us: 1.23x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.25x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 535 us: 1.30x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.83 ms: 1.32x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.2 ms: 1.35x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.4 ms: 1.36x slower                                                    |
| many_optionals                   | 200 us                                                         | 385 us: 1.92x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.5 ms: 2.68x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.9 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251016-3.15.0a1+-7f371ed-NOGIL/bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 64.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x