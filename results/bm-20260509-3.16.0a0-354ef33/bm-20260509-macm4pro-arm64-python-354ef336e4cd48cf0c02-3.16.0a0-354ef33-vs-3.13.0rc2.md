# Results vs. 3.13.0rc2

- fork: python
- ref: 354ef336e4cd48cf0c02
- machine: darwin-arm64
- commit hash: 354ef33
- commit date: 2026-05-09
- overall geometric mean: 1.034x faster
- HPT reliability: 97.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 968 ms: 1.08x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 331 ms: 1.57x faster                                                    |
| async_generators                 | 193 ms                                                         | 147 ms: 1.31x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 310 ms: 1.24x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 258 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| nbody          | 42.5 ms                                                        | 45.3 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 833 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 104 us: 1.05x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 68.3 ms: 1.10x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                    |
| pylint                           | 106 ms                                                         | 55.7 ms: 1.90x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 305 ms: 1.72x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 331 ms: 1.57x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.13 ms: 1.52x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                  |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| go                               | 72.6 ms                                                        | 54.3 ms: 1.34x faster                                                   |
| async_generators                 | 193 ms                                                         | 147 ms: 1.31x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.2 ms: 1.27x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 310 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.75 ms: 1.24x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 833 ms: 1.20x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 120 ms: 1.19x faster                                                    |
| pyflate                          | 222 ms                                                         | 188 ms: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.12 us: 1.16x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 864 us: 1.15x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.12x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.75 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 968 ms: 1.08x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.8 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 277 ms: 1.06x faster                                                    |
| fannkuch                         | 179 ms                                                         | 169 ms: 1.06x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 126 ms: 1.06x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.91 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 118 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                    |
| richards                         | 22.1 ms                                                        | 21.3 ms: 1.04x faster                                                   |
| float                            | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.1 ms: 1.02x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.6 ms: 1.02x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 46.8 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 935 ns: 1.01x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.9 ms: 1.00x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 323 ms: 1.00x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 654 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.48 us: 1.02x slower                                                   |
| thrift                           | 309 us                                                         | 316 us: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.5 us: 1.03x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.30 us: 1.03x slower                                                   |
| pycparser                        | 470 ms                                                         | 484 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.1 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.1 ns: 1.04x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 104 us: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 433 us: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.3 ms: 1.07x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.28 us: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 171 ms: 1.08x slower                                                    |
| raytrace                         | 109 ms                                                         | 118 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.93 ms: 1.09x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.81 ms: 1.09x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 68.3 ms: 1.10x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 51.0 ms: 1.19x slower                                                   |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 40.4 ms: 1.20x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 258 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.9 ms: 1.24x slower                                                   |
| generators                       | 15.7 ms                                                        | 20.0 ms: 1.27x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 151 ms: 1.47x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 59.5 ms: 1.60x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 102 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                            |

Benchmark hidden because not significant (3): dask, sphinx, sympy_integrate
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260509-3.16.0a0-354ef33/bm-20260509-macm4pro-arm64-python-354ef336e4cd48cf0c02-3.16.0a0-354ef33.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.034x faster

# HPT report

- Reliability score: 97.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x