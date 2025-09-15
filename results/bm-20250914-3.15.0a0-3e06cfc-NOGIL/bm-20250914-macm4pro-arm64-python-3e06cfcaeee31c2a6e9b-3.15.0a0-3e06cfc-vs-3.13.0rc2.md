# Results vs. 3.13.0rc2

- fork: python
- ref: 3e06cfcaeee31c2a6e9b
- machine: darwin-arm64
- commit hash: 3e06cfc
- commit date: 2025-09-14
- overall geometric mean: 1.003x faster
- HPT reliability: 75.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.1 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                          | 1.08x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.02 ms: 1.16x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 970 ms: 1.03x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.53 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                   |
| mako            | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 759 us: 2.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.66x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 473 us: 2.10x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.04x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 600 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.1 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                   |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                   |
| go                               | 72.6 ms                                                        | 61.6 ms: 1.18x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 54.6 ms: 1.17x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.02 ms: 1.16x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.38 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 836 ns: 1.13x faster                                                    |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| float                            | 31.4 ms                                                        | 30.0 ms: 1.05x faster                                                   |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 970 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                    |
| dask                             | 525 ms                                                         | 531 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 95.9 ms: 1.01x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 11.0 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.9 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.06 ms: 1.07x slower                                                   |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                   |
| thrift                           | 309 us                                                         | 337 us: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.53 ms: 1.10x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                   |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 722 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.51 us: 1.12x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.8 ns: 1.13x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 48.8 ms: 1.13x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.8 ms: 1.13x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.4 ms: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.15x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.2 ms: 1.17x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.4 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.9 ms: 1.19x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.21x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.51 us: 1.25x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.2 ms: 1.29x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.3 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.31 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.0 ms: 1.33x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                   |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 582 us: 1.41x slower                                                    |
| many_optionals                   | 200 us                                                         | 334 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.3 ms: 2.71x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.5 ms: 2.96x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250914-3.15.0a0-3e06cfc-NOGIL/bm-20250914-macm4pro-arm64-python-3e06cfcaeee31c2a6e9b-3.15.0a0-3e06cfc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 75.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x