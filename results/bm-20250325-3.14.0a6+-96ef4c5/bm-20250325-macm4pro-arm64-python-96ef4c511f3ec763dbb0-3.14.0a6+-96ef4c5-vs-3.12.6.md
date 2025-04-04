# Results vs. 3.12.6

- fork: python
- ref: 96ef4c511f3ec763dbb0
- machine: darwin-arm64
- commit hash: 96ef4c5
- commit date: 2025-03-25
- overall geometric mean: 1.065x faster
- HPT reliability: 99.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                    |
| sphinx         | 434 ms                                                   | 419 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 261 ms: 1.71x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 135 ms: 1.19x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.0 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                    |
| nbody          | 54.2 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 100 ms: 1.01x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.8 ms: 1.13x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.3 ms: 1.06x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| tomli_loads          | 957 ms                                                   | 936 ms: 1.02x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.08 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.04 ms: 1.13x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.04 ms: 2.30x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 261 ms: 1.84x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 261 ms: 1.71x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 271 ms: 1.69x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 151 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.41x faster                                                    |
| deepcopy                         | 161 us                                                   | 114 us: 1.41x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.77 us: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| float                            | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                     |
| k_core                           | 1.12 sec                                                 | 963 ms: 1.16x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 46.9 ms: 1.16x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 53.2 ms: 1.15x faster                                                    |
| go                               | 70.0 ms                                                  | 61.9 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.8 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.04 sec: 1.10x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 50.2 ms: 1.09x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 47.2 ms: 1.09x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 65.4 us: 1.09x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.08x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                                     |
| nbody                            | 54.2 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.3 ms: 1.06x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.5 ms: 1.05x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.4 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 419 ms: 1.03x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.77 ms: 1.03x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.72 us: 1.03x faster                                                    |
| pyflate                          | 216 ms                                                   | 210 ms: 1.03x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.96 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 936 ms: 1.02x faster                                                     |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                     |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.9 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| mdp                              | 1.09 sec                                                 | 1.08 sec: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 957 ns: 1.01x faster                                                     |
| chaos                            | 28.9 ms                                                  | 28.7 ms: 1.01x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 57.1 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 100 ms: 1.01x slower                                                     |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                     |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.85 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 204 ms: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 681 ms: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 22.6 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.4 ms: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                   |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.44 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.5 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.9 ms: 1.07x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.4 ms: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 904 us: 1.09x slower                                                     |
| fannkuch                         | 176 ms                                                   | 192 ms: 1.09x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.04 ms: 1.13x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.08 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 135 ms: 1.19x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.13 ms: 1.20x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.0 ms: 2.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (3): genshi_text, richards_super, pycparser
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250325-3.14.0a6+-96ef4c5/bm-20250325-macm4pro-arm64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 99.90% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x