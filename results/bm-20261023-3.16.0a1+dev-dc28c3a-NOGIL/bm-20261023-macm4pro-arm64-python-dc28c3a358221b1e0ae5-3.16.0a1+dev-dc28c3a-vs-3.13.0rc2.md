# Results vs. 3.13.0rc2

- fork: python
- ref: dc28c3a358221b1e0ae5
- machine: darwin-arm64
- commit hash: dc28c3a
- commit date: 2026-10-23
- overall geometric mean: 1.004x faster
- HPT reliability: 73.21%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 438 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 287 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 295 ms: 1.31x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.04x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| float          | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                       |
| nbody          | 42.5 ms                                                        | 60.1 ms: 1.41x slower                                                       |
| Geometric mean | (ref)                                                          | 1.12x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.04 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 90.9 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.1 ms: 1.32x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.9 ms: 1.16x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 876 ms: 1.14x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 106 us: 1.07x slower                                                        |
| xml_etree_generate   | 35.8 ms                                                        | 38.4 ms: 1.07x slower                                                       |
| xml_etree_process    | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.79 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 764 us: 2.67x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 461 us: 2.16x faster                                                        |
| pylint                           | 106 ms                                                         | 51.9 ms: 2.03x faster                                                       |
| mdp                              | 1.06 sec                                                       | 571 ms: 1.85x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 287 ms: 1.82x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 290 ms: 1.81x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.72x faster                                                        |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.27 ms: 1.47x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 289 ms: 1.40x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 295 ms: 1.31x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| go                               | 72.6 ms                                                        | 59.7 ms: 1.22x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 783 ns: 1.21x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.04 ms: 1.18x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.0 us: 1.18x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.9 ms: 1.16x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 56.0 us: 1.15x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 876 ms: 1.14x faster                                                        |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.13x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 57.2 ms: 1.12x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                      |
| asyncio_websockets               | 194 ms                                                         | 182 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.04x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 178 ms: 1.04x faster                                                        |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 289 ms: 1.04x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 90.9 ms: 1.04x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 137 ms: 1.04x faster                                                        |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 179 ms: 1.03x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 124 ms: 1.02x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.12 ms: 1.02x slower                                                       |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                        |
| float                            | 31.4 ms                                                        | 32.5 ms: 1.04x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 137 ms: 1.04x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 106 us: 1.07x slower                                                        |
| sphinx                           | 409 ms                                                         | 438 ms: 1.07x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 38.4 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.09 ms: 1.09x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 713 ms: 1.10x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.69 us: 1.10x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.2 ms: 1.10x slower                                                       |
| thrift                           | 309 us                                                         | 342 us: 1.11x slower                                                        |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 48.7 ms: 1.11x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.7 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 467 us: 1.13x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 42.2 ms: 1.13x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.79 ms: 1.14x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.16x slower                                                        |
| connected_components             | 208 ms                                                         | 241 ms: 1.16x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.4 ms: 1.17x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.19x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.16 us: 1.20x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.76 ms: 1.21x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.0 ms: 1.22x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.7 ns: 1.22x slower                                                       |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                        |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 264 ms: 1.27x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.29x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.1 ms: 1.32x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 60.1 ms: 1.41x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.8 ms: 1.45x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 66.3 ms: 1.55x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.74x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                                |

Benchmark hidden because not significant (3): pycparser, fannkuch, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261023-3.16.0a1+dev-dc28c3a-NOGIL/bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1+dev-dc28c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 73.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x