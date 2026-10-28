# Results vs. 3.13.0rc2

- fork: python
- ref: 6c695bfad45ddde73d0d
- machine: darwin-arm64
- commit hash: 6c695bf
- commit date: 2026-10-27
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 111 ms: 1.01x faster                                                        |
| docutils       | 1.05 sec                                                       | 884 ms: 1.18x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.0 ms: 1.16x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 256 ms: 2.05x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.1 ms: 1.99x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 270 ms: 1.93x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 272 ms: 1.49x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.34x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 154 ms: 1.20x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 158 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 39.1 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.6 ms: 3.13x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                       |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                        |
| nbody          | 42.5 ms                                                        | 42.3 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.98 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.48 ms: 1.34x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 806 ms: 1.24x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.3 us: 1.08x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                       |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 493 ms: 2.15x faster                                                        |
| pylint                           | 106 ms                                                         | 50.1 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 256 ms: 2.05x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.1 ms: 1.99x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 270 ms: 1.93x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 609 us: 1.63x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.86 ms: 1.62x faster                                                       |
| deepcopy                         | 145 us                                                         | 93.6 us: 1.55x faster                                                       |
| k_core                           | 1.46 sec                                                       | 976 ms: 1.50x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 272 ms: 1.49x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 263 ms: 1.47x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 45.1 us: 1.43x faster                                                       |
| go                               | 72.6 ms                                                        | 50.7 ms: 1.43x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 106 ms: 1.34x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.48 ms: 1.34x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.4 ms: 1.32x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.01 us: 1.29x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.30 ms: 1.24x faster                                                       |
| pyflate                          | 222 ms                                                         | 179 ms: 1.24x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 806 ms: 1.24x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 109 ms: 1.22x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 154 ms: 1.20x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 8.98 ms: 1.19x faster                                                       |
| docutils                         | 1.05 sec                                                       | 884 ms: 1.18x faster                                                        |
| gc_traversal                     | 2.04 ms                                                        | 1.72 ms: 1.18x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 158 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 27.1 ms: 1.16x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.0 ms: 1.16x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 17.4 ms: 1.14x faster                                                       |
| fannkuch                         | 179 ms                                                         | 157 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 261 ms: 1.13x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.89 sec: 1.13x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.8 ms: 1.12x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| richards                         | 22.1 ms                                                        | 19.8 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.11x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 39.1 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.75 ms: 1.10x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.59 ms: 1.10x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.5 ms: 1.10x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.4 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.3 us: 1.08x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 40.7 ms: 1.08x faster                                                       |
| json                             | 1.94 ms                                                        | 1.81 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.30 us: 1.06x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.12 us: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 905 ns: 1.05x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.50 us: 1.05x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.21 ms: 1.04x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                        |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                        |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.9 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.74 ms: 1.02x faster                                                       |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 639 ms: 1.02x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 408 us: 1.01x faster                                                        |
| nbody                            | 42.5 ms                                                        | 42.3 ms: 1.01x faster                                                       |
| 2to3                             | 112 ms                                                         | 111 ms: 1.01x faster                                                        |
| chaos                            | 24.3 ms                                                        | 24.1 ms: 1.01x faster                                                       |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                        |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                        |
| mako                             | 4.41 ms                                                        | 4.46 ms: 1.01x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 41.2 ns: 1.01x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.5 ms: 1.02x slower                                                       |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 64.3 ms: 1.03x slower                                                       |
| pathlib                          | 11.1 ms                                                        | 11.5 ms: 1.04x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.3 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                        |
| generators                       | 15.7 ms                                                        | 16.7 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.37 ms: 1.07x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 45.9 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.1 ms: 1.07x slower                                                       |
| many_optionals                   | 200 us                                                         | 220 us: 1.10x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.1 ms: 1.11x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.35x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 90.6 ms: 3.13x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                                |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261027-3.16.0a1+dev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1+dev-6c695bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x