# Results vs. base

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.144x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 245 ms                                                                                                            | 299 ms: 1.22x slower                                                                                                    |
| docutils       | 2.53 sec                                                                                                          | 2.83 sec: 1.12x slower                                                                                                  |
| sphinx         | 968 ms                                                                                                            | 1.11 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 605 ms                                                                                                            | 552 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 252 ms                                                                                                            | 239 ms: 1.05x faster                                                                                                    |
| async_tree_io              | 604 ms                                                                                                            | 582 ms: 1.04x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                                                            | 499 ms: 1.04x slower                                                                                                    |
| async_tree_none            | 259 ms                                                                                                            | 276 ms: 1.07x slower                                                                                                    |
| coroutines                 | 22.0 ms                                                                                                           | 23.7 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 531 ms: 1.08x slower                                                                                                    |
| async_tree_memoization     | 312 ms                                                                                                            | 343 ms: 1.10x slower                                                                                                    |
| async_generators           | 318 ms                                                                                                            | 377 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                                                            | 194 ms: 1.02x slower                                                                                                    |
| float          | 70.7 ms                                                                                                           | 76.9 ms: 1.09x slower                                                                                                   |
| nbody          | 85.3 ms                                                                                                           | 129 ms: 1.51x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.2 ms                                                                                                           | 23.0 ms: 1.05x faster                                                                                                   |
| regex_effbot   | 2.78 ms                                                                                                           | 2.84 ms: 1.02x slower                                                                                                   |
| regex_compile  | 123 ms                                                                                                            | 156 ms: 1.27x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.0 ms                                                                                                           | 88.0 ms: 1.02x faster                                                                                                   |
| json_loads           | 28.3 us                                                                                                           | 29.3 us: 1.04x slower                                                                                                   |
| json_dumps           | 11.0 ms                                                                                                           | 12.8 ms: 1.17x slower                                                                                                   |
| xml_etree_generate   | 82.1 ms                                                                                                           | 96.2 ms: 1.17x slower                                                                                                   |
| pickle_pure_python   | 299 us                                                                                                            | 362 us: 1.21x slower                                                                                                    |
| xml_etree_process    | 57.2 ms                                                                                                           | 70.1 ms: 1.23x slower                                                                                                   |
| unpickle_pure_python | 206 us                                                                                                            | 254 us: 1.23x slower                                                                                                    |
| tomli_loads          | 1.88 sec                                                                                                          | 2.40 sec: 1.28x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 8.53 ms                                                                                                           | 11.1 ms: 1.30x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.0 ms                                                                                                           | 60.0 ms: 1.28x slower                                                                                                   |
| django_template | 32.7 ms                                                                                                           | 42.6 ms: 1.30x slower                                                                                                   |
| mako            | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| genshi_text     | 20.6 ms                                                                                                           | 28.0 ms: 1.36x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.32x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.21 ms                                                                                                           | 1.74 ms: 2.42x faster                                                                                                   |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.33 ms: 1.39x faster                                                                                                   |
| async_tree_io_tg           | 605 ms                                                                                                            | 552 ms: 1.10x faster                                                                                                    |
| sqlite_synth               | 2.17 us                                                                                                           | 2.03 us: 1.07x faster                                                                                                   |
| async_tree_none_tg         | 252 ms                                                                                                            | 239 ms: 1.05x faster                                                                                                    |
| regex_v8                   | 24.2 ms                                                                                                           | 23.0 ms: 1.05x faster                                                                                                   |
| async_tree_io              | 604 ms                                                                                                            | 582 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 90.0 ms                                                                                                           | 88.0 ms: 1.02x faster                                                                                                   |
| pidigits                   | 191 ms                                                                                                            | 194 ms: 1.02x slower                                                                                                    |
| regex_effbot               | 2.78 ms                                                                                                           | 2.84 ms: 1.02x slower                                                                                                   |
| json                       | 4.95 ms                                                                                                           | 5.07 ms: 1.02x slower                                                                                                   |
| pathlib                    | 19.1 ms                                                                                                           | 19.7 ms: 1.03x slower                                                                                                   |
| json_loads                 | 28.3 us                                                                                                           | 29.3 us: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                                                            | 499 ms: 1.04x slower                                                                                                    |
| python_startup             | 14.8 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| async_tree_none            | 259 ms                                                                                                            | 276 ms: 1.07x slower                                                                                                    |
| coroutines                 | 22.0 ms                                                                                                           | 23.7 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                            | 531 ms: 1.08x slower                                                                                                    |
| pycparser                  | 1.10 sec                                                                                                          | 1.19 sec: 1.08x slower                                                                                                  |
| float                      | 70.7 ms                                                                                                           | 76.9 ms: 1.09x slower                                                                                                   |
| async_tree_memoization     | 312 ms                                                                                                            | 343 ms: 1.10x slower                                                                                                    |
| bench_mp_pool              | 86.7 ms                                                                                                           | 95.7 ms: 1.10x slower                                                                                                   |
| dulwich_log                | 65.6 ms                                                                                                           | 73.0 ms: 1.11x slower                                                                                                   |
| docutils                   | 2.53 sec                                                                                                          | 2.83 sec: 1.12x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                          | 2.30 sec: 1.14x slower                                                                                                  |
| sphinx                     | 968 ms                                                                                                            | 1.11 sec: 1.14x slower                                                                                                  |
| bpe_tokeniser              | 4.14 sec                                                                                                          | 4.77 sec: 1.15x slower                                                                                                  |
| mdp                        | 2.27 sec                                                                                                          | 2.62 sec: 1.16x slower                                                                                                  |
| many_optionals             | 1.01 ms                                                                                                           | 1.17 ms: 1.16x slower                                                                                                   |
| pylint                     | 273 ms                                                                                                            | 316 ms: 1.16x slower                                                                                                    |
| subparsers                 | 21.6 ms                                                                                                           | 25.2 ms: 1.17x slower                                                                                                   |
| json_dumps                 | 11.0 ms                                                                                                           | 12.8 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 82.1 ms                                                                                                           | 96.2 ms: 1.17x slower                                                                                                   |
| logging_silent             | 97.7 ns                                                                                                           | 115 ns: 1.18x slower                                                                                                    |
| async_generators           | 318 ms                                                                                                            | 377 ms: 1.19x slower                                                                                                    |
| pickle_pure_python         | 299 us                                                                                                            | 362 us: 1.21x slower                                                                                                    |
| telco                      | 7.34 ms                                                                                                           | 8.87 ms: 1.21x slower                                                                                                   |
| generators                 | 26.7 ms                                                                                                           | 32.4 ms: 1.21x slower                                                                                                   |
| 2to3                       | 245 ms                                                                                                            | 299 ms: 1.22x slower                                                                                                    |
| sqlglot_normalize          | 100 ms                                                                                                            | 123 ms: 1.22x slower                                                                                                    |
| sympy_expand               | 450 ms                                                                                                            | 552 ms: 1.23x slower                                                                                                    |
| coverage                   | 79.2 ms                                                                                                           | 97.1 ms: 1.23x slower                                                                                                   |
| xml_etree_process          | 57.2 ms                                                                                                           | 70.1 ms: 1.23x slower                                                                                                   |
| sqlglot_optimize           | 50.3 ms                                                                                                           | 61.7 ms: 1.23x slower                                                                                                   |
| unpickle_pure_python       | 206 us                                                                                                            | 254 us: 1.23x slower                                                                                                    |
| thrift                     | 716 us                                                                                                            | 891 us: 1.24x slower                                                                                                    |
| scimark_sor                | 111 ms                                                                                                            | 138 ms: 1.25x slower                                                                                                    |
| pprint_safe_repr           | 675 ms                                                                                                            | 841 ms: 1.25x slower                                                                                                    |
| scimark_fft                | 317 ms                                                                                                            | 396 ms: 1.25x slower                                                                                                    |
| sympy_sum                  | 150 ms                                                                                                            | 188 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 19.2 ms                                                                                                           | 24.1 ms: 1.25x slower                                                                                                   |
| spectral_norm              | 91.0 ms                                                                                                           | 114 ms: 1.26x slower                                                                                                    |
| sqlalchemy_declarative     | 125 ms                                                                                                            | 157 ms: 1.26x slower                                                                                                    |
| sqlalchemy_imperative      | 19.1 ms                                                                                                           | 24.0 ms: 1.26x slower                                                                                                   |
| sympy_str                  | 266 ms                                                                                                            | 335 ms: 1.26x slower                                                                                                    |
| comprehensions             | 15.8 us                                                                                                           | 19.8 us: 1.26x slower                                                                                                   |
| sqlglot_transpile          | 1.53 ms                                                                                                           | 1.92 ms: 1.26x slower                                                                                                   |
| shortest_path              | 430 ms                                                                                                            | 542 ms: 1.26x slower                                                                                                    |
| pyflate                    | 399 ms                                                                                                            | 503 ms: 1.26x slower                                                                                                    |
| pprint_pformat             | 1.38 sec                                                                                                          | 1.74 sec: 1.26x slower                                                                                                  |
| logging_format             | 6.47 us                                                                                                           | 8.17 us: 1.26x slower                                                                                                   |
| regex_compile              | 123 ms                                                                                                            | 156 ms: 1.27x slower                                                                                                    |
| logging_simple             | 5.75 us                                                                                                           | 7.31 us: 1.27x slower                                                                                                   |
| deepcopy                   | 246 us                                                                                                            | 313 us: 1.27x slower                                                                                                    |
| deltablue                  | 3.00 ms                                                                                                           | 3.82 ms: 1.28x slower                                                                                                   |
| tomli_loads                | 1.88 sec                                                                                                          | 2.40 sec: 1.28x slower                                                                                                  |
| genshi_xml                 | 47.0 ms                                                                                                           | 60.0 ms: 1.28x slower                                                                                                   |
| deepcopy_reduce            | 2.50 us                                                                                                           | 3.19 us: 1.28x slower                                                                                                   |
| connected_components       | 386 ms                                                                                                            | 497 ms: 1.29x slower                                                                                                    |
| chaos                      | 54.0 ms                                                                                                           | 69.7 ms: 1.29x slower                                                                                                   |
| scimark_lu                 | 110 ms                                                                                                            | 142 ms: 1.29x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.38 ms                                                                                                           | 5.67 ms: 1.29x slower                                                                                                   |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.60 ms: 1.30x slower                                                                                                   |
| go                         | 110 ms                                                                                                            | 142 ms: 1.30x slower                                                                                                    |
| crypto_pyaes               | 67.3 ms                                                                                                           | 87.5 ms: 1.30x slower                                                                                                   |
| django_template            | 32.7 ms                                                                                                           | 42.6 ms: 1.30x slower                                                                                                   |
| python_startup_no_site     | 8.53 ms                                                                                                           | 11.1 ms: 1.30x slower                                                                                                   |
| raytrace                   | 251 ms                                                                                                            | 328 ms: 1.30x slower                                                                                                    |
| typing_runtime_protocols   | 149 us                                                                                                            | 195 us: 1.31x slower                                                                                                    |
| meteor_contest             | 98.3 ms                                                                                                           | 129 ms: 1.32x slower                                                                                                    |
| nqueens                    | 73.5 ms                                                                                                           | 96.8 ms: 1.32x slower                                                                                                   |
| hexiom                     | 5.66 ms                                                                                                           | 7.51 ms: 1.33x slower                                                                                                   |
| richards                   | 41.2 ms                                                                                                           | 55.6 ms: 1.35x slower                                                                                                   |
| deepcopy_memo              | 28.6 us                                                                                                           | 38.7 us: 1.35x slower                                                                                                   |
| fannkuch                   | 368 ms                                                                                                            | 499 ms: 1.35x slower                                                                                                    |
| scimark_monte_carlo        | 62.3 ms                                                                                                           | 84.5 ms: 1.36x slower                                                                                                   |
| mako                       | 11.6 ms                                                                                                           | 15.7 ms: 1.36x slower                                                                                                   |
| genshi_text                | 20.6 ms                                                                                                           | 28.0 ms: 1.36x slower                                                                                                   |
| richards_super             | 47.1 ms                                                                                                           | 64.4 ms: 1.37x slower                                                                                                   |
| nbody                      | 85.3 ms                                                                                                           | 129 ms: 1.51x slower                                                                                                    |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.17 ms: 3.08x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (4): xml_etree_parse, asyncio_websockets, regex_dna, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-vultr-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json: html5lib

- Geometric mean (including insignificant results): 1.144x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.20x