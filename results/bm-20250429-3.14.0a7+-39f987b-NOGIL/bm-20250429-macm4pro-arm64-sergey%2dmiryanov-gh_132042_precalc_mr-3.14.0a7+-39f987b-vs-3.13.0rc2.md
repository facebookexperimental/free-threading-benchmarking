# Results vs. 3.13.0rc2

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.008x faster
- HPT reliability: 82.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                                |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                              |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                               |
| sphinx         | 409 ms                                                         | 428 ms: 1.05x slower                                                                |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                                |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                                |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                                |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                                |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                               |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                                |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                                |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                                |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                                |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                                |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                                |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                               |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                                |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                                |
| async_tree_eager                 | 43.2 ms                                                        | 50.5 ms: 1.17x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                               |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                               |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                                |
| nbody          | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                               |
| Geometric mean | (ref)                                                          | 1.06x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                               |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                               |
| regex_dna      | 94.6 ms                                                        | 104 ms: 1.10x slower                                                                |
| regex_compile  | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                               |
| Geometric mean | (ref)                                                          | 1.01x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.3 ms: 1.27x faster                                                               |
| xml_etree_parse      | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                               |
| tomli_loads          | 1000 ms                                                        | 989 ms: 1.01x faster                                                                |
| xml_etree_generate   | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                               |
| xml_etree_process    | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                               |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                                |
| json_dumps           | 4.65 ms                                                        | 5.22 ms: 1.12x slower                                                               |
| json_loads           | 10.8 us                                                        | 12.5 us: 1.16x slower                                                               |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                                |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                               |
| python_startup_no_site | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                               |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                               |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                               |
| mako            | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                               |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                               |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                                        |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 195 ms: 2.67x faster                                                                |
| gc_traversal                     | 2.04 ms                                                        | 768 us: 2.66x faster                                                                |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.55x faster                                                                |
| create_gc_cycles                 | 993 us                                                         | 459 us: 2.16x faster                                                                |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                                |
| mdp                              | 1.06 sec                                                       | 573 ms: 1.84x faster                                                                |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                                |
| async_tree_none_tg               | 133 ms                                                         | 86.0 ms: 1.54x faster                                                               |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                                |
| k_core                           | 1.46 sec                                                       | 994 ms: 1.47x faster                                                                |
| async_tree_memoization           | 184 ms                                                         | 132 ms: 1.40x faster                                                                |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 233 ms: 1.29x faster                                                                |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.3 ms: 1.27x faster                                                               |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 242 ms: 1.21x faster                                                                |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                               |
| deepcopy                         | 145 us                                                         | 124 us: 1.17x faster                                                                |
| scimark_sor                      | 64.0 ms                                                        | 55.0 ms: 1.16x faster                                                               |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                                |
| go                               | 72.6 ms                                                        | 63.5 ms: 1.14x faster                                                               |
| float                            | 31.4 ms                                                        | 28.0 ms: 1.12x faster                                                               |
| xml_etree_parse                  | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                               |
| pyflate                          | 222 ms                                                         | 203 ms: 1.09x faster                                                                |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                                |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                                |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                              |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                               |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                               |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                               |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                               |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                              |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                                |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                               |
| tomli_loads                      | 1000 ms                                                        | 989 ms: 1.01x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                                |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                                |
| xml_etree_generate               | 35.8 ms                                                        | 37.0 ms: 1.03x slower                                                               |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                               |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                                |
| sphinx                           | 409 ms                                                         | 428 ms: 1.05x slower                                                                |
| json                             | 1.94 ms                                                        | 2.04 ms: 1.05x slower                                                               |
| xml_etree_process                | 25.4 ms                                                        | 26.7 ms: 1.05x slower                                                               |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                               |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                                |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                                |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                                |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                               |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                                |
| logging_silent                   | 40.6 ns                                                        | 44.2 ns: 1.09x slower                                                               |
| regex_dna                        | 94.6 ms                                                        | 104 ms: 1.10x slower                                                                |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                                |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                                |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                                |
| python_startup                   | 8.63 ms                                                        | 9.48 ms: 1.10x slower                                                               |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                               |
| regex_compile                    | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                               |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.11x slower                                                               |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                               |
| nqueens                          | 37.2 ms                                                        | 41.4 ms: 1.11x slower                                                               |
| richards                         | 22.1 ms                                                        | 24.6 ms: 1.12x slower                                                               |
| pprint_safe_repr                 | 322 ms                                                         | 360 ms: 1.12x slower                                                                |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                               |
| json_dumps                       | 4.65 ms                                                        | 5.22 ms: 1.12x slower                                                               |
| pprint_pformat                   | 650 ms                                                         | 733 ms: 1.13x slower                                                                |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                               |
| richards_super                   | 24.7 ms                                                        | 28.3 ms: 1.15x slower                                                               |
| typing_runtime_protocols         | 64.6 us                                                        | 74.3 us: 1.15x slower                                                               |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                               |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                                |
| json_loads                       | 10.8 us                                                        | 12.5 us: 1.16x slower                                                               |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.6 ms: 1.16x slower                                                               |
| python_startup_no_site           | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                               |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                                |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.17x slower                                                                |
| async_tree_eager                 | 43.2 ms                                                        | 50.5 ms: 1.17x slower                                                               |
| spectral_norm                    | 43.7 ms                                                        | 51.7 ms: 1.18x slower                                                               |
| meteor_contest                   | 47.9 ms                                                        | 56.7 ms: 1.18x slower                                                               |
| chaos                            | 24.3 ms                                                        | 28.7 ms: 1.18x slower                                                               |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                                |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.19x slower                                                               |
| logging_simple                   | 2.24 us                                                        | 2.66 us: 1.19x slower                                                               |
| sympy_sum                        | 52.3 ms                                                        | 62.2 ms: 1.19x slower                                                               |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.95 ms: 1.19x slower                                                               |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                                |
| logging_format                   | 2.45 us                                                        | 2.94 us: 1.20x slower                                                               |
| generators                       | 15.7 ms                                                        | 19.1 ms: 1.22x slower                                                               |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                                |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                               |
| mako                             | 4.41 ms                                                        | 5.59 ms: 1.27x slower                                                               |
| comprehensions                   | 6.80 us                                                        | 8.65 us: 1.27x slower                                                               |
| scimark_lu                       | 42.8 ms                                                        | 55.5 ms: 1.30x slower                                                               |
| coverage                         | 31.2 ms                                                        | 40.8 ms: 1.31x slower                                                               |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.31x slower                                                               |
| nbody                            | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                               |
| subparsers                       | 6.26 ms                                                        | 9.05 ms: 1.45x slower                                                               |
| bench_thread_pool                | 412 us                                                         | 600 us: 1.46x slower                                                                |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.9 ms: 2.69x slower                                                               |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                                        |

Benchmark hidden because not significant (2): pathlib, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 82.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x