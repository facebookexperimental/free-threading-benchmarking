# Results vs. 3.13.0rc2

- fork: python
- ref: a6b4aa687cd9f8f95e3b
- machine: darwin-arm64
- commit hash: a6b4aa6
- commit date: 2026-10-14
- overall geometric mean: 1.095x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 904 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 1.99x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 281 ms: 1.44x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.82 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| nbody          | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                       |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 815 ms: 1.23x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 93.8 us: 1.06x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.48 ms: 1.02x slower                                                       |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 503 ms: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 52.4 ms: 2.01x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 263 ms: 1.99x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.96 ms: 1.58x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 646 us: 1.54x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.4 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 970 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 281 ms: 1.44x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.6 us: 1.41x faster                                                       |
| go                               | 72.6 ms                                                        | 52.7 ms: 1.38x faster                                                       |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 49.0 us: 1.32x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 49.0 ms: 1.31x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 815 ms: 1.23x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.07 us: 1.21x faster                                                       |
| pyflate                          | 222 ms                                                         | 186 ms: 1.20x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.18x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                        |
| docutils                         | 1.05 sec                                                       | 904 ms: 1.16x faster                                                        |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.40 ms: 1.14x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.80 ms: 1.13x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 272 ms: 1.11x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.10x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.10x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.82 ms: 1.09x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.3 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.08x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.66 ms: 1.07x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.8 ms: 1.07x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.1 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 93.8 us: 1.06x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| nbody                            | 42.5 ms                                                        | 40.5 ms: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 309 ms: 1.04x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.73 ms: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 631 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.61 us: 1.03x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.38 us: 1.03x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.02x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 926 ns: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.37 ms: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 25.0 ms: 1.01x faster                                                       |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                        |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| mako                             | 4.41 ms                                                        | 4.48 ms: 1.02x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.8 ms: 1.02x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 63.9 ms: 1.02x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.87 ms: 1.03x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 55.0 ms: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.47 ms: 1.09x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.8 ms: 1.09x slower                                                       |
| many_optionals                   | 200 us                                                         | 226 us: 1.13x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.09x faster                                                                |

Benchmark hidden because not significant (4): deltablue, bench_thread_pool, pycparser, connected_components
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261014-3.16.0a1+dev-a6b4aa6/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x