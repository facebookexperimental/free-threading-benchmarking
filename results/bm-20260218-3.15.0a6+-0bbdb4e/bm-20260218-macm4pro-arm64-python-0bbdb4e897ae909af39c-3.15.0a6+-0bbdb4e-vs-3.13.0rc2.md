# Results vs. 3.13.0rc2

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: darwin-arm64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.046x faster
- HPT reliability: 96.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.06x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 872 ms: 1.15x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 64.5 ms: 1.03x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 146 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.46 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                    |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 224 ms: 2.32x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 558 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 232 ms: 1.75x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 910 ms: 1.61x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.16 ms: 1.51x faster                                                    |
| deepcopy                         | 145 us                                                         | 101 us: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.40x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 11.8 us: 1.40x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| go                               | 72.6 ms                                                        | 55.9 ms: 1.30x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 51.5 ms: 1.24x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.86 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 872 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 262 ms: 1.12x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.5 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.68 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 929 us: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.06x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.89 ms: 1.06x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.8 ms: 1.06x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 23.5 ms: 1.05x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.03 sec: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.1 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 119 ms: 1.04x faster                                                     |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 41.9 ms: 1.03x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.1 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 320 ms: 1.01x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.00x faster                                                   |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 25.6 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 227 ms: 1.01x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.01x slower                                                     |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| pycparser                        | 470 ms                                                         | 479 ms: 1.02x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 10.2 ms: 1.02x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 2.91 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.7 ms: 1.02x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 66.1 us: 1.02x slower                                                    |
| thrift                           | 309 us                                                         | 317 us: 1.02x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.72 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.9 ms: 1.03x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.51 us: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.5 ms: 1.03x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 103 us: 1.03x slower                                                     |
| coverage                         | 31.2 ms                                                        | 32.3 ms: 1.03x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.32 us: 1.04x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.96 ms: 1.04x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 46.1 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 436 us: 1.06x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.8 ms: 1.06x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.3 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.46 ms: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.09x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.3 ms: 1.09x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.46 us: 1.10x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 47.5 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.11x slower                                                     |
| nbody                            | 42.5 ms                                                        | 47.4 ms: 1.12x slower                                                    |
| raytrace                         | 109 ms                                                         | 122 ms: 1.12x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 146 us: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 121 ms: 1.18x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 39.7 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                    |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.3 ms: 1.35x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.2 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (5): async_tree_eager_cpu_io_mixed, pidigits, json_loads, xml_etree_generate, pprint_pformat
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-macm4pro-arm64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.046x faster

# HPT report

- Reliability score: 96.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x