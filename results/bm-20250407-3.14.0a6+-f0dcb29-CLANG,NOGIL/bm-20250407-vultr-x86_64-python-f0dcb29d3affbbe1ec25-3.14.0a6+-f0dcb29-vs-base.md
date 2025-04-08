# Results vs. base

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.005x faster
- HPT reliability: 87.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                                                            | 268 ms: 1.05x slower                                                                                                          |
| docutils       | 2.58 sec                                                                                                          | 2.63 sec: 1.02x slower                                                                                                        |
| sphinx         | 1000 ms                                                                                                           | 1.02 sec: 1.02x slower                                                                                                        |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 631 ms                                                                                                            | 476 ms: 1.33x faster                                                                                                          |
| async_tree_none_tg         | 265 ms                                                                                                            | 208 ms: 1.27x faster                                                                                                          |
| async_tree_io              | 632 ms                                                                                                            | 508 ms: 1.25x faster                                                                                                          |
| async_tree_memoization_tg  | 324 ms                                                                                                            | 262 ms: 1.24x faster                                                                                                          |
| coroutines                 | 24.5 ms                                                                                                           | 20.0 ms: 1.22x faster                                                                                                         |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                                                            | 426 ms: 1.17x faster                                                                                                          |
| async_tree_none            | 282 ms                                                                                                            | 242 ms: 1.16x faster                                                                                                          |
| async_tree_memoization     | 321 ms                                                                                                            | 290 ms: 1.10x faster                                                                                                          |
| async_tree_cpu_io_mixed    | 503 ms                                                                                                            | 456 ms: 1.10x faster                                                                                                          |
| async_generators           | 337 ms                                                                                                            | 321 ms: 1.05x faster                                                                                                          |
| asyncio_websockets         | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                          |
| Geometric mean             | (ref)                                                                                                             | 1.17x faster                                                                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| float          | 71.4 ms                                                                                                           | 64.2 ms: 1.11x faster                                                                                                         |
| pidigits       | 190 ms                                                                                                            | 187 ms: 1.02x faster                                                                                                          |
| nbody          | 92.6 ms                                                                                                           | 110 ms: 1.18x slower                                                                                                          |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.1 ms                                                                                                           | 21.7 ms: 1.02x faster                                                                                                         |
| regex_compile  | 130 ms                                                                                                            | 134 ms: 1.03x slower                                                                                                          |
| regex_dna      | 181 ms                                                                                                            | 188 ms: 1.04x slower                                                                                                          |
| regex_effbot   | 2.84 ms                                                                                                           | 3.03 ms: 1.07x slower                                                                                                         |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.7 ms                                                                                                           | 84.3 ms: 1.11x faster                                                                                                         |
| pickle_pure_python   | 322 us                                                                                                            | 308 us: 1.04x faster                                                                                                          |
| tomli_loads          | 1.99 sec                                                                                                          | 1.94 sec: 1.03x faster                                                                                                        |
| unpickle_pure_python | 222 us                                                                                                            | 218 us: 1.02x faster                                                                                                          |
| json_loads           | 27.7 us                                                                                                           | 28.8 us: 1.04x slower                                                                                                         |
| xml_etree_parse      | 130 ms                                                                                                            | 142 ms: 1.09x slower                                                                                                          |
| json_dumps           | 11.2 ms                                                                                                           | 12.7 ms: 1.13x slower                                                                                                         |
| Geometric mean       | (ref)                                                                                                             | 1.01x slower                                                                                                                  |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                                                           | 15.6 ms: 1.03x slower                                                                                                         |
| python_startup_no_site | 8.64 ms                                                                                                           | 11.0 ms: 1.27x slower                                                                                                         |
| Geometric mean         | (ref)                                                                                                             | 1.15x slower                                                                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                           | 36.1 ms: 1.01x faster                                                                                                         |
| genshi_text     | 22.0 ms                                                                                                           | 23.0 ms: 1.05x slower                                                                                                         |
| mako            | 12.2 ms                                                                                                           | 14.1 ms: 1.15x slower                                                                                                         |
| Geometric mean  | (ref)                                                                                                             | 1.05x slower                                                                                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json | results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                                                           | 2.11 ms: 2.02x faster                                                                                                         |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.36 ms: 1.36x faster                                                                                                         |
| async_tree_io_tg           | 631 ms                                                                                                            | 476 ms: 1.33x faster                                                                                                          |
| logging_silent             | 101 ns                                                                                                            | 78.6 ns: 1.28x faster                                                                                                         |
| async_tree_none_tg         | 265 ms                                                                                                            | 208 ms: 1.27x faster                                                                                                          |
| async_tree_io              | 632 ms                                                                                                            | 508 ms: 1.25x faster                                                                                                          |
| async_tree_memoization_tg  | 324 ms                                                                                                            | 262 ms: 1.24x faster                                                                                                          |
| coroutines                 | 24.5 ms                                                                                                           | 20.0 ms: 1.22x faster                                                                                                         |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                                                            | 426 ms: 1.17x faster                                                                                                          |
| async_tree_none            | 282 ms                                                                                                            | 242 ms: 1.16x faster                                                                                                          |
| sqlite_synth               | 2.18 us                                                                                                           | 1.95 us: 1.12x faster                                                                                                         |
| xml_etree_iterparse        | 93.7 ms                                                                                                           | 84.3 ms: 1.11x faster                                                                                                         |
| float                      | 71.4 ms                                                                                                           | 64.2 ms: 1.11x faster                                                                                                         |
| async_tree_memoization     | 321 ms                                                                                                            | 290 ms: 1.10x faster                                                                                                          |
| async_tree_cpu_io_mixed    | 503 ms                                                                                                            | 456 ms: 1.10x faster                                                                                                          |
| scimark_sor                | 115 ms                                                                                                            | 106 ms: 1.09x faster                                                                                                          |
| pathlib                    | 19.7 ms                                                                                                           | 18.6 ms: 1.06x faster                                                                                                         |
| scimark_lu                 | 117 ms                                                                                                            | 111 ms: 1.06x faster                                                                                                          |
| generators                 | 29.2 ms                                                                                                           | 27.7 ms: 1.06x faster                                                                                                         |
| async_generators           | 337 ms                                                                                                            | 321 ms: 1.05x faster                                                                                                          |
| spectral_norm              | 98.0 ms                                                                                                           | 93.5 ms: 1.05x faster                                                                                                         |
| pickle_pure_python         | 322 us                                                                                                            | 308 us: 1.04x faster                                                                                                          |
| bpe_tokeniser              | 4.35 sec                                                                                                          | 4.19 sec: 1.04x faster                                                                                                        |
| deepcopy_reduce            | 2.69 us                                                                                                           | 2.59 us: 1.04x faster                                                                                                         |
| deepcopy                   | 262 us                                                                                                            | 254 us: 1.03x faster                                                                                                          |
| tomli_loads                | 1.99 sec                                                                                                          | 1.94 sec: 1.03x faster                                                                                                        |
| nqueens                    | 80.8 ms                                                                                                           | 79.1 ms: 1.02x faster                                                                                                         |
| pidigits                   | 190 ms                                                                                                            | 187 ms: 1.02x faster                                                                                                          |
| regex_v8                   | 22.1 ms                                                                                                           | 21.7 ms: 1.02x faster                                                                                                         |
| comprehensions             | 17.3 us                                                                                                           | 17.0 us: 1.02x faster                                                                                                         |
| unpickle_pure_python       | 222 us                                                                                                            | 218 us: 1.02x faster                                                                                                          |
| scimark_fft                | 321 ms                                                                                                            | 316 ms: 1.02x faster                                                                                                          |
| pycparser                  | 1.17 sec                                                                                                          | 1.15 sec: 1.01x faster                                                                                                        |
| django_template            | 36.6 ms                                                                                                           | 36.1 ms: 1.01x faster                                                                                                         |
| asyncio_websockets         | 517 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                          |
| hexiom                     | 6.12 ms                                                                                                           | 6.11 ms: 1.00x faster                                                                                                         |
| deltablue                  | 3.36 ms                                                                                                           | 3.41 ms: 1.01x slower                                                                                                         |
| go                         | 114 ms                                                                                                            | 116 ms: 1.02x slower                                                                                                          |
| scimark_monte_carlo        | 63.8 ms                                                                                                           | 64.8 ms: 1.02x slower                                                                                                         |
| sqlglot_v2_optimize        | 52.5 ms                                                                                                           | 53.4 ms: 1.02x slower                                                                                                         |
| pprint_safe_repr           | 732 ms                                                                                                            | 746 ms: 1.02x slower                                                                                                          |
| docutils                   | 2.58 sec                                                                                                          | 2.63 sec: 1.02x slower                                                                                                        |
| many_optionals             | 1.04 ms                                                                                                           | 1.06 ms: 1.02x slower                                                                                                         |
| sphinx                     | 1000 ms                                                                                                           | 1.02 sec: 1.02x slower                                                                                                        |
| dulwich_log                | 68.9 ms                                                                                                           | 70.4 ms: 1.02x slower                                                                                                         |
| pprint_pformat             | 1.49 sec                                                                                                          | 1.52 sec: 1.02x slower                                                                                                        |
| richards                   | 44.5 ms                                                                                                           | 45.7 ms: 1.03x slower                                                                                                         |
| json                       | 4.96 ms                                                                                                           | 5.10 ms: 1.03x slower                                                                                                         |
| sqlglot_v2_transpile       | 1.59 ms                                                                                                           | 1.64 ms: 1.03x slower                                                                                                         |
| logging_simple             | 6.24 us                                                                                                           | 6.42 us: 1.03x slower                                                                                                         |
| scimark_sparse_mat_mult    | 4.40 ms                                                                                                           | 4.52 ms: 1.03x slower                                                                                                         |
| raytrace                   | 260 ms                                                                                                            | 267 ms: 1.03x slower                                                                                                          |
| regex_compile              | 130 ms                                                                                                            | 134 ms: 1.03x slower                                                                                                          |
| python_startup             | 15.1 ms                                                                                                           | 15.6 ms: 1.03x slower                                                                                                         |
| sympy_expand               | 471 ms                                                                                                            | 489 ms: 1.04x slower                                                                                                          |
| regex_dna                  | 181 ms                                                                                                            | 188 ms: 1.04x slower                                                                                                          |
| json_loads                 | 27.7 us                                                                                                           | 28.8 us: 1.04x slower                                                                                                         |
| sympy_sum                  | 159 ms                                                                                                            | 166 ms: 1.04x slower                                                                                                          |
| mdp                        | 1.18 sec                                                                                                          | 1.23 sec: 1.04x slower                                                                                                        |
| telco                      | 7.29 ms                                                                                                           | 7.60 ms: 1.04x slower                                                                                                         |
| sympy_str                  | 281 ms                                                                                                            | 294 ms: 1.05x slower                                                                                                          |
| genshi_text                | 22.0 ms                                                                                                           | 23.0 ms: 1.05x slower                                                                                                         |
| sympy_integrate            | 19.6 ms                                                                                                           | 20.5 ms: 1.05x slower                                                                                                         |
| fannkuch                   | 396 ms                                                                                                            | 416 ms: 1.05x slower                                                                                                          |
| k_core                     | 2.06 sec                                                                                                          | 2.17 sec: 1.05x slower                                                                                                        |
| subparsers                 | 22.5 ms                                                                                                           | 23.7 ms: 1.05x slower                                                                                                         |
| 2to3                       | 255 ms                                                                                                            | 268 ms: 1.05x slower                                                                                                          |
| logging_format             | 6.92 us                                                                                                           | 7.28 us: 1.05x slower                                                                                                         |
| typing_runtime_protocols   | 162 us                                                                                                            | 171 us: 1.05x slower                                                                                                          |
| sqlglot_v2_parse           | 1.28 ms                                                                                                           | 1.35 ms: 1.05x slower                                                                                                         |
| bench_mp_pool              | 88.9 ms                                                                                                           | 93.9 ms: 1.06x slower                                                                                                         |
| pyflate                    | 420 ms                                                                                                            | 447 ms: 1.07x slower                                                                                                          |
| deepcopy_memo              | 29.7 us                                                                                                           | 31.6 us: 1.07x slower                                                                                                         |
| regex_effbot               | 2.84 ms                                                                                                           | 3.03 ms: 1.07x slower                                                                                                         |
| richards_super             | 50.3 ms                                                                                                           | 53.7 ms: 1.07x slower                                                                                                         |
| xml_etree_parse            | 130 ms                                                                                                            | 142 ms: 1.09x slower                                                                                                          |
| crypto_pyaes               | 69.7 ms                                                                                                           | 77.1 ms: 1.11x slower                                                                                                         |
| sqlalchemy_declarative     | 132 ms                                                                                                            | 146 ms: 1.11x slower                                                                                                          |
| sqlalchemy_imperative      | 20.6 ms                                                                                                           | 22.8 ms: 1.11x slower                                                                                                         |
| json_dumps                 | 11.2 ms                                                                                                           | 12.7 ms: 1.13x slower                                                                                                         |
| mako                       | 12.2 ms                                                                                                           | 14.1 ms: 1.15x slower                                                                                                         |
| shortest_path              | 441 ms                                                                                                            | 513 ms: 1.16x slower                                                                                                          |
| coverage                   | 79.9 ms                                                                                                           | 93.4 ms: 1.17x slower                                                                                                         |
| nbody                      | 92.6 ms                                                                                                           | 110 ms: 1.18x slower                                                                                                          |
| meteor_contest             | 101 ms                                                                                                            | 120 ms: 1.20x slower                                                                                                          |
| connected_components       | 399 ms                                                                                                            | 479 ms: 1.20x slower                                                                                                          |
| python_startup_no_site     | 8.64 ms                                                                                                           | 11.0 ms: 1.27x slower                                                                                                         |
| bench_thread_pool          | 1.06 ms                                                                                                           | 3.07 ms: 2.91x slower                                                                                                         |
| Geometric mean             | (ref)                                                                                                             | 1.00x slower                                                                                                                  |

Benchmark hidden because not significant (6): xml_etree_process, sqlglot_v2_normalize, chaos, genshi_xml, xml_etree_generate, pylint
Ignored benchmarks (1) of results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: html5lib

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 87.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.24x