# Results vs. 3.13.0rc2

- fork: python
- ref: 79321fdce3227cf09bb8
- machine: darwin-arm64
- commit hash: 79321fd
- commit date: 2026-04-22
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| sphinx         | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.6 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.2 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.56 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 809 ms: 1.24x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.6 us: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 65.2 ms: 1.05x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.95 ms                                                        | 5.84 ms: 1.02x faster                                                    |
| python_startup         | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| Geometric mean         | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 9.83 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 220 ms: 2.38x faster                                                     |
| pylint                           | 106 ms                                                         | 50.4 ms: 2.09x faster                                                    |
| mdp                              | 1.06 sec                                                       | 533 ms: 1.99x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 231 ms: 1.67x faster                                                     |
| k_core                           | 1.46 sec                                                       | 896 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.95 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.3 us: 1.49x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.45x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 100 ms: 1.42x faster                                                     |
| go                               | 72.6 ms                                                        | 51.9 ms: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.38x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 134 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.6 ms: 1.33x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.6 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 809 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                    |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 250 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.8 ms: 1.16x faster                                                    |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.56 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 173 ms: 1.11x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 21.2 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.3 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.2 ms: 1.06x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 939 us: 1.06x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 35.2 ms: 1.06x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 95.6 us: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| sphinx                           | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 629 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 42.5 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 5.84 ms: 1.02x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.02x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.83 ms: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| connected_components             | 208 ms                                                         | 205 ms: 1.01x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.53 ms: 1.01x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 938 ns: 1.01x faster                                                     |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.22 us: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                     |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.01 us: 1.03x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 425 us: 1.03x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.1 ns: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                    |
| nbody                            | 42.5 ms                                                        | 44.4 ms: 1.04x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 65.2 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.68 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.07x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.07x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 47.9 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 235 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 38.9 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.42 ms: 1.19x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.7 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 248 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.2 ms: 2.81x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (3): regex_dna, chaos, thrift
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260422-3.15.0a8+-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8+-79321fd.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.20x