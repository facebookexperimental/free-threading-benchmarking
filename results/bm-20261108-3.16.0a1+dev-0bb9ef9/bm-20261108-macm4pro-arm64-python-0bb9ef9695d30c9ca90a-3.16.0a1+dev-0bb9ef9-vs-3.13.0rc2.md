# Results vs. 3.13.0rc2

- fork: python
- ref: 0bb9ef9695d30c9ca90a
- machine: darwin-arm64
- commit hash: 0bb9ef9
- commit date: 2026-11-08
- overall geometric mean: 1.104x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                        |
| docutils       | 1.05 sec                                                       | 902 ms: 1.16x faster                                                        |
| html5lib       | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| sphinx         | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.1 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                        |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 9.71 ms: 1.11x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.13x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| pidigits       | 166 ms                                                         | 149 ms: 1.12x faster                                                        |
| nbody          | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                          | 1.08x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 90.9 ms: 1.04x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 819 ms: 1.22x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.5 ms: 1.08x faster                                                       |
| unpickle_pure_python | 99.5 us                                                        | 92.3 us: 1.08x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 66.5 ms: 1.06x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.07x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mdp                              | 1.06 sec                                                       | 504 ms: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 50.9 ms: 2.07x faster                                                       |
| async_tree_eager_io              | 525 ms                                                         | 262 ms: 2.00x faster                                                        |
| async_generators                 | 193 ms                                                         | 98.1 ms: 1.97x faster                                                       |
| async_tree_eager_io_tg           | 521 ms                                                         | 276 ms: 1.89x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                       |
| create_gc_cycles                 | 993 us                                                         | 636 us: 1.56x faster                                                        |
| deepcopy                         | 145 us                                                         | 95.4 us: 1.52x faster                                                       |
| k_core                           | 1.46 sec                                                       | 984 ms: 1.49x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 269 ms: 1.44x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 45.4 us: 1.42x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 11.7 us: 1.41x faster                                                       |
| go                               | 72.6 ms                                                        | 52.0 ms: 1.39x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 110 ms: 1.30x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 49.6 ms: 1.29x faster                                                       |
| json_dumps                       | 4.65 ms                                                        | 3.61 ms: 1.29x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.04 us: 1.24x faster                                                       |
| pyflate                          | 222 ms                                                         | 181 ms: 1.22x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 819 ms: 1.22x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| async_tree_none_tg               | 133 ms                                                         | 111 ms: 1.19x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 157 ms: 1.18x faster                                                        |
| docutils                         | 1.05 sec                                                       | 902 ms: 1.16x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.27 ms: 1.15x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 160 ms: 1.15x faster                                                        |
| float                            | 31.4 ms                                                        | 27.3 ms: 1.15x faster                                                       |
| gc_traversal                     | 2.04 ms                                                        | 1.78 ms: 1.15x faster                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 26.1 ms: 1.14x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.87 sec: 1.14x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 20.5 ms: 1.13x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 269 ms: 1.12x faster                                                        |
| pidigits                         | 166 ms                                                         | 149 ms: 1.12x faster                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                        |
| fannkuch                         | 179 ms                                                         | 160 ms: 1.11x faster                                                        |
| scimark_fft                      | 124 ms                                                         | 111 ms: 1.11x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                       |
| coroutines                       | 10.8 ms                                                        | 9.71 ms: 1.11x faster                                                       |
| richards                         | 22.1 ms                                                        | 20.1 ms: 1.10x faster                                                       |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                        |
| nqueens                          | 37.2 ms                                                        | 34.2 ms: 1.09x faster                                                       |
| hexiom                           | 2.85 ms                                                        | 2.62 ms: 1.09x faster                                                       |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.5 ms: 1.08x faster                                                       |
| telco                            | 3.07 ms                                                        | 2.83 ms: 1.08x faster                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 92.3 us: 1.08x faster                                                       |
| richards_super                   | 24.7 ms                                                        | 23.0 ms: 1.07x faster                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 40.4 ms: 1.07x faster                                                       |
| spectral_norm                    | 43.7 ms                                                        | 41.5 ms: 1.05x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.21 ms: 1.05x faster                                                       |
| sphinx                           | 409 ms                                                         | 390 ms: 1.05x faster                                                        |
| xml_etree_generate               | 35.8 ms                                                        | 34.3 ms: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.86 ms: 1.04x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 90.9 ms: 1.04x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                        |
| logging_simple                   | 2.24 us                                                        | 2.16 us: 1.03x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 312 ms: 1.03x faster                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 7.33 ms: 1.03x faster                                                       |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                        |
| sqlite_synth                     | 948 ns                                                         | 928 ns: 1.02x faster                                                        |
| thrift                           | 309 us                                                         | 303 us: 1.02x faster                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.75 ms: 1.02x faster                                                       |
| pprint_pformat                   | 650 ms                                                         | 642 ms: 1.01x faster                                                        |
| connected_components             | 208 ms                                                         | 206 ms: 1.01x faster                                                        |
| logging_format                   | 2.45 us                                                        | 2.42 us: 1.01x faster                                                       |
| bench_thread_pool                | 412 us                                                         | 409 us: 1.01x faster                                                        |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                        |
| comprehensions                   | 6.80 us                                                        | 6.83 us: 1.00x slower                                                       |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                        |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                        |
| nbody                            | 42.5 ms                                                        | 43.1 ms: 1.01x slower                                                       |
| chaos                            | 24.3 ms                                                        | 24.7 ms: 1.02x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 49.2 ms: 1.03x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 98.8 ms: 1.04x slower                                                       |
| raytrace                         | 109 ms                                                         | 113 ms: 1.04x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 42.6 ns: 1.05x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 168 ms: 1.05x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.05x slower                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 66.5 ms: 1.06x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                        |
| python_startup_no_site           | 5.95 ms                                                        | 6.42 ms: 1.08x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 46.3 ms: 1.08x slower                                                       |
| generators                       | 15.7 ms                                                        | 17.1 ms: 1.09x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 53.7 ms: 1.12x slower                                                       |
| many_optionals                   | 200 us                                                         | 226 us: 1.13x slower                                                        |
| pathlib                          | 11.1 ms                                                        | 12.7 ms: 1.14x slower                                                       |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 141 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                       |
| Geometric mean                   | (ref)                                                          | 1.10x faster                                                                |

Benchmark hidden because not significant (2): mako, deltablue
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261108-3.16.0a1+dev-0bb9ef9/bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.104x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x