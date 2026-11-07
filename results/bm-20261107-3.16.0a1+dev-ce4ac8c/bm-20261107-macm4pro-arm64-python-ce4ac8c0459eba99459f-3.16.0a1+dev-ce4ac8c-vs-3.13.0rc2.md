# Results vs. 3.13.0rc2

- fork: python
- ref: ce4ac8c0459eba99459f
- machine: darwin-arm64
- commit hash: ce4ac8c
- commit date: 2026-11-07
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 892 ms: 1.17x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 409 ms                                                         | 384 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                          | 1.09x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.9 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.43x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.19x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.21x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                       |
| pidigits       | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| nbody          | 42.5 ms                                                        | 41.3 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                          | 1.11x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.03 ms: 1.18x faster                                                       |
| regex_effbot   | 1.61 ms                                                        | 1.38 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 814 ms: 1.23x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 91.8 us: 1.08x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 7.96 ms: 1.08x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 4.34 ms: 1.02x faster                                                       |
| django_template | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.07x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 500 ms: 2.12x faster                                                        |
| pylint                           | 106 ms                                                         | 50.0 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 97.9 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 277 ms: 1.88x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.91 ms: 1.60x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 623 us: 1.60x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.1 us: 1.53x faster                                                       |
| k_core                           | 1.46 sec                                                       | 972 ms: 1.51x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 278 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.43x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 11.5 us: 1.43x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 45.5 us: 1.42x faster                                                       |
| go                               | 72.6 ms                                                        | 51.1 ms: 1.42x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 48.8 ms: 1.31x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.55 ms: 1.31x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 109 ms: 1.30x faster                                                        |
| deepcopy_reduce                  | 1.30 us                                                        | 1.02 us: 1.27x faster                                                       |
| pyflate                          | 222 ms                                                         | 179 ms: 1.24x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 814 ms: 1.23x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.20x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.19x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.03 ms: 1.18x faster                                                       |
| docutils                         | 1.05 sec                                                       | 892 ms: 1.17x faster                                                        |
| float                            | 31.4 ms                                                        | 26.8 ms: 1.17x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.38 ms: 1.17x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.75 ms: 1.17x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 25.9 ms: 1.15x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 20.3 ms: 1.14x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                       |
| pidigits                         | 166 ms                                                         | 148 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                        |
| fannkuch                         | 179 ms                                                         | 159 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.11x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.68 ms: 1.11x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| python_startup                   | 8.63 ms                                                        | 7.96 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 91.8 us: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 22.8 ms: 1.08x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.84 ms: 1.08x faster                                                       |
| nqueens                          | 37.2 ms                                                        | 34.6 ms: 1.08x faster                                                       |
| sphinx                           | 409 ms                                                         | 384 ms: 1.07x faster                                                        |
| spectral_norm                    | 43.7 ms                                                        | 41.1 ms: 1.06x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.7 ms: 1.06x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                       |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                       |
| logging_simple                   | 2.24 us                                                        | 2.14 us: 1.04x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 308 ms: 1.04x faster                                                        |
| json_loads                       | 10.8 us                                                        | 10.4 us: 1.04x faster                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.25 ms: 1.04x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 913 ns: 1.04x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.6 ms: 1.03x faster                                                       |
| comprehensions                   | 6.80 us                                                        | 6.58 us: 1.03x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.03x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.37 us: 1.03x faster                                                       |
| nbody                            | 42.5 ms                                                        | 41.3 ms: 1.03x faster                                                       |
| thrift                           | 309 us                                                         | 301 us: 1.03x faster                                                        |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 638 ms: 1.02x faster                                                        |
| pycparser                        | 470 ms                                                         | 463 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                       |
| mako                             | 4.41 ms                                                        | 4.34 ms: 1.02x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                       |
| deltablue                        | 1.45 ms                                                        | 1.43 ms: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 410 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.01x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 97.9 ms: 1.03x slower                                                       |
| raytrace                         | 109 ms                                                         | 112 ms: 1.03x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 42.0 ns: 1.03x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 54.4 ms: 1.04x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.04x slower                                                        |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                       |
| generators                       | 15.7 ms                                                        | 16.8 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.1 ms: 1.07x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.1 ms: 1.08x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.4 ms: 1.10x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 225 us: 1.12x slower                                                        |
| django_template                  | 12.5 ms                                                        | 14.5 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.37x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.7 ms: 3.21x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                                |

Benchmark hidden because not significant (3): connected_components, chaos, xml_etree_parse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261107-3.16.0a1+dev-ce4ac8c/bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x