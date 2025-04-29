# Results vs. 3.13.0rc2

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.022x faster
- HPT reliability: 53.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                                |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                              |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                               |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                          | 1.02x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                                |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                                |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                                |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                                |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                                |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                                |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                                |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                                |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                                                |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                                |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                                |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                               |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                                |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                                                |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                                |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.5 ms: 3.06x slower                                                               |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                               |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                                |
| nbody          | 42.5 ms                                                        | 51.3 ms: 1.21x slower                                                               |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                               |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                               |
| regex_compile  | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                               |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                                |
| Geometric mean | (ref)                                                          | 1.01x faster                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 918 ms: 1.09x faster                                                                |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                               |
| unpickle_pure_python | 99.5 us                                                        | 100 us: 1.01x slower                                                                |
| xml_etree_generate   | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                               |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                               |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                               |
| json_dumps           | 4.65 ms                                                        | 5.01 ms: 1.08x slower                                                               |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                                |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                                        |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                               |
| python_startup_no_site | 5.95 ms                                                        | 6.16 ms: 1.03x slower                                                               |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                               |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                               |
| django_template | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                               |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                        |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 246 ms: 2.14x faster                                                                |
| async_tree_eager_io_tg           | 521 ms                                                         | 251 ms: 2.08x faster                                                                |
| mdp                              | 1.06 sec                                                       | 527 ms: 2.01x faster                                                                |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                                |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                                |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                                |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                                |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                               |
| go                               | 72.6 ms                                                        | 56.4 ms: 1.29x faster                                                               |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.26x faster                                                                |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.26x faster                                                                |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                                |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                                |
| scimark_sor                      | 64.0 ms                                                        | 51.9 ms: 1.23x faster                                                               |
| deepcopy_reduce                  | 1.30 us                                                        | 1.10 us: 1.17x faster                                                               |
| pyflate                          | 222 ms                                                         | 196 ms: 1.13x faster                                                                |
| async_generators                 | 193 ms                                                         | 171 ms: 1.13x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.11x faster                                                                |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                               |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                                |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.10x faster                                                                |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                              |
| tomli_loads                      | 1000 ms                                                        | 918 ms: 1.09x faster                                                                |
| create_gc_cycles                 | 993 us                                                         | 915 us: 1.09x faster                                                                |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                               |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.08x faster                                                               |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                               |
| connected_components             | 208 ms                                                         | 199 ms: 1.04x faster                                                                |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                                |
| async_tree_eager                 | 43.2 ms                                                        | 41.5 ms: 1.04x faster                                                               |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                               |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                               |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                               |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                               |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                                |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                                |
| asyncio_websockets               | 194 ms                                                         | 193 ms: 1.01x faster                                                                |
| regex_compile                    | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                               |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                                |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                              |
| unpickle_pure_python             | 99.5 us                                                        | 100 us: 1.01x slower                                                                |
| xml_etree_generate               | 35.8 ms                                                        | 36.1 ms: 1.01x slower                                                               |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                               |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                                |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                               |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                                |
| nqueens                          | 37.2 ms                                                        | 38.0 ms: 1.02x slower                                                               |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.02x slower                                                               |
| deltablue                        | 1.45 ms                                                        | 1.49 ms: 1.03x slower                                                               |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                               |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                                |
| sympy_str                        | 95.5 ms                                                        | 98.4 ms: 1.03x slower                                                               |
| python_startup                   | 8.63 ms                                                        | 8.92 ms: 1.03x slower                                                               |
| python_startup_no_site           | 5.95 ms                                                        | 6.16 ms: 1.03x slower                                                               |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.0 ms: 1.04x slower                                                               |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                                |
| pprint_pformat                   | 650 ms                                                         | 679 ms: 1.04x slower                                                                |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                               |
| pycparser                        | 470 ms                                                         | 496 ms: 1.05x slower                                                                |
| meteor_contest                   | 47.9 ms                                                        | 50.6 ms: 1.06x slower                                                               |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                                |
| bench_mp_pool                    | 37.8 ms                                                        | 40.3 ms: 1.07x slower                                                               |
| bench_thread_pool                | 412 us                                                         | 440 us: 1.07x slower                                                                |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                               |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                               |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                               |
| logging_format                   | 2.45 us                                                        | 2.63 us: 1.08x slower                                                               |
| json_dumps                       | 4.65 ms                                                        | 5.01 ms: 1.08x slower                                                               |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                                |
| spectral_norm                    | 43.7 ms                                                        | 47.3 ms: 1.08x slower                                                               |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                                |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                               |
| pylint                           | 106 ms                                                         | 116 ms: 1.09x slower                                                                |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.47 ms: 1.09x slower                                                               |
| coverage                         | 31.2 ms                                                        | 34.3 ms: 1.10x slower                                                               |
| comprehensions                   | 6.80 us                                                        | 7.51 us: 1.10x slower                                                               |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.97 ms: 1.11x slower                                                               |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                               |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                                |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                               |
| scimark_lu                       | 42.8 ms                                                        | 48.6 ms: 1.14x slower                                                               |
| crypto_pyaes                     | 33.6 ms                                                        | 38.3 ms: 1.14x slower                                                               |
| many_optionals                   | 200 us                                                         | 236 us: 1.18x slower                                                                |
| django_template                  | 12.5 ms                                                        | 15.0 ms: 1.20x slower                                                               |
| nbody                            | 42.5 ms                                                        | 51.3 ms: 1.21x slower                                                               |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 257 ms: 1.24x slower                                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                                |
| subparsers                       | 6.26 ms                                                        | 8.84 ms: 1.41x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.5 ms: 3.06x slower                                                               |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                                        |

Benchmark hidden because not significant (9): richards, richards_super, genshi_text, pathlib, sympy_integrate, sqlite_synth, xml_etree_process, typing_runtime_protocols, logging_silent
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250429-3.14.0a7+-39f987b/bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 53.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x