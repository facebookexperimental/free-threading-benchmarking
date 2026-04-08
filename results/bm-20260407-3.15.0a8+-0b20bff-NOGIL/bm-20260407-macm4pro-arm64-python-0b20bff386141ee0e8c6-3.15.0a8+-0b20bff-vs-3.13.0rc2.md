# Results vs. 3.13.0rc2

- fork: python
- ref: 0b20bff386141ee0e8c6
- machine: darwin-arm64
- commit hash: 0b20bff
- commit date: 2026-04-07
- overall geometric mean: 1.019x faster
- HPT reliability: 52.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 988 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.9 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.06 ms: 1.19x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 796 us: 2.57x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 240 ms: 2.17x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.14x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 510 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 605 ms: 1.75x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.11 ms: 1.52x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.24x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.24x faster                                                     |
| go                               | 72.6 ms                                                        | 59.2 ms: 1.23x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 781 ns: 1.21x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.93 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 256 ms: 1.17x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 859 ms: 1.16x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                    |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.9 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.15 us: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| float                            | 31.4 ms                                                        | 28.4 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| docutils                         | 1.05 sec                                                       | 988 ms: 1.06x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.06x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 61.1 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| pycparser                        | 470 ms                                                         | 455 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.01 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 176 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.1 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 418 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.02x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 673 ms: 1.04x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| pylint                           | 106 ms                                                         | 110 ms: 1.04x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.57 us: 1.05x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.5 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.3 ms: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 26.8 ms: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.03 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 40.6 ms: 1.09x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.3 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.6 ns: 1.10x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.0 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.13 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                     |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.11x slower                                                     |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.70 ms: 1.12x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 72.7 us: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.63 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 60.6 ms: 1.16x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                    |
| raytrace                         | 109 ms                                                         | 126 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.06 ms: 1.19x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.17 us: 1.20x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.8 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.9 ms: 1.25x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.9 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.1 ms: 1.31x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.8 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 568 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.3 ms: 3.23x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260407-3.15.0a8+-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8+-0b20bff.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 52.66% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.32x