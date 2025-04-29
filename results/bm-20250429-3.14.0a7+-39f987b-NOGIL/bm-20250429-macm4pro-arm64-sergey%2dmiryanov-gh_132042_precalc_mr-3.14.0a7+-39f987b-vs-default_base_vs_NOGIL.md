# Results vs. default_base_vs_NOGIL

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: darwin-arm64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.008x slower
- HPT reliability: 98.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                   | 123 ms: 1.07x slower                                                                |
| docutils       | 1.07 sec                                                                 | 1.02 sec: 1.05x faster                                                              |
| html5lib       | 24.6 ms                                                                  | 24.0 ms: 1.03x faster                                                               |
| sphinx         | 416 ms                                                                   | 428 ms: 1.03x slower                                                                |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 258 ms                                                                   | 195 ms: 1.32x faster                                                                |
| async_tree_io_tg                 | 252 ms                                                                   | 196 ms: 1.29x faster                                                                |
| async_tree_none_tg               | 107 ms                                                                   | 86.0 ms: 1.24x faster                                                               |
| async_tree_eager_io              | 250 ms                                                                   | 206 ms: 1.21x faster                                                                |
| async_tree_io                    | 255 ms                                                                   | 210 ms: 1.21x faster                                                                |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 113 ms: 1.20x faster                                                                |
| async_tree_memoization_tg        | 149 ms                                                                   | 125 ms: 1.19x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 274 ms                                                                   | 233 ms: 1.18x faster                                                                |
| async_tree_eager_tg              | 89.4 ms                                                                  | 77.9 ms: 1.15x faster                                                               |
| async_tree_eager_cpu_io_mixed_tg | 257 ms                                                                   | 225 ms: 1.15x faster                                                                |
| async_tree_cpu_io_mixed          | 276 ms                                                                   | 242 ms: 1.14x faster                                                                |
| async_tree_memoization           | 149 ms                                                                   | 132 ms: 1.13x faster                                                                |
| async_tree_none                  | 115 ms                                                                   | 102 ms: 1.12x faster                                                                |
| asyncio_websockets               | 194 ms                                                                   | 190 ms: 1.02x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 223 ms: 1.01x faster                                                                |
| coroutines                       | 10.3 ms                                                                  | 10.2 ms: 1.01x faster                                                               |
| async_generators                 | 175 ms                                                                   | 178 ms: 1.02x slower                                                                |
| async_tree_eager                 | 43.0 ms                                                                  | 50.5 ms: 1.17x slower                                                               |
| Geometric mean                   | (ref)                                                                    | 1.12x faster                                                                        |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 29.1 ms                                                                  | 28.0 ms: 1.04x faster                                                               |
| pidigits       | 170 ms                                                                   | 169 ms: 1.01x faster                                                                |
| nbody          | 49.3 ms                                                                  | 56.2 ms: 1.14x slower                                                               |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_v8       | 10.4 ms                                                                  | 10.0 ms: 1.04x faster                                                               |
| regex_effbot   | 1.50 ms                                                                  | 1.51 ms: 1.01x slower                                                               |
| regex_dna      | 102 ms                                                                   | 104 ms: 1.01x slower                                                                |
| regex_compile  | 49.0 ms                                                                  | 52.8 ms: 1.08x slower                                                               |
| Geometric mean | (ref)                                                                    | 1.02x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 44.2 ms                                                                  | 36.3 ms: 1.22x faster                                                               |
| xml_etree_parse      | 62.6 ms                                                                  | 56.8 ms: 1.10x faster                                                               |
| xml_etree_generate   | 36.3 ms                                                                  | 37.0 ms: 1.02x slower                                                               |
| pickle_pure_python   | 146 us                                                                   | 152 us: 1.04x slower                                                                |
| json_dumps           | 5.00 ms                                                                  | 5.22 ms: 1.04x slower                                                               |
| xml_etree_process    | 25.4 ms                                                                  | 26.7 ms: 1.05x slower                                                               |
| tomli_loads          | 933 ms                                                                   | 989 ms: 1.06x slower                                                                |
| json_loads           | 11.7 us                                                                  | 12.5 us: 1.07x slower                                                               |
| unpickle_pure_python | 100 us                                                                   | 109 us: 1.09x slower                                                                |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 9.16 ms                                                                  | 9.48 ms: 1.04x slower                                                               |
| python_startup_no_site | 6.26 ms                                                                  | 6.92 ms: 1.11x slower                                                               |
| Geometric mean         | (ref)                                                                    | 1.07x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 15.3 ms                                                                  | 16.4 ms: 1.07x slower                                                               |
| genshi_xml      | 21.6 ms                                                                  | 23.5 ms: 1.09x slower                                                               |
| mako            | 4.97 ms                                                                  | 5.59 ms: 1.13x slower                                                               |
| genshi_text     | 10.0 ms                                                                  | 11.5 ms: 1.15x slower                                                               |
| Geometric mean  | (ref)                                                                    | 1.11x slower                                                                        |

