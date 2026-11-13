# Results vs. 3.13.0rc2

- fork: python
- ref: ecefd40671f340d543c2
- machine: darwin-arm64
- commit hash: ecefd40
- commit date: 2026-11-12
- overall geometric mean: 1.097x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| docutils       | 1.05 sec                                                       | 918 ms: 1.14x faster                                                        |
| html5lib       | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                       |
| sphinx         | 409 ms                                                         | 394 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.6 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.67 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.0 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 152 ms: 1.09x faster                                                        |
| nbody          | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.36 ms: 1.18x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                       |
| regex_compile  | 47.9 ms                                                        | 53.9 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.59 ms: 1.29x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 822 ms: 1.22x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 91.9 us: 1.08x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 66.0 ms: 1.06x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 505 ms: 2.09x faster                                                        |
| pylint                           | 106 ms                                                         | 52.3 ms: 2.02x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.98x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.6 ms: 1.96x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 278 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.97 ms: 1.58x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 642 us: 1.55x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.5 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.1 us: 1.43x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.39x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.59 ms: 1.29x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 822 ms: 1.22x faster                                                        |
| pyflate                          | 222 ms                                                         | 183 ms: 1.21x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.36 ms: 1.18x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 27.4 ms: 1.15x faster                                                       |
| docutils                         | 1.05 sec                                                       | 918 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.3 ms: 1.14x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 163 ms: 1.13x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.81 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.67 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 273 ms: 1.10x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.2 ms: 1.09x faster                                                       |
| pidigits                         | 166 ms                                                         | 152 ms: 1.09x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 114 ms: 1.09x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.62 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.3 ms: 1.08x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 91.9 us: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.6 ms: 1.06x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 22.0 ms: 1.05x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.6 ms: 1.05x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.2 ms: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 394 ms: 1.04x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 913 ns: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.17 us: 1.03x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 314 ms: 1.02x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 302 us: 1.02x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.38 ms: 1.02x faster                                                       |
| mako                             | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| nbody                            | 42.5 ms                                                        | 41.8 ms: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.45 ms: 1.00x faster                                                       |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                        |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.72 ms: 1.01x slower                                                       |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                        |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                       |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 99.1 ms: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| regex_dna                        | 94.6 ms                                                        | 98.6 ms: 1.04x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 44.7 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 66.0 ms: 1.06x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 43.2 ns: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.9 ms: 1.13x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.71 ms: 1.13x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                       |
| many_optionals                   | 200 us                                                         | 231 us: 1.15x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 143 ms: 1.39x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.0 ms: 3.25x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (2): pprint_pformat, comprehensions
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-ecefd40/bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x