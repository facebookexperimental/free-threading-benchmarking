# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: 60f2173
- commit date: 2025-03-24
- overall geometric mean: 1.086x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 130 ms: 1.17x slower                                                   |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                 |
| html5lib       | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                  |
| sphinx         | 409 ms                                                         | 439 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 234 ms: 2.25x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 99.4 ms: 1.33x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.24x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                   |
| async_generators                 | 193 ms                                                         | 191 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.09x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 55.6 ms: 1.29x slower                                                  |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                   |
| float          | 31.4 ms                                                        | 35.6 ms: 1.13x slower                                                  |
| nbody          | 42.5 ms                                                        | 78.8 ms: 1.85x slower                                                  |
| Geometric mean | (ref)                                                          | 1.27x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                  |
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                  |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                  |
| regex_compile  | 47.9 ms                                                        | 59.4 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                          | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                  |
| xml_etree_parse      | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                  |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                  |
| tomli_loads          | 1000 ms                                                        | 1.09 sec: 1.09x slower                                                 |
| json_dumps           | 4.65 ms                                                        | 5.20 ms: 1.12x slower                                                  |
| xml_etree_generate   | 35.8 ms                                                        | 40.8 ms: 1.14x slower                                                  |
| xml_etree_process    | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                                  |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 171 us: 1.31x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                  |
| python_startup_no_site | 5.95 ms                                                        | 7.26 ms: 1.22x slower                                                  |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.2 ms: 1.22x slower                                                  |
| genshi_text     | 9.97 ms                                                        | 13.1 ms: 1.31x slower                                                  |
| mako            | 4.41 ms                                                        | 6.23 ms: 1.41x slower                                                  |
| django_template | 12.5 ms                                                        | 18.2 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                          | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 223 ms: 2.34x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 234 ms: 2.25x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 930 us: 2.20x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 500 us: 1.98x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 241 ms: 1.60x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.07 sec: 1.37x faster                                                 |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 99.4 ms: 1.33x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.24x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                  |
| deepcopy                         | 145 us                                                         | 129 us: 1.13x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 842 ns: 1.13x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 57.1 ms: 1.09x faster                                                  |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                   |
| async_generators                 | 193 ms                                                         | 191 ms: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.7 ms: 1.01x faster                                                  |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                   |
| go                               | 72.6 ms                                                        | 74.8 ms: 1.03x slower                                                  |
| html5lib                         | 23.1 ms                                                        | 24.3 ms: 1.05x slower                                                  |
| pyflate                          | 222 ms                                                         | 234 ms: 1.05x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 39.9 ms: 1.05x slower                                                  |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                  |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                  |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.25 sec: 1.06x slower                                                 |
| deepcopy_reduce                  | 1.30 us                                                        | 1.38 us: 1.06x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 17.6 us: 1.07x slower                                                  |
| sphinx                           | 409 ms                                                         | 439 ms: 1.07x slower                                                   |
| pycparser                        | 470 ms                                                         | 507 ms: 1.08x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.09x slower                                                  |
| tomli_loads                      | 1000 ms                                                        | 1.09 sec: 1.09x slower                                                 |
| scimark_sor                      | 64.0 ms                                                        | 70.2 ms: 1.10x slower                                                  |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.11x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 5.20 ms: 1.12x slower                                                  |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                   |
| mdp                              | 1.06 sec                                                       | 1.20 sec: 1.13x slower                                                 |
| connected_components             | 208 ms                                                         | 235 ms: 1.13x slower                                                   |
| float                            | 31.4 ms                                                        | 35.6 ms: 1.13x slower                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 40.8 ms: 1.14x slower                                                  |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.4 ms: 1.16x slower                                                  |
| 2to3                             | 112 ms                                                         | 130 ms: 1.17x slower                                                   |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.92 ms: 1.18x slower                                                  |
| telco                            | 3.07 ms                                                        | 3.63 ms: 1.18x slower                                                  |
| pylint                           | 106 ms                                                         | 125 ms: 1.19x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                                  |
| sympy_integrate                  | 7.53 ms                                                        | 9.08 ms: 1.21x slower                                                  |
| sympy_sum                        | 52.3 ms                                                        | 63.7 ms: 1.22x slower                                                  |
| python_startup_no_site           | 5.95 ms                                                        | 7.26 ms: 1.22x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 26.2 ms: 1.22x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 59.4 ms: 1.24x slower                                                  |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                   |
| fannkuch                         | 179 ms                                                         | 223 ms: 1.25x slower                                                   |
| richards                         | 22.1 ms                                                        | 27.6 ms: 1.25x slower                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 81.0 us: 1.25x slower                                                  |
| sympy_str                        | 95.5 ms                                                        | 121 ms: 1.26x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 60.9 ms: 1.27x slower                                                  |
| richards_super                   | 24.7 ms                                                        | 31.4 ms: 1.27x slower                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 412 ms: 1.28x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 204 ms: 1.28x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 55.6 ms: 1.29x slower                                                  |
| logging_format                   | 2.45 us                                                        | 3.15 us: 1.29x slower                                                  |
| logging_simple                   | 2.24 us                                                        | 2.88 us: 1.29x slower                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 844 ms: 1.30x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.30x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 13.1 ms: 1.31x slower                                                  |
| pickle_pure_python               | 130 us                                                         | 171 us: 1.31x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 49.5 ms: 1.33x slower                                                  |
| spectral_norm                    | 43.7 ms                                                        | 59.3 ms: 1.36x slower                                                  |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.6 ms: 1.36x slower                                                  |
| chaos                            | 24.3 ms                                                        | 33.2 ms: 1.37x slower                                                  |
| logging_silent                   | 40.6 ns                                                        | 55.7 ns: 1.37x slower                                                  |
| crypto_pyaes                     | 33.6 ms                                                        | 46.5 ms: 1.38x slower                                                  |
| deltablue                        | 1.45 ms                                                        | 2.01 ms: 1.39x slower                                                  |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.48 ms: 1.39x slower                                                  |
| hexiom                           | 2.85 ms                                                        | 3.99 ms: 1.40x slower                                                  |
| mako                             | 4.41 ms                                                        | 6.23 ms: 1.41x slower                                                  |
| generators                       | 15.7 ms                                                        | 22.2 ms: 1.42x slower                                                  |
| django_template                  | 12.5 ms                                                        | 18.2 ms: 1.45x slower                                                  |
| raytrace                         | 109 ms                                                         | 159 ms: 1.46x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.21 ms: 1.47x slower                                                  |
| bench_thread_pool                | 412 us                                                         | 610 us: 1.48x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 10.1 us: 1.49x slower                                                  |
| scimark_lu                       | 42.8 ms                                                        | 66.7 ms: 1.56x slower                                                  |
| nbody                            | 42.5 ms                                                        | 78.8 ms: 1.85x slower                                                  |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.10x slower                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-60f2173-NOGIL/bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-60f2173.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.18x