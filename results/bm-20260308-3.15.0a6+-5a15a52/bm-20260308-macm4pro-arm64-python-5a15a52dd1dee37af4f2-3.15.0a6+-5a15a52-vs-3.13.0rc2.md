# Results vs. 3.13.0rc2

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: darwin-arm64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.046x faster
- HPT reliability: 80.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| html5lib       | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 233 ms: 1.74x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.06x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.8 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| nbody          | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.0 ms: 1.00x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 862 ms: 1.16x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.06 ms: 1.05x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.54 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| mako            | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.33x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 233 ms: 2.25x faster                                                     |
| mdp                              | 1.06 sec                                                       | 555 ms: 1.91x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 233 ms: 1.74x faster                                                     |
| k_core                           | 1.46 sec                                                       | 911 ms: 1.61x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 243 ms: 1.59x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.44x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.34x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| go                               | 72.6 ms                                                        | 56.6 ms: 1.28x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.19x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 191 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 862 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 255 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 931 us: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.06x faster                                                     |
| richards                         | 22.1 ms                                                        | 21.0 ms: 1.05x faster                                                    |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.04x faster                                                     |
| richards_super                   | 24.7 ms                                                        | 23.7 ms: 1.04x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.4 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.0 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 122 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 48.0 ms: 1.00x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.0 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.26 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 326 ms: 1.01x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.3 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 2.89 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                    |
| connected_components             | 208 ms                                                         | 212 ms: 1.02x slower                                                     |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.8 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| thrift                           | 309 us                                                         | 317 us: 1.03x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 66.3 us: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 667 ms: 1.03x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.74 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.1 ms: 1.03x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.1 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.06 ms: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.53 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 435 us: 1.06x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.89 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.3 ns: 1.07x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.1 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.82 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.54 ms: 1.10x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.50 us: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.3 ms: 1.11x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.9 ms: 1.11x slower                                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| nbody                            | 42.5 ms                                                        | 48.8 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.5 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.4 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 260 us: 1.30x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 84.8 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (3): sphinx, sqlite_synth, json_loads
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260308-3.15.0a6+-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 80.35% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.19x