# Results vs. 3.12.6

- fork: nascheme
- ref: gh_158197_split_dict
- machine: darwin-arm64
- commit hash: 703df80
- commit date: 2026-10-16
- overall geometric mean: 1.133x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                          |
| docutils       | 1.02 sec                                                 | 991 ms: 1.03x faster                                                          |
| html5lib       | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                         |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                    | 1.02x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.81x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                          |
| async_tree_none                  | 178 ms                                                   | 130 ms: 1.37x faster                                                          |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.35x faster                                                          |
| async_tree_none_tg               | 172 ms                                                   | 130 ms: 1.33x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 281 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                          |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                          |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                          |
| async_tree_eager                 | 45.6 ms                                                  | 44.6 ms: 1.02x faster                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                          |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.43x slower                                                          |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                         |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                          |
| nbody          | 54.2 ms                                                  | 53.9 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                         |
| regex_dna      | 99.6 ms                                                  | 87.4 ms: 1.14x faster                                                         |
| regex_v8       | 9.59 ms                                                  | 8.63 ms: 1.11x faster                                                         |
| regex_compile  | 54.6 ms                                                  | 58.3 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                         |
| json_dumps           | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                         |
| xml_etree_parse      | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                         |
| tomli_loads          | 957 ms                                                   | 845 ms: 1.13x faster                                                          |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                         |
| unpickle_pure_python | 103 us                                                   | 98.1 us: 1.05x faster                                                         |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                         |
| pickle_pure_python   | 139 us                                                   | 142 us: 1.02x slower                                                          |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.76 ms: 1.22x slower                                                         |
| python_startup_no_site | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                         |
| Geometric mean         | (ref)                                                    | 1.24x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                         |
| mako            | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                         |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                                  |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.93 ms: 5.28x faster                                                         |
| gc_traversal                     | 2.01 ms                                                  | 756 us: 2.66x faster                                                          |
| pylint                           | 128 ms                                                   | 50.3 ms: 2.55x faster                                                         |
| mdp                              | 1.09 sec                                                 | 544 ms: 2.01x faster                                                          |
| async_tree_eager_io              | 496 ms                                                   | 273 ms: 1.81x faster                                                          |
| create_gc_cycles                 | 830 us                                                   | 461 us: 1.80x faster                                                          |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                          |
| async_tree_io                    | 459 ms                                                   | 270 ms: 1.70x faster                                                          |
| async_tree_eager_io_tg           | 446 ms                                                   | 273 ms: 1.63x faster                                                          |
| deepcopy                         | 161 us                                                   | 99.3 us: 1.63x faster                                                         |
| generators                       | 21.9 ms                                                  | 15.3 ms: 1.43x faster                                                         |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.40x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 130 ms: 1.37x faster                                                          |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 171 ms: 1.35x faster                                                          |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.34x faster                                                         |
| typing_runtime_protocols         | 71.0 us                                                  | 53.2 us: 1.33x faster                                                         |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                         |
| async_tree_none_tg               | 172 ms                                                   | 130 ms: 1.33x faster                                                          |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                         |
| go                               | 70.0 ms                                                  | 54.8 ms: 1.28x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 175 ms: 1.27x faster                                                          |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.26x faster                                                         |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                         |
| spectral_norm                    | 54.4 ms                                                  | 44.2 ms: 1.23x faster                                                         |
| sqlite_synth                     | 967 ns                                                   | 787 ns: 1.23x faster                                                          |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 281 ms: 1.21x faster                                                          |
| pathlib                          | 12.4 ms                                                  | 10.3 ms: 1.20x faster                                                         |
| raytrace                         | 145 ms                                                   | 121 ms: 1.20x faster                                                          |
| logging_silent                   | 50.9 ns                                                  | 42.3 ns: 1.20x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.58 ms: 1.19x faster                                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                         |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                         |
| scimark_sor                      | 61.0 ms                                                  | 52.5 ms: 1.16x faster                                                         |
| k_core                           | 1.12 sec                                                 | 962 ms: 1.16x faster                                                          |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 287 ms: 1.16x faster                                                          |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                          |
| nqueens                          | 43.5 ms                                                  | 37.6 ms: 1.16x faster                                                         |
| async_generators                 | 206 ms                                                   | 180 ms: 1.14x faster                                                          |
| regex_dna                        | 99.6 ms                                                  | 87.4 ms: 1.14x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 845 ms: 1.13x faster                                                          |
| logging_format                   | 2.80 us                                                  | 2.49 us: 1.13x faster                                                         |
| logging_simple                   | 2.57 us                                                  | 2.28 us: 1.13x faster                                                         |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                          |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                          |
| regex_v8                         | 9.59 ms                                                  | 8.63 ms: 1.11x faster                                                         |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                          |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                         |
| deltablue                        | 1.73 ms                                                  | 1.57 ms: 1.10x faster                                                         |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.08x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                         |
| html5lib                         | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 7.62 ms: 1.05x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 181 ms: 1.05x faster                                                          |
| unpickle_pure_python             | 103 us                                                   | 98.1 us: 1.05x faster                                                         |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                         |
| docutils                         | 1.02 sec                                                 | 991 ms: 1.03x faster                                                          |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                          |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                         |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                          |
| async_tree_eager                 | 45.6 ms                                                  | 44.6 ms: 1.02x faster                                                         |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.8 ms: 1.01x faster                                                         |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                          |
| nbody                            | 54.2 ms                                                  | 53.9 ms: 1.01x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                          |
| sympy_sum                        | 57.6 ms                                                  | 57.3 ms: 1.00x faster                                                         |
| richards                         | 22.4 ms                                                  | 22.3 ms: 1.00x faster                                                         |
| richards_super                   | 25.4 ms                                                  | 25.6 ms: 1.01x slower                                                         |
| thrift                           | 322 us                                                   | 326 us: 1.01x slower                                                          |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.11 ms: 1.02x slower                                                         |
| pickle_pure_python               | 139 us                                                   | 142 us: 1.02x slower                                                          |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.02x slower                                                          |
| crypto_pyaes                     | 38.8 ms                                                  | 40.0 ms: 1.03x slower                                                         |
| scimark_lu                       | 51.3 ms                                                  | 52.9 ms: 1.03x slower                                                         |
| pprint_pformat                   | 665 ms                                                   | 686 ms: 1.03x slower                                                          |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                         |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                          |
| sympy_expand                     | 167 ms                                                   | 176 ms: 1.06x slower                                                          |
| regex_compile                    | 54.6 ms                                                  | 58.3 ms: 1.07x slower                                                         |
| meteor_contest                   | 47.7 ms                                                  | 53.0 ms: 1.11x slower                                                         |
| shortest_path                    | 219 ms                                                   | 246 ms: 1.13x slower                                                          |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                         |
| mako                             | 4.77 ms                                                  | 5.57 ms: 1.17x slower                                                         |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                         |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                          |
| connected_components             | 201 ms                                                   | 242 ms: 1.21x slower                                                          |
| python_startup                   | 8.01 ms                                                  | 9.76 ms: 1.22x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                          |
| python_startup_no_site           | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                         |
| bench_thread_pool                | 419 us                                                   | 573 us: 1.37x slower                                                          |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 155 ms: 1.38x slower                                                          |
| coverage                         | 26.9 ms                                                  | 38.1 ms: 1.42x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 110 ms: 3.43x slower                                                          |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                                  |

Benchmark hidden because not significant (2): sympy_str, xml_etree_process
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261016-3.16.0a1+dev-703df80-CLANG,NOGIL/bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1+dev-703df80.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.133x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.29x