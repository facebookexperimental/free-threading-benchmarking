# Results vs. 3.13.0rc2

- fork: python
- ref: cf6758ff9ebd6df8ac2a
- machine: darwin-arm64
- commit hash: cf6758f
- commit date: 2025-12-24
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 21.7 ms: 1.07x faster                                                    |
| sphinx         | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.8 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 935 ms: 1.07x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 33.9 ms: 1.05x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 96.0 us: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.9 ms: 1.03x faster                                                    |
| mako            | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 219 ms: 2.38x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 222 ms: 2.37x faster                                                     |
| mdp                              | 1.06 sec                                                       | 541 ms: 1.96x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.81x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 234 ms: 1.65x faster                                                     |
| k_core                           | 1.46 sec                                                       | 900 ms: 1.63x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.05 ms: 1.55x faster                                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.43x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 103 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 140 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 48.9 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.88 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 255 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.14x faster                                                     |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.10x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.08x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.8 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.85 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 935 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.5 ms: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.7 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 33.9 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.3 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                     |
| sphinx                           | 409 ms                                                         | 391 ms: 1.05x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.9 ms: 1.04x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.73 ms: 1.04x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.4 ms: 1.04x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 626 ms: 1.04x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 96.0 us: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.6 us: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.72 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.9 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 162 ms: 1.02x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.8 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.43 us: 1.00x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.23 us: 1.00x faster                                                    |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.05 ms: 1.00x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 44.2 ms: 1.01x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.75 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 961 ns: 1.01x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.0 ms: 1.02x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.2 ms: 1.04x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.07 us: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 54.7 ms: 1.05x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.9 ms: 1.05x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| nbody                            | 42.5 ms                                                        | 44.9 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.31 ms: 1.06x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.70 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.0 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 242 ms: 1.16x slower                                                     |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.4 ms: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.20x slower                                                     |
| generators                       | 15.7 ms                                                        | 19.0 ms: 1.21x slower                                                    |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (1): connected_components
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251224-3.15.0a3+-cf6758f/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3+-cf6758f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x