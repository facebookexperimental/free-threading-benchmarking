# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.005x slower
- HPT reliability: 89.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.02x faster                                                       |
| sphinx         | 409 ms                                                         | 446 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                          | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 296 ms: 1.76x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 300 ms: 1.75x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.75x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 299 ms: 1.35x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 300 ms: 1.29x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                                |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.2 ms: 1.39x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.8 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 869 ms: 1.15x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.0 ms: 1.14x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 158 us: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 785 us: 2.60x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 472 us: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 51.8 ms: 2.04x faster                                                       |
| mdp                              | 1.06 sec                                                       | 566 ms: 1.87x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 296 ms: 1.76x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 300 ms: 1.75x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.75x faster                                                        |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.29 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 299 ms: 1.35x faster                                                        |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 300 ms: 1.29x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.32 ms: 1.22x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.81 ms: 1.22x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.2 us: 1.22x faster                                                       |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.21x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.9 ms: 1.19x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.11 ms: 1.17x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 869 ms: 1.15x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.4 us: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.14x faster                                                      |
| pidigits                         | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| pyflate                          | 222 ms                                                         | 197 ms: 1.12x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.5 ms: 1.09x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 288 ms: 1.05x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 91.1 ms: 1.04x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.02x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                       |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                        |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                        |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 37.5 ms: 1.05x slower                                                       |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.14 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 349 ms: 1.08x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 41.1 ms: 1.09x slower                                                       |
| shortest_path                    | 225 ms                                                         | 244 ms: 1.09x slower                                                        |
| sphinx                           | 409 ms                                                         | 446 ms: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 52.6 ms: 1.10x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.70 us: 1.10x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                        |
| thrift                           | 309 us                                                         | 344 us: 1.11x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.0 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                       |
| 2to3                             | 112 ms                                                         | 125 ms: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 730 ms: 1.12x slower                                                        |
| spectral_norm                    | 43.7 ms                                                        | 49.5 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 468 us: 1.14x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.77 ms: 1.14x slower                                                       |
| connected_components             | 208 ms                                                         | 237 ms: 1.14x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.0 ms: 1.14x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.3 ms: 1.17x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.18x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.18x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 158 us: 1.21x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 49.3 ns: 1.21x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.17 ms: 1.22x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.23x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.6 ms: 1.24x slower                                                       |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                        |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.3 ms: 1.33x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 63.8 ms: 1.33x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.2 ms: 1.39x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.5 ms: 1.49x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 155 ms: 1.51x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 65.7 ms: 1.54x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, json
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-NOGIL/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 89.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x