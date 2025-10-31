# Results vs. 3.13.0rc2

- fork: python
- ref: ac1ffd77858b62d169a0
- machine: darwin-arm64
- commit hash: ac1ffd7
- commit date: 2025-10-30
- overall geometric mean: 1.008x faster
- HPT reliability: 68.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 992 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 969 ms: 1.03x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                    |
| mako            | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                    |
| django_template | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 754 us: 2.71x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 193 ms: 2.70x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 202 ms: 2.60x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 470 us: 2.11x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                     |
| mdp                              | 1.06 sec                                                       | 598 ms: 1.77x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 86.4 ms: 1.54x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 990 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 99.7 ms: 1.43x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 130 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 234 ms: 1.29x faster                                                     |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 241 ms: 1.22x faster                                                     |
| go                               | 72.6 ms                                                        | 61.5 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.5 ms: 1.15x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 829 ns: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 109 ms: 1.12x faster                                                     |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.7 ms: 1.06x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.01 sec: 1.06x faster                                                   |
| float                            | 31.4 ms                                                        | 29.7 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 992 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 969 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                    |
| pycparser                        | 470 ms                                                         | 476 ms: 1.01x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 185 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                     |
| pylint                           | 106 ms                                                         | 111 ms: 1.06x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.00 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 224 ms: 1.08x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 225 ms: 1.08x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.9 ms: 1.08x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 111 ms: 1.08x slower                                                     |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                    |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.63 ms: 1.12x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 360 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 42.5 ms: 1.12x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.8 ns: 1.13x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 735 ms: 1.13x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 48.9 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.13x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.14x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.2 us: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.82 us: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.7 ms: 1.15x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.3 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.3 ms: 1.19x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 191 ms: 1.20x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.2 ms: 1.20x slower                                                    |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.2 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.37 us: 1.23x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 54.1 ms: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.0 ms: 1.28x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.2 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 536 us: 1.30x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.75 ms: 1.30x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.6 ms: 1.33x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 378 us: 1.89x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.1 ms: 2.67x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.9 ms: 3.02x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251030-3.15.0a1+-ac1ffd7-NOGIL/bm-20251030-macm4pro-arm64-python-ac1ffd77858b62d169a0-3.15.0a1+-ac1ffd7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 68.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x