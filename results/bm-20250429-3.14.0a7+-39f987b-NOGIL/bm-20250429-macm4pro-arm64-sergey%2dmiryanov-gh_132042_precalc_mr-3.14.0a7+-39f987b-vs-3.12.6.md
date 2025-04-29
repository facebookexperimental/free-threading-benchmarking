# Results vs. 3.12.6

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.087x faster
- HPT reliability: 90.68%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.07x slower                                                                |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                              |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                               |
| sphinx         | 434 ms                                                   | 428 ms: 1.01x faster                                                                |
| Geometric mean | (ref)                                                    | 1.02x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                                |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                                |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                                |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                                |
| async_tree_none_tg               | 172 ms                                                   | 86.0 ms: 2.00x faster                                                               |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                                |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                                |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                                |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.37x faster                                                                |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                               |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                                |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                                |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                                |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                               |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                                        |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                               |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                               |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                                |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                               |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                               |
| regex_dna      | 99.6 ms                                                  | 104 ms: 1.04x slower                                                                |
| regex_v8       | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                               |
| Geometric mean | (ref)                                                    | 1.01x faster                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.3 ms: 1.42x faster                                                               |
| xml_etree_parse      | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                               |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                               |
| tomli_loads          | 957 ms                                                   | 989 ms: 1.03x slower                                                                |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                                |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                                |
| json_loads           | 10.9 us                                                  | 12.5 us: 1.15x slower                                                               |
| json_dumps           | 4.26 ms                                                  | 5.22 ms: 1.23x slower                                                               |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                                        |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                               |
| python_startup_no_site | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                               |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                               |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                               |
| mako            | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                               |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                               |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                                        |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.61x faster                                                                |
| async_tree_io_tg                 | 480 ms                                                   | 196 ms: 2.45x faster                                                                |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                                |
| subparsers                       | 20.8 ms                                                  | 9.05 ms: 2.29x faster                                                               |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                                |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                                |
| async_tree_none_tg               | 172 ms                                                   | 86.0 ms: 2.00x faster                                                               |
| mdp                              | 1.09 sec                                                 | 573 ms: 1.90x faster                                                                |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                                |
| create_gc_cycles                 | 830 us                                                   | 459 us: 1.81x faster                                                                |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                                |
| async_tree_memoization           | 223 ms                                                   | 132 ms: 1.69x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 233 ms: 1.45x faster                                                                |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.3 ms: 1.42x faster                                                               |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.37x faster                                                                |
| float                            | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                               |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                               |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                               |
| deepcopy                         | 161 us                                                   | 124 us: 1.30x faster                                                                |
| xml_etree_parse                  | 67.9 ms                                                  | 56.8 ms: 1.20x faster                                                               |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                                |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                                |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                                |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                               |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                               |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                               |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                              |
| comprehensions                   | 9.84 us                                                  | 8.65 us: 1.14x faster                                                               |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                                |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                                |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                                                |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                               |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                               |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                               |
| go                               | 70.0 ms                                                  | 63.5 ms: 1.10x faster                                                               |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                               |
| pyflate                          | 216 ms                                                   | 203 ms: 1.06x faster                                                                |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                                |
| spectral_norm                    | 54.4 ms                                                  | 51.7 ms: 1.05x faster                                                               |
| nqueens                          | 43.5 ms                                                  | 41.4 ms: 1.05x faster                                                               |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                               |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                                |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                               |
| sphinx                           | 434 ms                                                   | 428 ms: 1.01x faster                                                                |
| chaos                            | 28.9 ms                                                  | 28.7 ms: 1.01x faster                                                               |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                              |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                               |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                               |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.02x slower                                                                |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.03x slower                                                               |
| tomli_loads                      | 957 ms                                                   | 989 ms: 1.03x slower                                                                |
| logging_simple                   | 2.57 us                                                  | 2.66 us: 1.03x slower                                                               |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                               |
| regex_dna                        | 99.6 ms                                                  | 104 ms: 1.04x slower                                                                |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                               |
| regex_v8                         | 9.59 ms                                                  | 10.0 ms: 1.04x slower                                                               |
| typing_runtime_protocols         | 71.0 us                                                  | 74.3 us: 1.05x slower                                                               |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                                |
| logging_format                   | 2.80 us                                                  | 2.94 us: 1.05x slower                                                               |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                               |
| json                             | 1.93 ms                                                  | 2.04 ms: 1.05x slower                                                               |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.06x slower                                                               |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                                |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                                |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                                |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.07x slower                                                                |
| 2to3                             | 114 ms                                                   | 123 ms: 1.07x slower                                                                |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                               |
| sympy_sum                        | 57.6 ms                                                  | 62.2 ms: 1.08x slower                                                               |
| scimark_lu                       | 51.3 ms                                                  | 55.5 ms: 1.08x slower                                                               |
| fannkuch                         | 176 ms                                                   | 190 ms: 1.08x slower                                                                |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                                |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                               |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                               |
| richards                         | 22.4 ms                                                  | 24.6 ms: 1.10x slower                                                               |
| pprint_safe_repr                 | 328 ms                                                   | 360 ms: 1.10x slower                                                                |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                                |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.6 ms: 1.10x slower                                                               |
| pprint_pformat                   | 665 ms                                                   | 733 ms: 1.10x slower                                                                |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                               |
| richards_super                   | 25.4 ms                                                  | 28.3 ms: 1.11x slower                                                               |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                                |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.95 ms: 1.15x slower                                                               |
| json_loads                       | 10.9 us                                                  | 12.5 us: 1.15x slower                                                               |
| mako                             | 4.77 ms                                                  | 5.59 ms: 1.17x slower                                                               |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                               |
| meteor_contest                   | 47.7 ms                                                  | 56.7 ms: 1.19x slower                                                               |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                               |
| python_startup_no_site           | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                               |
| json_dumps                       | 4.26 ms                                                  | 5.22 ms: 1.23x slower                                                               |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                               |
| many_optionals                   | 195 us                                                   | 249 us: 1.28x slower                                                                |
| bench_thread_pool                | 419 us                                                   | 600 us: 1.43x slower                                                                |
| coverage                         | 26.9 ms                                                  | 40.8 ms: 1.52x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                               |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                                        |

Benchmark hidden because not significant (3): asyncio_websockets, xml_etree_process, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 90.68% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x