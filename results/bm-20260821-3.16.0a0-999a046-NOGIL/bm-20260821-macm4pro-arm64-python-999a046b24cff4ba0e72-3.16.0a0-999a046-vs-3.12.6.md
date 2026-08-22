# Results vs. 3.12.6

- fork: python
- ref: 999a046b24cff4ba0e72
- machine: darwin-arm64
- commit hash: 999a046
- commit date: 2026-08-21
- overall geometric mean: 1.015x faster
- HPT reliability: 71.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 136 ms: 1.19x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 313 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 307 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 318 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 191 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.0 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.71x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| nbody          | 54.2 ms                                                  | 62.0 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.06 ms: 1.06x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 68.7 ms: 1.26x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| tomli_loads          | 957 ms                                                   | 946 ms: 1.01x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 116 us: 1.13x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 31.4 ms: 1.18x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 164 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                   |
| django_template | 13.6 ms                                                  | 17.7 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.25x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.55 ms: 4.56x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| pylint                           | 128 ms                                                   | 54.5 ms: 2.35x faster                                                   |
| mdp                              | 1.09 sec                                                 | 618 ms: 1.77x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 312 ms: 1.59x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 313 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 307 ms: 1.45x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 318 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_generators                 | 206 ms                                                   | 164 ms: 1.26x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 186 ms: 1.24x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.0 us: 1.22x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 148 ms: 1.21x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 814 ns: 1.19x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.3 us: 1.18x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 147 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.2 ms: 1.17x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 191 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.71 us: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 301 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 307 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 92.5 ms: 1.08x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                   |
| float                            | 37.9 ms                                                  | 35.3 ms: 1.07x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.06 ms: 1.06x faster                                                   |
| go                               | 70.0 ms                                                  | 66.4 ms: 1.05x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 128 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| pyflate                          | 216 ms                                                   | 212 ms: 1.02x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 946 ms: 1.01x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 61.4 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 43.9 ms: 1.01x slower                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                   |
| coroutines                       | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.87 us: 1.02x slower                                                   |
| pycparser                        | 497 ms                                                   | 512 ms: 1.03x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                   |
| sphinx                           | 434 ms                                                   | 461 ms: 1.06x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.56 ms: 1.07x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.10 sec: 1.07x slower                                                  |
| fannkuch                         | 176 ms                                                   | 190 ms: 1.08x slower                                                    |
| raytrace                         | 145 ms                                                   | 158 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.3 ms: 1.09x slower                                                   |
| chaos                            | 28.9 ms                                                  | 31.6 ms: 1.09x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.3 ms: 1.10x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 63.1 ms: 1.10x slower                                                   |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| thrift                           | 322 us                                                   | 360 us: 1.12x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 368 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 116 us: 1.13x slower                                                    |
| generators                       | 21.9 ms                                                  | 24.8 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.2 ms: 1.14x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 756 ms: 1.14x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 52.0 ms: 1.14x slower                                                   |
| nbody                            | 54.2 ms                                                  | 62.0 ms: 1.14x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.54 ms: 1.16x slower                                                   |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.17x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 196 ms: 1.17x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 31.4 ms: 1.18x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 164 us: 1.18x slower                                                    |
| 2to3                             | 114 ms                                                   | 136 ms: 1.19x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 30.6 ms: 1.20x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.15 ms: 1.21x slower                                                   |
| richards                         | 22.4 ms                                                  | 27.1 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                   |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 68.7 ms: 1.26x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 2.22 ms: 1.29x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.7 ms: 1.30x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 280 ms: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                    |
| many_optionals                   | 195 us                                                   | 272 us: 1.39x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 72.1 ms: 1.41x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 159 ms: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 41.4 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 119 ms: 3.71x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (2): spectral_norm, logging_silent
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260821-3.16.0a0-999a046-NOGIL/bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.015x faster

# HPT report

- Reliability score: 71.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x