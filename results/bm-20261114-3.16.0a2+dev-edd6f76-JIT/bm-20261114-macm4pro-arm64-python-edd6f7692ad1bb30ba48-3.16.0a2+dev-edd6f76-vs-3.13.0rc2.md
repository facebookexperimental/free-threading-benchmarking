# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.236x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 865 ms: 1.21x faster                                                        |
| html5lib       | 23.1 ms                                                        | 17.9 ms: 1.29x faster                                                       |
| sphinx         | 409 ms                                                         | 379 ms: 1.08x faster                                                        |
| Geometric mean | (ref)                                                          | 1.14x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 268 ms: 1.94x faster                                                        |
| async_generators                 | 193 ms                                                         | 105 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 36.7 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.3 ms: 3.08x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.17x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.2 ms: 1.42x faster                                                       |
| nbody          | 42.5 ms                                                        | 30.8 ms: 1.38x faster                                                       |
| pidigits       | 166 ms                                                         | 144 ms: 1.15x faster                                                        |
| Geometric mean | (ref)                                                          | 1.31x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.94 ms: 1.20x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 89.6 ms: 1.06x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 625 ms: 1.60x faster                                                        |
| json_dumps           | 4.65 ms                                                        | 3.32 ms: 1.40x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 72.5 us: 1.37x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 109 us: 1.19x faster                                                        |
| xml_etree_process    | 25.4 ms                                                        | 21.6 ms: 1.17x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 31.9 ms: 1.12x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                          | 1.21x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.00 ms: 1.08x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.67 ms: 1.20x faster                                                       |
| django_template | 12.5 ms                                                        | 12.2 ms: 1.02x faster                                                       |
| Geometric mean  | (ref)                                                          | 1.11x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| richards                         | 22.1 ms                                                        | 9.65 ms: 2.29x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 10.9 ms: 2.27x faster                                                       |
| mdp                              | 1.06 sec                                                       | 498 ms: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 49.7 ms: 2.12x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.09x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 31.7 ms: 2.02x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 268 ms: 1.94x faster                                                        |
| async_generators                 | 193 ms                                                         | 105 ms: 1.85x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.46 ms: 1.81x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 9.74 us: 1.69x faster                                                       |
| deepcopy                         | 145 us                                                         | 87.9 us: 1.65x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 40.3 us: 1.60x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 625 ms: 1.60x faster                                                        |
| k_core                           | 1.46 sec                                                       | 921 ms: 1.59x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 632 us: 1.57x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 261 ms: 1.55x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 255 ms: 1.52x faster                                                        |
| go                               | 72.6 ms                                                        | 47.9 ms: 1.52x faster                                                       |
| pyflate                          | 222 ms                                                         | 149 ms: 1.49x faster                                                        |
| float                            | 31.4 ms                                                        | 22.2 ms: 1.42x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.32 ms: 1.40x faster                                                       |
| scimark_lu                       | 42.8 ms                                                        | 30.8 ms: 1.39x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 31.5 ms: 1.39x faster                                                       |
| nbody                            | 42.5 ms                                                        | 30.8 ms: 1.38x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 72.5 us: 1.37x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 946 ns: 1.37x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 91.6 ms: 1.35x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.9 ms: 1.31x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 249 ms: 1.29x faster                                                        |
| html5lib                         | 23.1 ms                                                        | 17.9 ms: 1.29x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 1.74 us: 1.29x faster                                                       |
| logging_format                   | 2.45 us                                                        | 1.90 us: 1.29x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 5.35 us: 1.27x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.15 ms: 1.26x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 515 ms: 1.26x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 30.1 ms: 1.24x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 151 ms: 1.23x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.75 sec: 1.22x faster                                                      |
| fannkuch                         | 179 ms                                                         | 147 ms: 1.21x faster                                                        |
| docutils                         | 1.05 sec                                                       | 865 ms: 1.21x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.20x faster                                                        |
| logging_silent                   | 40.6 ns                                                        | 33.8 ns: 1.20x faster                                                       |
| mako                             | 4.41 ms                                                        | 3.67 ms: 1.20x faster                                                       |
| chaos                            | 24.3 ms                                                        | 20.2 ms: 1.20x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 8.94 ms: 1.20x faster                                                       |
| pickle_pure_python               | 130 us                                                         | 109 us: 1.19x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 16.7 ms: 1.19x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.58 ms: 1.19x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.40 ms: 1.19x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 36.7 ms: 1.18x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 21.6 ms: 1.17x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.77 ms: 1.15x faster                                                       |
| pidigits                         | 166 ms                                                         | 144 ms: 1.15x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.1 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 258 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 31.9 ms: 1.12x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 30.4 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.63 ms: 1.09x faster                                                       |
| raytrace                         | 109 ms                                                         | 99.8 ms: 1.09x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                       |
| sphinx                           | 409 ms                                                         | 379 ms: 1.08x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 8.00 ms: 1.08x faster                                                       |
| json                             | 1.94 ms                                                        | 1.80 ms: 1.08x faster                                                       |
| many_optionals                   | 200 us                                                         | 186 us: 1.07x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.4 ms: 1.07x faster                                                       |
| meteor_contest                   | 47.9 ms                                                        | 44.7 ms: 1.07x faster                                                       |
| thrift                           | 309 us                                                         | 290 us: 1.07x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 89.6 ms: 1.06x faster                                                       |
| regex_compile                    | 47.9 ms                                                        | 45.6 ms: 1.05x faster                                                       |
| pycparser                        | 470 ms                                                         | 449 ms: 1.05x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 913 ns: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.28 ms: 1.03x faster                                                       |
| shortest_path                    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| django_template                  | 12.5 ms                                                        | 12.2 ms: 1.02x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                        |
| bench_thread_pool                | 412 us                                                         | 406 us: 1.01x faster                                                        |
| sympy_sum                        | 52.3 ms                                                        | 51.9 ms: 1.01x faster                                                       |
| sympy_str                        | 95.5 ms                                                        | 94.8 ms: 1.01x faster                                                       |
| sympy_expand                     | 159 ms                                                         | 159 ms: 1.00x faster                                                        |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 64.2 ms: 1.03x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 42.0 ms: 1.11x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.5 ms: 1.12x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 139 ms: 1.36x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.3 ms: 3.08x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76-JIT/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.236x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.14x