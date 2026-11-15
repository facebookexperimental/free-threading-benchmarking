# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| docutils       | 1.05 sec                                                       | 900 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.4 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.6 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.65 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 144 ms: 1.15x faster                                                        |
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                       |
| nbody          | 42.5 ms                                                        | 43.5 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.28 ms: 1.26x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 785 ms: 1.27x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.7 ms: 1.10x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 94.5 us: 1.05x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 138 us: 1.06x slower                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 7.97 ms: 1.08x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.38 ms: 1.01x faster                                                       |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 499 ms: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 50.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 264 ms: 1.99x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.6 ms: 1.98x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.91 ms: 1.60x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 625 us: 1.59x faster                                                        |
| k_core                           | 1.46 sec                                                       | 967 ms: 1.51x faster                                                        |
| deepcopy                         | 145 us                                                         | 96.3 us: 1.51x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.0 us: 1.44x faster                                                       |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                        |
| go                               | 72.6 ms                                                        | 51.5 ms: 1.41x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.53 ms: 1.32x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.9 ms: 1.31x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 111 ms: 1.28x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 785 ms: 1.27x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.28 ms: 1.26x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                       |
| pyflate                          | 222 ms                                                         | 182 ms: 1.22x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                       |
| docutils                         | 1.05 sec                                                       | 900 ms: 1.16x faster                                                        |
| pidigits                         | 166 ms                                                         | 144 ms: 1.15x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 162 ms: 1.14x faster                                                        |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.4 ms: 1.13x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.4 ms: 1.13x faster                                                       |
| fannkuch                         | 179 ms                                                         | 158 ms: 1.13x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.7 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 270 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.65 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 265 ms: 1.11x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.7 ms: 1.10x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                       |
| scimark_fft                      | 124 ms                                                         | 112 ms: 1.10x faster                                                        |
| telco                            | 3.07 ms                                                        | 2.79 ms: 1.10x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.61 ms: 1.09x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.7 ms: 1.09x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.3 ms: 1.09x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 7.97 ms: 1.08x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.0 ms: 1.07x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.93 ms: 1.06x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 89.8 ms: 1.05x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 94.5 us: 1.05x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 306 ms: 1.05x faster                                                        |
| json                             | 1.94 ms                                                        | 1.85 ms: 1.05x faster                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.57 us: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 628 ms: 1.03x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.41 ms: 1.03x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 922 ns: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.73 ms: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.8 ms: 1.02x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                       |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                        |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 407 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 222 ms: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                       |
| mako                             | 4.41 ms                                                        | 4.38 ms: 1.01x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 48.1 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.6 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.02x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 97.7 ms: 1.02x slower                                                       |
| nbody                            | 42.5 ms                                                        | 43.5 ms: 1.02x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.3 ms: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 138 us: 1.06x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                       |
| generators                       | 15.7 ms                                                        | 16.9 ms: 1.08x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.3 ms: 1.08x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.5 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.2 ms: 1.11x slower                                                       |
| many_optionals                   | 200 us                                                         | 227 us: 1.13x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x