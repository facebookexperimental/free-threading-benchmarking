# Results vs. 3.13.0rc2

- fork: python
- ref: a936af924efc6e2fb59e
- machine: darwin-arm64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.081x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 130 ms: 1.16x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 431 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.12x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.22x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 56.1 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 157 ms: 1.05x faster                                                     |
| float          | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                    |
| nbody          | 42.5 ms                                                        | 78.2 ms: 1.84x slower                                                    |
| Geometric mean | (ref)                                                          | 1.25x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 90.4 ms: 1.05x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 58.4 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 40.5 ms: 1.13x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 127 us: 1.27x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 168 us: 1.29x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.20 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.8 ms: 1.29x slower                                                    |
| mako            | 4.41 ms                                                        | 6.17 ms: 1.40x slower                                                    |
| django_template | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 229 ms: 2.29x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 901 us: 2.27x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 476 us: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.39x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 138 ms: 1.34x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 99.0 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 253 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 830 ns: 1.14x faster                                                     |
| deepcopy                         | 145 us                                                         | 128 us: 1.14x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 57.9 ms: 1.08x faster                                                    |
| pidigits                         | 166 ms                                                         | 157 ms: 1.05x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 90.4 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.4 ms: 1.02x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_generators                 | 193 ms                                                         | 190 ms: 1.02x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 38.1 ms: 1.01x slower                                                    |
| go                               | 72.6 ms                                                        | 73.4 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.5 ms: 1.03x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.0 ms: 1.04x slower                                                    |
| pyflate                          | 222 ms                                                         | 231 ms: 1.04x slower                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 17.2 us: 1.05x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.24 sec: 1.05x slower                                                   |
| sphinx                           | 409 ms                                                         | 431 ms: 1.05x slower                                                     |
| tomli_loads                      | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.12 ms: 1.06x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.37 us: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 500 ms: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.07x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 69.6 ms: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.11 ms: 1.10x slower                                                    |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                     |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.18 sec: 1.12x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.1 ms: 1.12x slower                                                    |
| float                            | 31.4 ms                                                        | 35.3 ms: 1.12x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 40.5 ms: 1.13x slower                                                    |
| connected_components             | 208 ms                                                         | 236 ms: 1.13x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.53 ms: 1.15x slower                                                    |
| 2to3                             | 112 ms                                                         | 130 ms: 1.16x slower                                                     |
| sqlglot_optimize                 | 22.2 ms                                                        | 25.8 ms: 1.16x slower                                                    |
| pylint                           | 106 ms                                                         | 123 ms: 1.16x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 62.6 ms: 1.20x slower                                                    |
| sqlglot_normalize                | 116 ms                                                         | 139 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.20 ms: 1.21x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 25.9 ms: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 37.9 ms: 1.21x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 58.4 ms: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 79.1 us: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 126 ms: 1.22x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 9.25 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 59.6 ms: 1.24x slower                                                    |
| fannkuch                         | 179 ms                                                         | 222 ms: 1.24x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 30.8 ms: 1.25x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 119 ms: 1.25x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 200 ms: 1.25x slower                                                     |
| logging_format                   | 2.45 us                                                        | 3.09 us: 1.26x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 408 ms: 1.27x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.84 us: 1.27x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 127 us: 1.27x slower                                                     |
| sqlglot_transpile                | 637 us                                                         | 814 us: 1.28x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 833 ms: 1.28x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 12.8 ms: 1.29x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 168 us: 1.29x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 56.1 ms: 1.30x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                     |
| sqlglot_parse                    | 519 us                                                         | 680 us: 1.31x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 49.0 ms: 1.32x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.0 ms: 1.34x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.95 ms: 1.34x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 58.9 ms: 1.35x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 46.0 ms: 1.37x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 55.7 ns: 1.37x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.6 ms: 1.38x slower                                                    |
| chaos                            | 24.3 ms                                                        | 33.6 ms: 1.38x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.94 ms: 1.38x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.17 ms: 1.40x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.49 ms: 1.40x slower                                                    |
| django_template                  | 12.5 ms                                                        | 18.0 ms: 1.44x slower                                                    |
| raytrace                         | 109 ms                                                         | 157 ms: 1.44x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 10.0 us: 1.47x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.28 ms: 1.48x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 618 us: 1.50x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 65.7 ms: 1.54x slower                                                    |
| nbody                            | 42.5 ms                                                        | 78.2 ms: 1.84x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.6 ms: 3.03x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.09x slower                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization
Ignored benchmarks (7) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.16x