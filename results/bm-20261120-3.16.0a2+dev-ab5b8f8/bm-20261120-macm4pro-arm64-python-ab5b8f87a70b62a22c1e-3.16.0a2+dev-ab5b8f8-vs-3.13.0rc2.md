# Results vs. 3.13.0rc2

- fork: python
- ref: ab5b8f87a70b62a22c1e
- machine: darwin-arm64
- commit hash: ab5b8f8
- commit date: 2026-11-20
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 114 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 896 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 381 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 193 ms                                                         | 98.5 ms: 1.96x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 280 ms: 1.86x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 279 ms: 1.45x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.5 ms: 3.23x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 146 ms: 1.14x faster                                                        |
| nbody          | 42.5 ms                                                        | 41.2 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 820 ms: 1.22x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 94.5 us: 1.05x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.2 ms: 1.05x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.04 ms: 1.07x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pylint                           | 106 ms                                                         | 50.3 ms: 2.10x faster                                                       |
| mdp                              | 1.06 sec                                                       | 504 ms: 2.10x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.5 ms: 1.96x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 280 ms: 1.86x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.93 ms: 1.59x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 628 us: 1.58x faster                                                        |
| deepcopy                         | 145 us                                                         | 94.9 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 974 ms: 1.50x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 279 ms: 1.45x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.2 us: 1.43x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 271 ms: 1.42x faster                                                        |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.39x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 47.7 ms: 1.34x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.25x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 820 ms: 1.22x faster                                                        |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.08 ms: 1.18x faster                                                       |
| docutils                         | 1.05 sec                                                       | 896 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.2 ms: 1.14x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.86 sec: 1.14x faster                                                      |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| pidigits                         | 166 ms                                                         | 146 ms: 1.14x faster                                                        |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.81 ms: 1.13x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 110 ms: 1.12x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.59 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.63 ms: 1.08x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.04 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 381 ms: 1.07x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 94.5 us: 1.05x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.2 ms: 1.05x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.15 us: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.87 ms: 1.04x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                       |
| scimark_lu                       | 42.8 ms                                                        | 41.3 ms: 1.04x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 918 ns: 1.03x faster                                                        |
| nbody                            | 42.5 ms                                                        | 41.2 ms: 1.03x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 315 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| mako                             | 4.41 ms                                                        | 4.33 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.02x faster                                                       |
| pycparser                        | 470 ms                                                         | 463 ms: 1.01x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 40.1 ns: 1.01x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 642 ms: 1.01x faster                                                        |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.78 us: 1.00x faster                                                       |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                       |
| 2to3                             | 112 ms                                                         | 114 ms: 1.02x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.2 ms: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.4 ms: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 36.4 ms: 1.08x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                       |
| many_optionals                   | 200 us                                                         | 229 us: 1.14x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 142 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.5 ms: 3.23x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261120-3.16.0a2+dev-ab5b8f8/bm-20261120-macm4pro-arm64-python-ab5b8f87a70b62a22c1e-3.16.0a2+dev-ab5b8f8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x