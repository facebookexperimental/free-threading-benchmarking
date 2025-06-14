# Results vs. 3.12.6

- fork: python
- ref: 56eabea056ae1da49b55
- machine: darwin-arm64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.082x faster
- HPT reliability: 92.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 423 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 991 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 813 us: 2.47x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 208 ms: 2.39x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.89 ms: 2.10x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 568 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.69x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 496 us: 1.67x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.33x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.31x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.01 us: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                    |
| go                               | 70.0 ms                                                  | 62.6 ms: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.3 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.4 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.02x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 53.2 ms: 1.02x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.69 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 54.0 ms: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.07 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 533 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.08 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.4 us: 1.03x slower                                                   |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 991 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.9 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.82 us: 1.10x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.6 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.1 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 224 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.5 ms: 1.12x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.14 us: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.7 ms: 1.15x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 380 ms: 1.16x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 775 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.69 ms: 1.19x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 62.1 ms: 1.21x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.78 ms: 1.22x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.09 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.9 ms: 2.45x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 219 ns: 4.31x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (3): regex_dna, asyncio_websockets, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 92.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x