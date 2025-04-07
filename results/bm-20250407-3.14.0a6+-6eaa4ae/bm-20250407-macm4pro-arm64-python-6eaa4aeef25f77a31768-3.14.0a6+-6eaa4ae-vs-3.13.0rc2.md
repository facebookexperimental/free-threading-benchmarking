# Results vs. 3.13.0rc2

- fork: python
- ref: 6eaa4aeef25f77a31768
- machine: darwin-arm64
- commit hash: 6eaa4ae
- commit date: 2025-04-07
- overall geometric mean: 1.029x faster
- HPT reliability: 78.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 170 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.1 ms: 3.08x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 50.4 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                    |
| regex_dna      | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 927 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 144 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| mako            | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 245 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                     |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 248 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 946 ms: 1.55x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.30x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 147 ms: 1.26x faster                                                     |
| go                               | 72.6 ms                                                        | 58.0 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 51.5 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 254 ms: 1.18x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 862 us: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.13x faster                                                    |
| async_generators                 | 193 ms                                                         | 170 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.93 sec: 1.10x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.90 ms: 1.08x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 927 ms: 1.08x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                    |
| float                            | 31.4 ms                                                        | 29.4 ms: 1.07x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.98 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 927 ns: 1.02x faster                                                     |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.02 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.43 ms: 1.01x faster                                                    |
| 2to3                             | 112 ms                                                         | 110 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 42.7 ms: 1.01x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.83 ms: 1.01x faster                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 44.6 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.5 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.3 ms: 1.01x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.0 ms: 1.01x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 10.1 ms: 1.01x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 25.7 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| richards                         | 22.1 ms                                                        | 22.4 ms: 1.02x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.5 ns: 1.02x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 102 us: 1.02x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 96.8 ms: 1.02x slower                                                    |
| fannkuch                         | 179 ms                                                         | 183 ms: 1.02x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.02x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 25.3 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.1 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 670 ms: 1.03x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 487 ms: 1.04x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 99.6 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 39.6 ms: 1.05x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 167 ms: 1.05x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 39.2 ms: 1.05x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 434 us: 1.05x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 130 ms: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.4 ms: 1.06x slower                                                    |
| pylint                           | 106 ms                                                         | 112 ms: 1.06x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.54 ms: 1.06x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.98 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.37 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 47.6 ms: 1.09x slower                                                    |
| chaos                            | 24.3 ms                                                        | 26.5 ms: 1.09x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.83 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 37.1 ms: 1.10x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 144 us: 1.11x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 47.4 ms: 1.11x slower                                                    |
| raytrace                         | 109 ms                                                         | 121 ms: 1.11x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.99 ms: 1.12x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.62 us: 1.12x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.72 ms: 1.13x slower                                                    |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.0 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| nbody                            | 42.5 ms                                                        | 50.4 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 132 ms: 1.29x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 8.60 ms: 1.37x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.1 ms: 3.08x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (4): sphinx, coverage, scimark_monte_carlo, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250407-3.14.0a6+-6eaa4ae/bm-20250407-macm4pro-arm64-python-6eaa4aeef25f77a31768-3.14.0a6+-6eaa4ae.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 78.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.08x