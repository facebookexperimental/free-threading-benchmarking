# Results vs. 3.13.0rc2

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: darwin-arm64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.020x faster
- HPT reliability: 53.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 255 ms: 1.59x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                    |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 173 ms: 1.04x slower                                                    |
| nbody          | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 909 ms: 1.10x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| mako            | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.09x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| mdp                              | 1.06 sec                                                       | 514 ms: 2.06x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 257 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 255 ms: 1.59x faster                                                    |
| k_core                           | 1.46 sec                                                       | 957 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 257 ms: 1.50x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.31x faster                                                   |
| deepcopy                         | 145 us                                                         | 112 us: 1.30x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 50.4 ms: 1.27x faster                                                   |
| go                               | 72.6 ms                                                        | 57.5 ms: 1.26x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.24x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 150 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 107 ms: 1.23x faster                                                    |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 268 ms: 1.12x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.17 us: 1.11x faster                                                   |
| async_generators                 | 193 ms                                                         | 175 ms: 1.10x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 909 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.1 ms: 1.09x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.93 ms: 1.08x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.49 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.6 us: 1.03x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.7 ms: 1.03x faster                                                   |
| float                            | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 969 us: 1.03x faster                                                    |
| connected_components             | 208 ms                                                         | 203 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 219 ms: 1.02x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.78 ms: 1.02x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.7 ns: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.2 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 97.4 us: 1.02x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.4 ms: 1.02x faster                                                   |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.4 ms: 1.01x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.55 ms: 1.00x slower                                                   |
| fannkuch                         | 179 ms                                                         | 179 ms: 1.00x slower                                                    |
| asyncio_websockets               | 194 ms                                                         | 194 ms: 1.00x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.5 ms: 1.01x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.0 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.2 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.1 ms: 1.02x slower                                                   |
| sqlite_synth                     | 948 ns                                                         | 962 ns: 1.02x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 48.7 ms: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                  |
| genshi_xml                       | 21.4 ms                                                        | 21.8 ms: 1.02x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 44.6 ms: 1.02x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.90 ms: 1.03x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 672 ms: 1.03x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 64.6 ms: 1.03x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 333 ms: 1.04x slower                                                    |
| pidigits                         | 166 ms                                                         | 173 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.5 ms: 1.04x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.05x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.52 ms: 1.05x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 99.2 ms: 1.05x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.88 ms: 1.05x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.16 ms: 1.06x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                   |
| pycparser                        | 470 ms                                                         | 501 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.7 ms: 1.07x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.39 us: 1.07x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 133 ms: 1.07x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.37 us: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.7 ms: 1.08x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.4 ms: 1.09x slower                                                   |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                    |
| raytrace                         | 109 ms                                                         | 119 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.94 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.1 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| nbody                            | 42.5 ms                                                        | 48.1 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 133 ms: 1.30x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.86 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.2 ms: 3.08x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (2): pathlib, sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.020x faster

# HPT report

- Reliability score: 53.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x