All benchmarks:
===============

| Benchmark                        | bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7+-208d06f | bm-20250429-macm4pro-arm64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------------|:------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| gc_traversal                     | 2.13 ms                                                                  | 768 us: 2.77x faster                                                                |
| create_gc_cycles                 | 949 us                                                                   | 459 us: 2.07x faster                                                                |
| async_tree_eager_io_tg           | 258 ms                                                                   | 195 ms: 1.32x faster                                                                |
| async_tree_io_tg                 | 252 ms                                                                   | 196 ms: 1.29x faster                                                                |
| async_tree_none_tg               | 107 ms                                                                   | 86.0 ms: 1.24x faster                                                               |
| xml_etree_iterparse              | 44.2 ms                                                                  | 36.3 ms: 1.22x faster                                                               |
| async_tree_eager_io              | 250 ms                                                                   | 206 ms: 1.21x faster                                                                |
| async_tree_io                    | 255 ms                                                                   | 210 ms: 1.21x faster                                                                |
| async_tree_eager_memoization_tg  | 135 ms                                                                   | 113 ms: 1.20x faster                                                                |
| async_tree_memoization_tg        | 149 ms                                                                   | 125 ms: 1.19x faster                                                                |
| async_tree_cpu_io_mixed_tg       | 274 ms                                                                   | 233 ms: 1.18x faster                                                                |
| sqlite_synth                     | 954 ns                                                                   | 824 ns: 1.16x faster                                                                |
| async_tree_eager_tg              | 89.4 ms                                                                  | 77.9 ms: 1.15x faster                                                               |
| async_tree_eager_cpu_io_mixed_tg | 257 ms                                                                   | 225 ms: 1.15x faster                                                                |
| async_tree_cpu_io_mixed          | 276 ms                                                                   | 242 ms: 1.14x faster                                                                |
| async_tree_memoization           | 149 ms                                                                   | 132 ms: 1.13x faster                                                                |
| async_tree_none                  | 115 ms                                                                   | 102 ms: 1.12x faster                                                                |
| xml_etree_parse                  | 62.6 ms                                                                  | 56.8 ms: 1.10x faster                                                               |
| docutils                         | 1.07 sec                                                                 | 1.02 sec: 1.05x faster                                                              |
| pycparser                        | 494 ms                                                                   | 472 ms: 1.05x faster                                                                |
| float                            | 29.1 ms                                                                  | 28.0 ms: 1.04x faster                                                               |
| regex_v8                         | 10.4 ms                                                                  | 10.0 ms: 1.04x faster                                                               |
| html5lib                         | 24.6 ms                                                                  | 24.0 ms: 1.03x faster                                                               |
| asyncio_websockets               | 194 ms                                                                   | 190 ms: 1.02x faster                                                                |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                   | 223 ms: 1.01x faster                                                                |
| pidigits                         | 170 ms                                                                   | 169 ms: 1.01x faster                                                                |
| coroutines                       | 10.3 ms                                                                  | 10.2 ms: 1.01x faster                                                               |
| pathlib                          | 11.2 ms                                                                  | 11.1 ms: 1.01x faster                                                               |
| bench_mp_pool                    | 41.7 ms                                                                  | 41.9 ms: 1.00x slower                                                               |
| regex_effbot                     | 1.50 ms                                                                  | 1.51 ms: 1.01x slower                                                               |
| bpe_tokeniser                    | 1.94 sec                                                                 | 1.96 sec: 1.01x slower                                                              |
| pyflate                          | 201 ms                                                                   | 203 ms: 1.01x slower                                                                |
| regex_dna                        | 102 ms                                                                   | 104 ms: 1.01x slower                                                                |
| subparsers                       | 8.92 ms                                                                  | 9.05 ms: 1.02x slower                                                               |
| async_generators                 | 175 ms                                                                   | 178 ms: 1.02x slower                                                                |
| xml_etree_generate               | 36.3 ms                                                                  | 37.0 ms: 1.02x slower                                                               |
| json                             | 1.98 ms                                                                  | 2.04 ms: 1.03x slower                                                               |
| sphinx                           | 416 ms                                                                   | 428 ms: 1.03x slower                                                                |
| python_startup                   | 9.16 ms                                                                  | 9.48 ms: 1.04x slower                                                               |
| many_optionals                   | 241 us                                                                   | 249 us: 1.04x slower                                                                |
| pickle_pure_python               | 146 us                                                                   | 152 us: 1.04x slower                                                                |
| sqlglot_v2_normalize             | 46.9 ms                                                                  | 49.0 ms: 1.04x slower                                                               |
| json_dumps                       | 5.00 ms                                                                  | 5.22 ms: 1.04x slower                                                               |
| k_core                           | 949 ms                                                                   | 994 ms: 1.05x slower                                                                |
| xml_etree_process                | 25.4 ms                                                                  | 26.7 ms: 1.05x slower                                                               |
| dulwich_log                      | 18.1 ms                                                                  | 19.0 ms: 1.05x slower                                                               |
| deltablue                        | 1.56 ms                                                                  | 1.64 ms: 1.05x slower                                                               |
| pprint_safe_repr                 | 342 ms                                                                   | 360 ms: 1.06x slower                                                                |
| sqlglot_v2_optimize              | 22.9 ms                                                                  | 24.1 ms: 1.06x slower                                                               |
| tomli_loads                      | 933 ms                                                                   | 989 ms: 1.06x slower                                                                |
| pprint_pformat                   | 691 ms                                                                   | 733 ms: 1.06x slower                                                                |
| generators                       | 17.9 ms                                                                  | 19.1 ms: 1.07x slower                                                               |
| fannkuch                         | 178 ms                                                                   | 190 ms: 1.07x slower                                                                |
| json_loads                       | 11.7 us                                                                  | 12.5 us: 1.07x slower                                                               |
| 2to3                             | 114 ms                                                                   | 123 ms: 1.07x slower                                                                |
| django_template                  | 15.3 ms                                                                  | 16.4 ms: 1.07x slower                                                               |
| chaos                            | 26.8 ms                                                                  | 28.7 ms: 1.07x slower                                                               |
| logging_silent                   | 41.2 ns                                                                  | 44.2 ns: 1.07x slower                                                               |
| shortest_path                    | 217 ms                                                                   | 233 ms: 1.07x slower                                                                |
| go                               | 59.1 ms                                                                  | 63.5 ms: 1.07x slower                                                               |
| raytrace                         | 121 ms                                                                   | 130 ms: 1.07x slower                                                                |
| regex_compile                    | 49.0 ms                                                                  | 52.8 ms: 1.08x slower                                                               |
| scimark_sparse_mat_mult          | 1.95 ms                                                                  | 2.11 ms: 1.08x slower                                                               |
| sqlglot_v2_transpile             | 673 us                                                                   | 729 us: 1.08x slower                                                                |
| scimark_sor                      | 50.7 ms                                                                  | 55.0 ms: 1.08x slower                                                               |
| genshi_xml                       | 21.6 ms                                                                  | 23.5 ms: 1.09x slower                                                               |
| sqlglot_v2_parse                 | 550 us                                                                   | 597 us: 1.09x slower                                                                |
| sympy_integrate                  | 7.48 ms                                                                  | 8.14 ms: 1.09x slower                                                               |
| telco                            | 2.97 ms                                                                  | 3.23 ms: 1.09x slower                                                               |
| unpickle_pure_python             | 100 us                                                                   | 109 us: 1.09x slower                                                                |
| sqlalchemy_imperative            | 5.44 ms                                                                  | 5.95 ms: 1.09x slower                                                               |
| deepcopy_memo                    | 12.8 us                                                                  | 14.0 us: 1.09x slower                                                               |
| nqueens                          | 37.7 ms                                                                  | 41.4 ms: 1.10x slower                                                               |
| connected_components             | 201 ms                                                                   | 221 ms: 1.10x slower                                                                |
| logging_simple                   | 2.41 us                                                                  | 2.66 us: 1.10x slower                                                               |
| python_startup_no_site           | 6.26 ms                                                                  | 6.92 ms: 1.11x slower                                                               |
| sympy_sum                        | 56.2 ms                                                                  | 62.2 ms: 1.11x slower                                                               |
| scimark_fft                      | 130 ms                                                                   | 144 ms: 1.11x slower                                                                |
| mdp                              | 517 ms                                                                   | 573 ms: 1.11x slower                                                                |
| comprehensions                   | 7.78 us                                                                  | 8.65 us: 1.11x slower                                                               |
| richards                         | 22.1 ms                                                                  | 24.6 ms: 1.11x slower                                                               |
| sympy_str                        | 99.0 ms                                                                  | 110 ms: 1.11x slower                                                                |
| logging_format                   | 2.63 us                                                                  | 2.94 us: 1.12x slower                                                               |
| sqlalchemy_declarative           | 46.1 ms                                                                  | 51.6 ms: 1.12x slower                                                               |
| meteor_contest                   | 50.6 ms                                                                  | 56.7 ms: 1.12x slower                                                               |
| hexiom                           | 2.85 ms                                                                  | 3.19 ms: 1.12x slower                                                               |
| scimark_monte_carlo              | 29.5 ms                                                                  | 33.0 ms: 1.12x slower                                                               |
| mako                             | 4.97 ms                                                                  | 5.59 ms: 1.13x slower                                                               |
| crypto_pyaes                     | 37.6 ms                                                                  | 42.5 ms: 1.13x slower                                                               |
| deepcopy                         | 110 us                                                                   | 124 us: 1.13x slower                                                                |
| sympy_expand                     | 166 ms                                                                   | 189 ms: 1.14x slower                                                                |
| nbody                            | 49.3 ms                                                                  | 56.2 ms: 1.14x slower                                                               |
| typing_runtime_protocols         | 65.0 us                                                                  | 74.3 us: 1.14x slower                                                               |
| spectral_norm                    | 45.2 ms                                                                  | 51.7 ms: 1.14x slower                                                               |
| richards_super                   | 24.7 ms                                                                  | 28.3 ms: 1.14x slower                                                               |
| deepcopy_reduce                  | 1.11 us                                                                  | 1.28 us: 1.15x slower                                                               |
| genshi_text                      | 10.0 ms                                                                  | 11.5 ms: 1.15x slower                                                               |
| scimark_lu                       | 48.3 ms                                                                  | 55.5 ms: 1.15x slower                                                               |
| async_tree_eager                 | 43.0 ms                                                                  | 50.5 ms: 1.17x slower                                                               |
| coverage                         | 33.2 ms                                                                  | 40.8 ms: 1.23x slower                                                               |
| bench_thread_pool                | 441 us                                                                   | 600 us: 1.36x slower                                                                |
| Geometric mean                   | (ref)                                                                    | 1.01x slower                                                                        |

Benchmark hidden because not significant (2): pylint, async_tree_eager_memoization

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 98.87% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x