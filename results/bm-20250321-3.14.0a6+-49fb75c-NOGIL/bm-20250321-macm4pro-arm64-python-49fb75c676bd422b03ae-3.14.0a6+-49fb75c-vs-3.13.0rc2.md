# Results vs. 3.13.0rc2

- fork: python
- ref: 49fb75c676bd422b03ae
- machine: darwin-arm64
- commit hash: 49fb75c
- commit date: 2025-03-21
- overall geometric mean: 1.090x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 132 ms: 1.19x slower                                                     |
| html5lib       | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                    |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.08x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.8 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 56.1 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmark hidden because not significant (2): async_tree_eager_memoization, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| float          | 31.4 ms                                                        | 36.0 ms: 1.15x slower                                                    |
| nbody          | 42.5 ms                                                        | 78.0 ms: 1.83x slower                                                    |
| Geometric mean | (ref)                                                          | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 59.2 ms: 1.24x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.21 ms: 1.12x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 41.0 ms: 1.15x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 30.6 ms: 1.21x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 170 us: 1.31x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.29 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.4 ms: 1.24x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 13.2 ms: 1.32x slower                                                    |
| mako            | 4.41 ms                                                        | 6.18 ms: 1.40x slower                                                    |
| django_template | 12.5 ms                                                        | 18.3 ms: 1.47x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.35x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 936 us: 2.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 511 us: 1.94x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.39x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.8 ms: 1.33x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.4 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| deepcopy                         | 145 us                                                         | 128 us: 1.13x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 844 ns: 1.12x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.67 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.9 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                    |
| go                               | 72.6 ms                                                        | 75.3 ms: 1.04x slower                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 17.3 us: 1.05x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.4 ms: 1.06x slower                                                    |
| pyflate                          | 222 ms                                                         | 235 ms: 1.06x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.26 sec: 1.06x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 40.4 ms: 1.07x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.39 us: 1.07x slower                                                    |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                   |
| scimark_sor                      | 64.0 ms                                                        | 69.1 ms: 1.08x slower                                                    |
| pycparser                        | 470 ms                                                         | 508 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.21 ms: 1.12x slower                                                    |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| connected_components             | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.20 sec: 1.14x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 41.0 ms: 1.15x slower                                                    |
| float                            | 31.4 ms                                                        | 36.0 ms: 1.15x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.3 ms: 1.15x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.5 ms: 1.16x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.61 ms: 1.18x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.92 ms: 1.18x slower                                                    |
| pylint                           | 106 ms                                                         | 125 ms: 1.19x slower                                                     |
| 2to3                             | 112 ms                                                         | 132 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 30.6 ms: 1.21x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 9.10 ms: 1.21x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.7 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.29 ms: 1.22x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 26.4 ms: 1.24x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 59.2 ms: 1.24x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 59.6 ms: 1.25x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 119 ms: 1.25x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 81.2 us: 1.26x slower                                                    |
| fannkuch                         | 179 ms                                                         | 226 ms: 1.26x slower                                                     |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 202 ms: 1.27x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 31.5 ms: 1.28x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 414 ms: 1.29x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                                     |
| logging_format                   | 2.45 us                                                        | 3.16 us: 1.29x slower                                                    |
| richards                         | 22.1 ms                                                        | 28.5 ms: 1.29x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.90 us: 1.30x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 56.1 ms: 1.30x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 845 ms: 1.30x slower                                                     |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 170 us: 1.31x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 13.2 ms: 1.32x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 164 ms: 1.32x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 49.6 ms: 1.33x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.4 ms: 1.35x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 55.3 ns: 1.36x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 59.7 ms: 1.37x slower                                                    |
| chaos                            | 24.3 ms                                                        | 33.4 ms: 1.38x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.98 ms: 1.40x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.03 ms: 1.40x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.18 ms: 1.40x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 47.2 ms: 1.40x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.51 ms: 1.41x slower                                                    |
| generators                       | 15.7 ms                                                        | 22.2 ms: 1.41x slower                                                    |
| django_template                  | 12.5 ms                                                        | 18.3 ms: 1.47x slower                                                    |
| raytrace                         | 109 ms                                                         | 163 ms: 1.49x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 10.2 us: 1.49x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 618 us: 1.50x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.43 ms: 1.51x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 68.4 ms: 1.60x slower                                                    |
| nbody                            | 42.5 ms                                                        | 78.0 ms: 1.83x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.10x slower                                                             |

Benchmark hidden because not significant (3): async_tree_eager_memoization, async_generators, docutils
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-49fb75c-NOGIL/bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.18x