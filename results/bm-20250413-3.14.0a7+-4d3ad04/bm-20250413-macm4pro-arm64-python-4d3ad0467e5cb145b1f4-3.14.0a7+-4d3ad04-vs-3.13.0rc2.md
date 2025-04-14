# Results vs. 3.13.0rc2

- fork: python
- ref: 4d3ad0467e5cb145b1f4
- machine: darwin-arm64
- commit hash: 4d3ad04
- commit date: 2025-04-13
- overall geometric mean: 1.031x faster
- HPT reliability: 86.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| nbody          | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 99.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|---------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads         | 1000 ms                                                        | 898 ms: 1.11x faster                                                     |
| xml_etree_iterparse | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                    |
| xml_etree_parse     | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                    |
| json_dumps          | 4.65 ms                                                        | 4.93 ms: 1.06x slower                                                    |
| json_loads          | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| pickle_pure_python  | 130 us                                                         | 144 us: 1.11x slower                                                     |
| Geometric mean      | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.01 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 247 ms: 2.13x faster                                                     |
| mdp                              | 1.06 sec                                                       | 516 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 249 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 940 ms: 1.56x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 250 ms: 1.54x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                    |
| go                               | 72.6 ms                                                        | 56.2 ms: 1.29x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.3 ms: 1.27x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 147 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 113 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.09 us: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.6 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 173 ms: 1.12x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 891 us: 1.11x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 898 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| float                            | 31.4 ms                                                        | 29.2 ms: 1.07x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.4 ms: 1.06x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.0 ms: 1.03x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 39.9 ns: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| genshi_text                      | 9.97 ms                                                        | 9.89 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 47.6 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.03 ms: 1.01x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 37.3 ms: 1.00x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 24.9 ms: 1.01x slower                                                    |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.9 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.3 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 328 ms: 1.02x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 664 ms: 1.02x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 98.2 ms: 1.03x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 45.4 ms: 1.04x slower                                                    |
| pycparser                        | 470 ms                                                         | 489 ms: 1.04x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.9 ms: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.01 ms: 1.04x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 99.6 ms: 1.05x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.93 ms: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 437 us: 1.06x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.3 ms: 1.07x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.35 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 113 ms: 1.07x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 40.7 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 117 ms: 1.08x slower                                                     |
| chaos                            | 24.3 ms                                                        | 26.2 ms: 1.08x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 46.4 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.40 us: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.85 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.7 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.00 ms: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.2 ms: 1.13x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.75 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.77 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.7 ms: 3.07x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (8): typing_runtime_protocols, genshi_xml, unpickle_pure_python, sphinx, xml_etree_process, sqlite_synth, xml_etree_generate, richards
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250413-3.14.0a7+-4d3ad04/bm-20250413-macm4pro-arm64-python-4d3ad0467e5cb145b1f4-3.14.0a7+-4d3ad04.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 86.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x