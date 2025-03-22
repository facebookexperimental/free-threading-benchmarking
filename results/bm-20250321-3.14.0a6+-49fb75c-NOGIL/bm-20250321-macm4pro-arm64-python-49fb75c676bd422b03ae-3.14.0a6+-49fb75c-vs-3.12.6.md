# Results vs. 3.12.6

- fork: python
- ref: 49fb75c676bd422b03ae
- machine: darwin-arm64
- commit hash: 49fb75c
- commit date: 2025-03-21
- overall geometric mean: 1.020x slower
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                    |
| sphinx         | 434 ms                                                   | 440 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.8 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 12.3 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.09x faster                                                     |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 56.1 ms: 1.23x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 36.0 ms: 1.05x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| nbody          | 54.2 ms                                                  | 78.0 ms: 1.44x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 59.2 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 41.0 ms: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 30.6 ms: 1.14x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 170 us: 1.22x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.21 ms: 1.22x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 128 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.25 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.4 ms: 1.21x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| mako            | 4.77 ms                                                  | 6.18 ms: 1.30x slower                                                    |
| django_template | 13.6 ms                                                  | 18.3 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.43 ms: 2.20x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 936 us: 2.14x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 99.8 ms: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 511 us: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| deepcopy                         | 161 us                                                   | 128 us: 1.26x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.9 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 844 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 12.3 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.09x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.7 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.1 ms: 1.07x faster                                                    |
| async_generators                 | 206 ms                                                   | 193 ms: 1.07x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.06x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 17.3 us: 1.06x faster                                                    |
| float                            | 37.9 ms                                                  | 36.0 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.39 us: 1.05x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.67 ms: 1.01x slower                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.26 sec: 1.01x slower                                                   |
| generators                       | 21.9 ms                                                  | 22.2 ms: 1.01x slower                                                    |
| sphinx                           | 434 ms                                                   | 440 ms: 1.01x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 40.4 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 508 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| comprehensions                   | 9.84 us                                                  | 10.2 us: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 41.0 ms: 1.05x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                    |
| go                               | 70.0 ms                                                  | 75.3 ms: 1.07x slower                                                    |
| thrift                           | 322 us                                                   | 346 us: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 122 ms: 1.08x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 59.2 ms: 1.08x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 55.3 ns: 1.09x slower                                                    |
| pyflate                          | 216 ms                                                   | 235 ms: 1.09x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 59.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 234 ms: 1.10x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.20 sec: 1.10x slower                                                   |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.5 ms: 1.10x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 63.7 ms: 1.11x slower                                                    |
| raytrace                         | 145 ms                                                   | 163 ms: 1.12x slower                                                     |
| logging_format                   | 2.80 us                                                  | 3.16 us: 1.13x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.08 sec: 1.13x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.90 us: 1.13x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 69.1 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 9.10 ms: 1.13x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 49.6 ms: 1.14x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.92 ms: 1.14x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 30.6 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 81.2 us: 1.14x slower                                                    |
| sympy_str                        | 104 ms                                                   | 119 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.25 ms: 1.15x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 164 ms: 1.15x slower                                                     |
| chaos                            | 28.9 ms                                                  | 33.4 ms: 1.16x slower                                                    |
| 2to3                             | 114 ms                                                   | 132 ms: 1.16x slower                                                     |
| connected_components             | 201 ms                                                   | 236 ms: 1.17x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 2.03 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.51 ms: 1.21x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 202 ms: 1.21x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 26.4 ms: 1.21x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 47.2 ms: 1.22x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 170 us: 1.22x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.21 ms: 1.22x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 56.1 ms: 1.23x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 31.5 ms: 1.24x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 128 us: 1.25x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 59.6 ms: 1.25x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.4 ms: 1.25x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 13.2 ms: 1.26x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 414 ms: 1.26x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 845 ms: 1.27x slower                                                     |
| richards                         | 22.4 ms                                                  | 28.5 ms: 1.27x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                    |
| fannkuch                         | 176 ms                                                   | 226 ms: 1.29x slower                                                     |
| mako                             | 4.77 ms                                                  | 6.18 ms: 1.30x slower                                                    |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.98 ms: 1.31x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 68.4 ms: 1.33x slower                                                    |
| django_template                  | 13.6 ms                                                  | 18.3 ms: 1.35x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.61 ms: 1.38x slower                                                    |
| nbody                            | 54.2 ms                                                  | 78.0 ms: 1.44x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 618 us: 1.48x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.0 ms: 2.74x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, async_tree_eager_cpu_io_mixed
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-49fb75c-NOGIL/bm-20250321-macm4pro-arm64-python-49fb75c676bd422b03ae-3.14.0a6+-49fb75c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.69% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x