# Results vs. 3.13.0rc2

- fork: python
- ref: 7f371ed84ba471bb1b11
- machine: darwin-arm64
- commit hash: 7f371ed
- commit date: 2025-10-16
- overall geometric mean: 1.039x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 403 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.6 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 46.1 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 867 ms: 1.15x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.4 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| mako            | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| django_template | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 241 ms: 2.18x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                     |
| mdp                              | 1.06 sec                                                       | 537 ms: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 247 ms: 1.64x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 249 ms: 1.55x faster                                                     |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                    |
| deepcopy                         | 145 us                                                         | 103 us: 1.41x faster                                                     |
| go                               | 72.6 ms                                                        | 53.5 ms: 1.36x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.29x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.28x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.6 ms: 1.27x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 184 ms: 1.21x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.18x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 867 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 174 ms: 1.11x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.94 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 928 us: 1.07x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.71 ms: 1.05x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.6 ms: 1.04x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.1 ms: 1.04x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.65 ms: 1.03x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 631 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.03x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 39.7 ns: 1.02x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 121 ms: 1.02x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.0 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 403 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| fannkuch                         | 179 ms                                                         | 177 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 98.4 us: 1.01x faster                                                    |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                     |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| thrift                           | 309 us                                                         | 307 us: 1.01x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.0 ms: 1.01x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.1 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 956 ns: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 95.7 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.27 us: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 477 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.1 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 49.0 ms: 1.02x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.48 ms: 1.02x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 164 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.83 ms: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.0 ms: 1.03x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.88 ms: 1.03x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.2 ms: 1.03x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 54.7 ms: 1.05x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.20 us: 1.06x slower                                                    |
| raytrace                         | 109 ms                                                         | 115 ms: 1.06x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.69 ms: 1.06x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                     |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.0 ms: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.2 ms: 1.10x slower                                                    |
| nbody                            | 42.5 ms                                                        | 47.5 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.9 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.1 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| many_optionals                   | 200 us                                                         | 370 us: 1.85x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 17.8 ms: 2.84x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 85.6 ms: 2.96x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (3): json, spectral_norm, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251016-3.15.0a1+-7f371ed/bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1+-7f371ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x