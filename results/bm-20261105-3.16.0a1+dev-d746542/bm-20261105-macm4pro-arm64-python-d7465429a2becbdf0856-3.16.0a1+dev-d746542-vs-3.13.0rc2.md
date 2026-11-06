# Results vs. 3.13.0rc2

- fork: python
- ref: d7465429a2becbdf0856
- machine: darwin-arm64
- commit hash: d746542
- commit date: 2026-11-05
- overall geometric mean: 1.114x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                        |
| docutils       | 1.05 sec                                                       | 894 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 409 ms                                                         | 386 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.3 ms: 1.99x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.90x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.4 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 798 ms: 1.25x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 93.2 us: 1.07x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.23 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 500 ms: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 51.3 ms: 2.06x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 260 ms: 2.02x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.3 ms: 1.99x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.90x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.87 ms: 1.62x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 616 us: 1.61x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.4 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 971 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.48x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 268 ms: 1.44x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                       |
| go                               | 72.6 ms                                                        | 51.4 ms: 1.41x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 46.0 us: 1.40x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.54 ms: 1.31x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.31x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 798 ms: 1.25x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.19x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.74 ms: 1.17x faster                                                       |
| docutils                         | 1.05 sec                                                       | 894 ms: 1.17x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.85 sec: 1.15x faster                                                      |
| regex_v8                         | 10.7 ms                                                        | 9.36 ms: 1.14x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.3 ms: 1.14x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                        |
| pidigits                         | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| richards                         | 22.1 ms                                                        | 19.9 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.10x faster                                                        |
| hexiom                           | 2.85 ms                                                        | 2.59 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.09x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.1 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 93.2 us: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 386 ms: 1.06x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.4 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.23 ms: 1.05x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 307 ms: 1.05x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 215 ms: 1.04x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.54 us: 1.04x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.04x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 915 ns: 1.04x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.7 ms: 1.03x faster                                                       |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.8 ms: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                        |
| pprint_pformat                   | 650 ms                                                         | 632 ms: 1.03x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.42 ms: 1.02x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 61.8 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.77 ms: 1.01x faster                                                       |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                        |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.4 ms: 1.01x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 48.4 ms: 1.01x slower                                                       |
| nbody                            | 42.5 ms                                                        | 43.4 ms: 1.02x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.8 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.03x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 54.6 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.06x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.36 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.0 ms: 1.07x slower                                                       |
| generators                       | 15.7 ms                                                        | 16.8 ms: 1.07x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.1 ms: 1.09x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.8 ms: 1.09x slower                                                       |
| many_optionals                   | 200 us                                                         | 223 us: 1.11x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.4 ms: 1.15x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (4): mako, pycparser, bench_thread_pool, shortest_path
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261105-3.16.0a1+dev-d746542/bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.114x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x