# Results vs. 3.13.0rc2

- fork: python
- ref: dc28c3a358221b1e0ae5
- machine: darwin-arm64
- commit hash: dc28c3a
- commit date: 2026-10-23
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 903 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                       |
| sphinx         | 409 ms                                                         | 387 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 100 ms: 1.93x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 273 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                       |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                        |
| nbody          | 42.5 ms                                                        | 41.5 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.02 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.50 ms: 1.33x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 799 ms: 1.25x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.9 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.39 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                       |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 498 ms: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 51.4 ms: 2.05x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 100 ms: 1.93x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 273 ms: 1.91x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 609 us: 1.63x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.91 ms: 1.60x faster                                                       |
| deepcopy                         | 145 us                                                         | 94.7 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 967 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.42x faster                                                       |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.40x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.50 ms: 1.33x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 49.5 us: 1.31x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 799 ms: 1.25x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| pyflate                          | 222 ms                                                         | 180 ms: 1.23x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 110 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.02 ms: 1.19x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.73 ms: 1.18x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 159 ms: 1.16x faster                                                        |
| docutils                         | 1.05 sec                                                       | 903 ms: 1.16x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 20.1 ms: 1.15x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.12x faster                                                      |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.12x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.12x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.1 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.4 ms: 1.08x faster                                                       |
| json                             | 1.94 ms                                                        | 1.80 ms: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.2 ms: 1.07x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.9 us: 1.07x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.8 ms: 1.07x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 88.8 ms: 1.07x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                       |
| sphinx                           | 409 ms                                                         | 387 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.4 ms: 1.06x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                       |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 310 ms: 1.04x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.57 us: 1.04x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.29 ms: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 630 ms: 1.03x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 919 ns: 1.03x faster                                                        |
| nbody                            | 42.5 ms                                                        | 41.5 ms: 1.03x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 35.2 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 304 us: 1.02x faster                                                        |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.76 ms: 1.01x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.44 ms: 1.01x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 25.2 ms: 1.01x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 47.7 ms: 1.00x faster                                                       |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.5 ms: 1.01x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 63.1 ms: 1.01x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.0 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.5 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 43.1 ns: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.39 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.2 ms: 1.08x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.7 ms: 1.09x slower                                                       |
| many_optionals                   | 200 us                                                         | 221 us: 1.10x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.4 ms: 1.12x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| generators                       | 15.7 ms                                                        | 18.2 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 91.8 ms: 3.17x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (3): 2to3, connected_components, bench_thread_pool
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-dc28c3a/bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x