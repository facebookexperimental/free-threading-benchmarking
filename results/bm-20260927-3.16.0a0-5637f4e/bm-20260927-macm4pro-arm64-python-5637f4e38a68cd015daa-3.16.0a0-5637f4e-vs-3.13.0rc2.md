# Results vs. 3.13.0rc2

- fork: python
- ref: 5637f4e38a68cd015daa
- machine: darwin-arm64
- commit hash: 5637f4e
- commit date: 2026-09-27
- overall geometric mean: 1.046x faster
- HPT reliability: 99.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| docutils       | 1.05 sec                                                       | 956 ms: 1.10x faster                                                    |
| html5lib       | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| sphinx         | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 343 ms: 1.53x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.52 ms: 1.13x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 345 ms: 1.12x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 134 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.1 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody          | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.56 ms: 1.31x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 817 ms: 1.22x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.19 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.70 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| django_template | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.11x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 512 ms: 2.07x faster                                                    |
| pylint                           | 106 ms                                                         | 56.2 ms: 1.88x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 343 ms: 1.53x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 342 ms: 1.52x faster                                                    |
| deepcopy                         | 145 us                                                         | 95.8 us: 1.51x faster                                                   |
| k_core                           | 1.46 sec                                                       | 978 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.9 us: 1.39x faster                                                   |
| go                               | 72.6 ms                                                        | 52.6 ms: 1.38x faster                                                   |
| async_generators                 | 193 ms                                                         | 144 ms: 1.34x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 48.9 us: 1.32x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.56 ms: 1.31x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 49.4 ms: 1.30x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.25x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 329 ms: 1.23x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 817 ms: 1.22x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 836 us: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.29 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.52 ms: 1.13x faster                                                   |
| fannkuch                         | 179 ms                                                         | 159 ms: 1.12x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 345 ms: 1.12x faster                                                    |
| docutils                         | 1.05 sec                                                       | 956 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.95 sec: 1.09x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.3 ms: 1.09x faster                                                   |
| richards                         | 22.1 ms                                                        | 20.3 ms: 1.09x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.3 ms: 1.08x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 21.5 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 173 ms: 1.07x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.87 ms: 1.07x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 301 ms: 1.07x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.0 ms: 1.06x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 125 ms: 1.06x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.69 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.4 ms: 1.05x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 117 ms: 1.05x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 618 ms: 1.05x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 136 ms: 1.05x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 1.95 ms: 1.04x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 287 ms: 1.02x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 42.7 ms: 1.02x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 2.18 us: 1.02x faster                                                   |
| sphinx                           | 409 ms                                                         | 400 ms: 1.02x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 929 ns: 1.02x faster                                                    |
| connected_components             | 208 ms                                                         | 204 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.69 us: 1.02x faster                                                   |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.01x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.41 us: 1.01x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 167 ms: 1.00x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.0 ms: 1.01x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.47 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.02x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 419 us: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.9 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 64.0 ms: 1.03x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.7 ns: 1.03x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 98.9 ms: 1.04x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.58 ms: 1.04x slower                                                   |
| pycparser                        | 470 ms                                                         | 491 ms: 1.05x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.6 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.3 ms: 1.06x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.19 ms: 1.06x slower                                                   |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 134 ms: 1.10x slower                                                    |
| generators                       | 15.7 ms                                                        | 17.4 ms: 1.11x slower                                                   |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 251 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.70 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 38.2 ms: 1.14x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                   |
| django_template                  | 12.5 ms                                                        | 14.8 ms: 1.18x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 245 us: 1.22x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 266 ms: 1.28x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 154 ms: 1.50x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 65.1 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 104 ms: 3.58x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (4): async_tree_memoization, xml_etree_generate, scimark_sparse_mat_mult, thrift
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260927-3.16.0a0-5637f4e/bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 99.25% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.17x