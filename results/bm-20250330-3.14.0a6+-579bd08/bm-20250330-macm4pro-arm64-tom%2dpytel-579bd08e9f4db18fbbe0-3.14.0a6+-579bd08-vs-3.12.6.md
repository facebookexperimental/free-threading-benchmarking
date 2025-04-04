# Results vs. 3.12.6

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: darwin-arm64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.065x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                          |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                        |
| html5lib       | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                         |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 263 ms: 1.69x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 274 ms: 1.68x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.57x faster                                                          |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                          |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                          |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                         |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                          |
| async_tree_eager                 | 45.6 ms                                                  | 43.7 ms: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                          |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 134 ms: 1.19x slower                                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.83x slower                                                         |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                         |
| nbody          | 54.2 ms                                                  | 51.5 ms: 1.05x faster                                                         |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                         |
| regex_compile  | 54.6 ms                                                  | 50.0 ms: 1.09x faster                                                         |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                                          |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                         |
| tomli_loads          | 957 ms                                                   | 941 ms: 1.02x faster                                                          |
| xml_etree_parse      | 67.9 ms                                                  | 67.1 ms: 1.01x faster                                                         |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                         |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                                          |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                         |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                          |
| json_dumps           | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                         |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.03 ms: 1.13x slower                                                         |
| python_startup_no_site | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                         |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                         |
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                         |
| genshi_xml      | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                         |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                         |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.01 ms: 2.31x faster                                                         |
| async_tree_eager_io              | 496 ms                                                   | 259 ms: 1.91x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 263 ms: 1.69x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 274 ms: 1.68x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.57x faster                                                          |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                          |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                          |
| deepcopy                         | 161 us                                                   | 114 us: 1.42x faster                                                          |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.41x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                          |
| comprehensions                   | 9.84 us                                                  | 7.77 us: 1.27x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                         |
| deepcopy_reduce                  | 1.46 us                                                  | 1.19 us: 1.22x faster                                                         |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                         |
| float                            | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                         |
| logging_silent                   | 50.9 ns                                                  | 43.3 ns: 1.18x faster                                                         |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                          |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                          |
| k_core                           | 1.12 sec                                                 | 964 ms: 1.16x faster                                                          |
| spectral_norm                    | 54.4 ms                                                  | 47.0 ms: 1.16x faster                                                         |
| scimark_sor                      | 61.0 ms                                                  | 52.9 ms: 1.15x faster                                                         |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                         |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                          |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                         |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                         |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                          |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.04 sec: 1.10x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 50.0 ms: 1.09x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 65.5 us: 1.08x faster                                                         |
| scimark_lu                       | 51.3 ms                                                  | 47.5 ms: 1.08x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                          |
| nbody                            | 54.2 ms                                                  | 51.5 ms: 1.05x faster                                                         |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.6 ms: 1.05x faster                                                         |
| nqueens                          | 43.5 ms                                                  | 41.5 ms: 1.05x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 43.7 ms: 1.04x faster                                                         |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                          |
| logging_format                   | 2.80 us                                                  | 2.70 us: 1.04x faster                                                         |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                          |
| deltablue                        | 1.73 ms                                                  | 1.67 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 7.77 ms: 1.03x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.96 ms: 1.03x faster                                                         |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                          |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.03x faster                                                          |
| pyflate                          | 216 ms                                                   | 212 ms: 1.02x faster                                                          |
| chaos                            | 28.9 ms                                                  | 28.4 ms: 1.02x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 941 ms: 1.02x faster                                                          |
| sqlalchemy_declarative           | 46.8 ms                                                  | 46.1 ms: 1.01x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 67.1 ms: 1.01x faster                                                         |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                         |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                          |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                                          |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                         |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                          |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                          |
| richards                         | 22.4 ms                                                  | 22.7 ms: 1.01x slower                                                         |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                          |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                         |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                                          |
| sympy_expand                     | 167 ms                                                   | 171 ms: 1.02x slower                                                          |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 337 ms: 1.03x slower                                                          |
| pprint_pformat                   | 665 ms                                                   | 684 ms: 1.03x slower                                                          |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                          |
| genshi_xml                       | 21.8 ms                                                  | 22.5 ms: 1.03x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                          |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                        |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                         |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.46 ms: 1.06x slower                                                         |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                         |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                         |
| html5lib                         | 23.0 ms                                                  | 24.6 ms: 1.07x slower                                                         |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                          |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                         |
| fannkuch                         | 176 ms                                                   | 190 ms: 1.08x slower                                                          |
| create_gc_cycles                 | 830 us                                                   | 905 us: 1.09x slower                                                          |
| python_startup                   | 8.01 ms                                                  | 9.03 ms: 1.13x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                          |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 134 ms: 1.19x slower                                                          |
| telco                            | 2.61 ms                                                  | 3.12 ms: 1.19x slower                                                         |
| json_dumps                       | 4.26 ms                                                  | 5.12 ms: 1.20x slower                                                         |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                         |
| many_optionals                   | 195 us                                                   | 240 us: 1.23x slower                                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.1 ms: 2.83x slower                                                         |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                                  |

Benchmark hidden because not significant (6): sympy_sum, sqlite_synth, shortest_path, richards_super, pycparser, mdp
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250330-3.14.0a6+-579bd08/bm-20250330-macm4pro-arm64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x