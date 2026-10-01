# Results vs. 3.13.0rc2

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: darwin-arm64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.046x faster
- HPT reliability: 97.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| docutils       | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| sphinx         | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 345 ms: 1.52x faster                                                    |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 330 ms: 1.23x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.42 ms: 1.14x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 344 ms: 1.12x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 138 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.9 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.62x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| nbody          | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                   |
| pidigits       | 166 ms                                                         | 172 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 794 ms: 1.26x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 139 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.06x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.53 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 512 ms: 2.07x faster                                                    |
| pylint                           | 106 ms                                                         | 56.4 ms: 1.87x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 345 ms: 1.52x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.12 ms: 1.52x faster                                                   |
| deepcopy                         | 145 us                                                         | 96.8 us: 1.50x faster                                                   |
| k_core                           | 1.46 sec                                                       | 997 ms: 1.47x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                   |
| go                               | 72.6 ms                                                        | 52.3 ms: 1.39x faster                                                   |
| async_generators                 | 193 ms                                                         | 143 ms: 1.35x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.9 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.58 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.5 ms: 1.29x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 794 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 330 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 181 ms: 1.23x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.26 ms: 1.16x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 864 us: 1.15x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.42 ms: 1.14x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 344 ms: 1.12x faster                                                    |
| fannkuch                         | 179 ms                                                         | 159 ms: 1.12x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.4 ms: 1.11x faster                                                   |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                   |
| docutils                         | 1.05 sec                                                       | 954 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 115 ms: 1.08x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.9 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.65 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.86 ms: 1.07x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 34.8 ms: 1.07x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 174 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 302 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 621 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 138 ms: 1.03x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.4 ms: 1.03x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 96.6 us: 1.03x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.65 us: 1.02x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 288 ms: 1.02x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.19 us: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 401 ms: 1.02x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.40 us: 1.02x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.00 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 296 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 93.1 ms: 1.02x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 932 ns: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.43 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 308 us: 1.00x faster                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                    |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.79 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.46 ms: 1.01x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 417 us: 1.01x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                   |
| nbody                            | 42.5 ms                                                        | 43.7 ms: 1.03x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.55 ms: 1.03x slower                                                   |
| pidigits                         | 166 ms                                                         | 172 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.2 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.4 ms: 1.05x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 65.5 ms: 1.05x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.06x slower                                                   |
| raytrace                         | 109 ms                                                         | 116 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 139 us: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.08x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.2 ms: 1.10x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.53 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.3 ms: 1.11x slower                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 135 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 250 ms: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.91 ms: 1.16x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.0 ms: 1.17x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.19x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.0 ms: 1.22x slower                                                   |
| many_optionals                   | 200 us                                                         | 246 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 268 ms: 1.29x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.9 ms: 1.53x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 105 ms: 3.62x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (2): json_loads, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 97.94% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x