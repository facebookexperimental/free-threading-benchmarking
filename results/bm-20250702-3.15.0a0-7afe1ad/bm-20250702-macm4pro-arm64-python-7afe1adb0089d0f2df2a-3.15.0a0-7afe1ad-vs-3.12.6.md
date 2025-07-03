# Results vs. 3.12.6

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: darwin-arm64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 255 ms: 1.88x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.78x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 173 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 909 ms: 1.05x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.04x faster                                                   |
| mako            | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 514 ms: 2.12x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.86 ms: 2.11x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 252 ms: 1.97x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 255 ms: 1.88x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 257 ms: 1.79x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 150 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.46x faster                                                   |
| deepcopy                         | 161 us                                                   | 112 us: 1.45x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.93 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.37 us: 1.34x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 39.7 ns: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.5 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.4 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 957 ms: 1.17x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.5 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 62.6 us: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.7 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.88 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.39 us: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.4 ms: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.1 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.4 us: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.05x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 909 ms: 1.05x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.5 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.7 ms: 1.01x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.1 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.2 ms: 1.01x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 99.2 ms: 1.00x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                    |
| connected_components             | 201 ms                                                   | 203 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.7 ms: 1.02x slower                                                   |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.85 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.94 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| json_dumps                       | 4.26 ms                                                  | 4.49 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                    |
| pidigits                         | 161 ms                                                   | 173 ms: 1.07x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.16 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.16x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 969 us: 1.17x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.2 ms: 2.78x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (6): json, sqlite_synth, genshi_xml, shortest_path, sympy_expand, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x