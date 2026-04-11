# Results vs. 3.13.0rc2

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: darwin-arm64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.095x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 409 ms                                                         | 388 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 214 ms: 2.46x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.44x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.3 ms: 1.45x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.3 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 244 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.18x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 213 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.5 ms: 1.19x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.6 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 801 ms: 1.25x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.3 us: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 214 ms: 2.46x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 213 ms: 2.44x faster                                                     |
| mdp                              | 1.06 sec                                                       | 525 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 220 ms: 1.84x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 227 ms: 1.70x faster                                                     |
| k_core                           | 1.46 sec                                                       | 894 ms: 1.64x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.85 ms: 1.63x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.6 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.3 ms: 1.45x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.45x faster                                                    |
| go                               | 72.6 ms                                                        | 51.2 ms: 1.42x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.39x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.3 ms: 1.35x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 801 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 244 ms: 1.23x faster                                                     |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| float                            | 31.4 ms                                                        | 26.5 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.18x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.90 sec: 1.12x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 20.8 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 39.9 ms: 1.08x faster                                                    |
| fannkuch                         | 179 ms                                                         | 166 ms: 1.08x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.08x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 934 us: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 303 ms: 1.06x faster                                                     |
| spectral_norm                    | 43.7 ms                                                        | 41.2 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 987 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 213 ms: 1.06x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.70 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 388 ms: 1.05x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 95.3 us: 1.04x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.36 us: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 454 ms: 1.04x faster                                                     |
| nqueens                          | 37.2 ms                                                        | 36.1 ms: 1.03x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.8 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.03x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 925 ns: 1.02x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.35 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 63.7 us: 1.01x faster                                                    |
| chaos                            | 24.3 ms                                                        | 23.9 ms: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.67 ms: 1.00x slower                                                    |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                     |
| thrift                           | 309 us                                                         | 313 us: 1.01x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 6.93 us: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.8 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.6 ms: 1.03x slower                                                    |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 99.7 ms: 1.04x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.24 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.8 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 45.2 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 232 ms: 1.12x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 37.8 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 118 ms: 1.15x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.1 ms: 1.15x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.38 ms: 1.16x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.1 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.4 ms: 2.78x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                             |

Benchmark hidden because not significant (3): regex_dna, connected_components, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x