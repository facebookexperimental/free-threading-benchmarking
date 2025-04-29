# Results vs. 3.12.6

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                                |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                              |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                               |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                                |
| Geometric mean | (ref)                                                    | 1.00x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                                |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                                |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                                |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                                |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                                |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                                |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                                |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                                |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                                |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                                |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                                |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                                |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                                |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                                |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                                |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.5 ms: 2.75x slower                                                               |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                               |
| nbody          | 54.2 ms                                                  | 51.3 ms: 1.06x faster                                                               |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                                |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                               |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                               |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.03x slower                                                                |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                                               |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                               |
| xml_etree_parse      | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                               |
| xml_etree_generate   | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                               |
| xml_etree_process    | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                               |
| tomli_loads          | 957 ms                                                   | 918 ms: 1.04x faster                                                                |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                                |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                                |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                               |
| json_dumps           | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                               |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.16 ms: 1.08x slower                                                               |
| python_startup         | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                               |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.96 ms: 1.05x faster                                                               |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                               |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                               |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                               |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                                        |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.84 ms: 2.35x faster                                                               |
| mdp                              | 1.09 sec                                                 | 527 ms: 2.07x faster                                                                |
| async_tree_eager_io              | 496 ms                                                   | 246 ms: 2.02x faster                                                                |
| async_tree_io_tg                 | 480 ms                                                   | 249 ms: 1.93x faster                                                                |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                                |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                                |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                                |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                                |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.56x faster                                                                |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                                |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                                |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                               |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                               |
| deepcopy_reduce                  | 1.46 us                                                  | 1.10 us: 1.32x faster                                                               |
| comprehensions                   | 9.84 us                                                  | 7.51 us: 1.31x faster                                                               |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                                |
| logging_silent                   | 50.9 ns                                                  | 40.8 ns: 1.25x faster                                                               |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                                |
| go                               | 70.0 ms                                                  | 56.4 ms: 1.24x faster                                                               |
| generators                       | 21.9 ms                                                  | 17.8 ms: 1.23x faster                                                               |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                                |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                                |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.19x faster                                                               |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                                |
| scimark_sor                      | 61.0 ms                                                  | 51.9 ms: 1.17x faster                                                               |
| k_core                           | 1.12 sec                                                 | 954 ms: 1.17x faster                                                                |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.6 ms: 1.16x faster                                                               |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                               |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                              |
| spectral_norm                    | 54.4 ms                                                  | 47.3 ms: 1.15x faster                                                               |
| nqueens                          | 43.5 ms                                                  | 38.0 ms: 1.14x faster                                                               |
| regex_compile                    | 54.6 ms                                                  | 48.2 ms: 1.13x faster                                                               |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                               |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                               |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                                |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                                |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                               |
| async_tree_eager                 | 45.6 ms                                                  | 41.5 ms: 1.10x faster                                                               |
| chaos                            | 28.9 ms                                                  | 26.4 ms: 1.09x faster                                                               |
| hexiom                           | 3.04 ms                                                  | 2.78 ms: 1.09x faster                                                               |
| typing_runtime_protocols         | 71.0 us                                                  | 64.9 us: 1.09x faster                                                               |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                                |
| xml_etree_parse                  | 67.9 ms                                                  | 63.0 ms: 1.08x faster                                                               |
| xml_etree_generate               | 38.9 ms                                                  | 36.1 ms: 1.08x faster                                                               |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                               |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.07x faster                                                               |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.06x faster                                                               |
| sympy_str                        | 104 ms                                                   | 98.4 ms: 1.06x faster                                                               |
| nbody                            | 54.2 ms                                                  | 51.3 ms: 1.06x faster                                                               |
| scimark_lu                       | 51.3 ms                                                  | 48.6 ms: 1.06x faster                                                               |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.97 ms: 1.06x faster                                                               |
| genshi_text                      | 10.5 ms                                                  | 9.96 ms: 1.05x faster                                                               |
| xml_etree_process                | 26.7 ms                                                  | 25.4 ms: 1.05x faster                                                               |
| tomli_loads                      | 957 ms                                                   | 918 ms: 1.04x faster                                                                |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                                |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                                |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                               |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                               |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                                |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                               |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                                |
| sqlalchemy_declarative           | 46.8 ms                                                  | 46.0 ms: 1.02x faster                                                               |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                                |
| crypto_pyaes                     | 38.8 ms                                                  | 38.3 ms: 1.01x faster                                                               |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                                |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                                |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                               |
| pprint_safe_repr                 | 328 ms                                                   | 331 ms: 1.01x slower                                                                |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                                |
| bench_mp_pool                    | 39.7 ms                                                  | 40.3 ms: 1.02x slower                                                               |
| pprint_pformat                   | 665 ms                                                   | 679 ms: 1.02x slower                                                                |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                                |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                               |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.03x slower                                                                |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                              |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                               |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                               |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                                |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                                |
| bench_thread_pool                | 419 us                                                   | 440 us: 1.05x slower                                                                |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                               |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.47 ms: 1.06x slower                                                               |
| meteor_contest                   | 47.7 ms                                                  | 50.6 ms: 1.06x slower                                                               |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                               |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.08x slower                                                               |
| python_startup_no_site           | 5.71 ms                                                  | 6.16 ms: 1.08x slower                                                               |
| create_gc_cycles                 | 830 us                                                   | 915 us: 1.10x slower                                                                |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                               |
| python_startup                   | 8.01 ms                                                  | 8.92 ms: 1.11x slower                                                               |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                               |
| json_dumps                       | 4.26 ms                                                  | 5.01 ms: 1.18x slower                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 133 ms: 1.18x slower                                                                |
| many_optionals                   | 195 us                                                   | 236 us: 1.21x slower                                                                |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                                |
| coverage                         | 26.9 ms                                                  | 34.3 ms: 1.27x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.5 ms: 2.75x slower                                                               |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                                        |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250429-3.14.0a7+-39f987b/bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.12x