# Results vs. 3.13.0rc2

- fork: python
- ref: e50acef0b2c2057874a9
- machine: darwin-arm64
- commit hash: e50acef
- commit date: 2026-04-19
- overall geometric mean: 1.020x faster
- HPT reliability: 55.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.9 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 891 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.73 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 823 us: 2.48x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 243 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| pylint                           | 106 ms                                                         | 51.8 ms: 2.04x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 523 us: 1.90x faster                                                     |
| mdp                              | 1.06 sec                                                       | 606 ms: 1.74x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 247 ms: 1.56x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.08 ms: 1.53x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1000 ms: 1.46x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.0 us: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 151 ms: 1.22x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 59.8 ms: 1.21x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 792 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 55.3 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.9 ms: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.31 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 891 ms: 1.12x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.05 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.6 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 421 ms: 1.03x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.3 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 684 ms: 1.05x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.5 ms: 1.06x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.9 ns: 1.08x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.2 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.6 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.64 ms: 1.12x slower                                                    |
| thrift                           | 309 us                                                         | 346 us: 1.12x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.73 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.5 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.6 us: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.6 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.15 us: 1.20x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.25x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.8 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 54.5 ms: 1.27x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.8 ms: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.4 ms: 1.32x slower                                                    |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 569 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.9 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260419-3.15.0a8+-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8+-e50acef.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 55.46% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x