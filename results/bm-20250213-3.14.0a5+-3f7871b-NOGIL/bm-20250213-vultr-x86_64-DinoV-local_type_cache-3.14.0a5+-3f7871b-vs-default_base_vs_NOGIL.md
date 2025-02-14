# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 3f7871b
- commit date: 2025-02-13
- overall geometric mean: 1.127x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 304 ms: 1.19x slower                                              |
| docutils       | 2.57 sec                                                               | 2.80 sec: 1.09x slower                                            |
| sphinx         | 981 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 579 ms: 1.08x faster                                              |
| async_tree_io              | 622 ms                                                                 | 606 ms: 1.03x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 260 ms: 1.02x faster                                              |
| coroutines                 | 22.2 ms                                                                | 23.3 ms: 1.05x slower                                             |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.07x slower                                              |
| async_tree_memoization     | 326 ms                                                                 | 356 ms: 1.09x slower                                              |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 559 ms: 1.12x slower                                              |
| async_generators           | 326 ms                                                                 | 374 ms: 1.15x slower                                              |
| async_tree_cpu_io_mixed    | 514 ms                                                                 | 591 ms: 1.15x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                      |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 72.5 ms                                                                | 76.6 ms: 1.06x slower                                             |
| pidigits       | 184 ms                                                                 | 206 ms: 1.12x slower                                              |
| nbody          | 91.6 ms                                                                | 129 ms: 1.41x slower                                              |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 23.1 ms: 1.05x faster                                             |
| regex_effbot   | 2.84 ms                                                                | 2.87 ms: 1.01x slower                                             |
| regex_dna      | 168 ms                                                                 | 185 ms: 1.10x slower                                              |
| regex_compile  | 128 ms                                                                 | 153 ms: 1.20x slower                                              |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 88.2 ms: 1.04x faster                                             |
| json_loads           | 28.9 us                                                                | 31.2 us: 1.08x slower                                             |
| pickle_pure_python   | 318 us                                                                 | 358 us: 1.13x slower                                              |
| json_dumps           | 11.4 ms                                                                | 12.9 ms: 1.13x slower                                             |
| unpickle_pure_python | 220 us                                                                 | 249 us: 1.13x slower                                              |
| xml_etree_generate   | 83.4 ms                                                                | 96.9 ms: 1.16x slower                                             |
| xml_etree_process    | 58.9 ms                                                                | 70.2 ms: 1.19x slower                                             |
| tomli_loads          | 1.95 sec                                                               | 2.35 sec: 1.21x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| python_startup_no_site | 7.48 ms                                                                | 9.64 ms: 1.29x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 42.4 ms: 1.22x slower                                             |
| genshi_xml      | 48.6 ms                                                                | 59.7 ms: 1.23x slower                                             |
| genshi_text     | 21.6 ms                                                                | 28.4 ms: 1.31x slower                                             |
| mako            | 11.7 ms                                                                | 16.0 ms: 1.37x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.43 ms                                                                | 1.75 ms: 2.54x faster                                             |
| create_gc_cycles           | 1.86 ms                                                                | 1.39 ms: 1.33x faster                                             |
| async_tree_io_tg           | 628 ms                                                                 | 579 ms: 1.08x faster                                              |
| sqlite_synth               | 2.20 us                                                                | 2.03 us: 1.08x faster                                             |
| regex_v8                   | 24.3 ms                                                                | 23.1 ms: 1.05x faster                                             |
| xml_etree_iterparse        | 91.5 ms                                                                | 88.2 ms: 1.04x faster                                             |
| async_tree_io              | 622 ms                                                                 | 606 ms: 1.03x faster                                              |
| async_tree_none_tg         | 265 ms                                                                 | 260 ms: 1.02x faster                                              |
| regex_effbot               | 2.84 ms                                                                | 2.87 ms: 1.01x slower                                             |
| pathlib                    | 18.7 ms                                                                | 19.2 ms: 1.02x slower                                             |
| json                       | 5.15 ms                                                                | 5.38 ms: 1.04x slower                                             |
| python_startup             | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| coroutines                 | 22.2 ms                                                                | 23.3 ms: 1.05x slower                                             |
| pycparser                  | 1.13 sec                                                               | 1.19 sec: 1.05x slower                                            |
| float                      | 72.5 ms                                                                | 76.6 ms: 1.06x slower                                             |
| logging_silent             | 105 ns                                                                 | 111 ns: 1.07x slower                                              |
| generators                 | 29.9 ms                                                                | 31.9 ms: 1.07x slower                                             |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.07x slower                                              |
| json_loads                 | 28.9 us                                                                | 31.2 us: 1.08x slower                                             |
| bench_mp_pool              | 87.7 ms                                                                | 94.9 ms: 1.08x slower                                             |
| docutils                   | 2.57 sec                                                               | 2.80 sec: 1.09x slower                                            |
| async_tree_memoization     | 326 ms                                                                 | 356 ms: 1.09x slower                                              |
| dulwich_log                | 75.8 ms                                                                | 83.1 ms: 1.10x slower                                             |
| scimark_sor                | 119 ms                                                                 | 131 ms: 1.10x slower                                              |
| regex_dna                  | 168 ms                                                                 | 185 ms: 1.10x slower                                              |
| bpe_tokeniser              | 4.22 sec                                                               | 4.69 sec: 1.11x slower                                            |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                 | 559 ms: 1.12x slower                                              |
| pidigits                   | 184 ms                                                                 | 206 ms: 1.12x slower                                              |
| pickle_pure_python         | 318 us                                                                 | 358 us: 1.13x slower                                              |
| json_dumps                 | 11.4 ms                                                                | 12.9 ms: 1.13x slower                                             |
| unpickle_pure_python       | 220 us                                                                 | 249 us: 1.13x slower                                              |
| sphinx                     | 981 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| k_core                     | 2.04 sec                                                               | 2.32 sec: 1.14x slower                                            |
| async_generators           | 326 ms                                                                 | 374 ms: 1.15x slower                                              |
| pylint                     | 279 ms                                                                 | 321 ms: 1.15x slower                                              |
| async_tree_cpu_io_mixed    | 514 ms                                                                 | 591 ms: 1.15x slower                                              |
| mdp                        | 2.33 sec                                                               | 2.71 sec: 1.16x slower                                            |
| xml_etree_generate         | 83.4 ms                                                                | 96.9 ms: 1.16x slower                                             |
| pyflate                    | 423 ms                                                                 | 493 ms: 1.16x slower                                              |
| telco                      | 7.30 ms                                                                | 8.54 ms: 1.17x slower                                             |
| go                         | 119 ms                                                                 | 140 ms: 1.17x slower                                              |
| pprint_safe_repr           | 701 ms                                                                 | 824 ms: 1.18x slower                                              |
| many_optionals             | 1.01 ms                                                                | 1.19 ms: 1.18x slower                                             |
| pprint_pformat             | 1.43 sec                                                               | 1.69 sec: 1.18x slower                                            |
| sqlglot_normalize          | 102 ms                                                                 | 121 ms: 1.18x slower                                              |
| subparsers                 | 21.8 ms                                                                | 25.8 ms: 1.18x slower                                             |
| 2to3                       | 256 ms                                                                 | 304 ms: 1.19x slower                                              |
| xml_etree_process          | 58.9 ms                                                                | 70.2 ms: 1.19x slower                                             |
| regex_compile              | 128 ms                                                                 | 153 ms: 1.20x slower                                              |
| sqlglot_optimize           | 51.4 ms                                                                | 61.7 ms: 1.20x slower                                             |
| spectral_norm              | 91.6 ms                                                                | 110 ms: 1.20x slower                                              |
| deepcopy_reduce            | 2.61 us                                                                | 3.14 us: 1.20x slower                                             |
| tomli_loads                | 1.95 sec                                                               | 2.35 sec: 1.21x slower                                            |
| coverage                   | 80.1 ms                                                                | 96.7 ms: 1.21x slower                                             |
| comprehensions             | 16.4 us                                                                | 19.8 us: 1.21x slower                                             |
| logging_simple             | 5.89 us                                                                | 7.14 us: 1.21x slower                                             |
| nqueens                    | 79.5 ms                                                                | 96.6 ms: 1.22x slower                                             |
| sqlglot_transpile          | 1.59 ms                                                                | 1.94 ms: 1.22x slower                                             |
| thrift                     | 735 us                                                                 | 897 us: 1.22x slower                                              |
| deepcopy                   | 252 us                                                                 | 308 us: 1.22x slower                                              |
| scimark_lu                 | 114 ms                                                                 | 139 ms: 1.22x slower                                              |
| django_template            | 34.6 ms                                                                | 42.4 ms: 1.22x slower                                             |
| sqlalchemy_declarative     | 127 ms                                                                 | 156 ms: 1.23x slower                                              |
| sympy_expand               | 450 ms                                                                 | 552 ms: 1.23x slower                                              |
| chaos                      | 56.5 ms                                                                | 69.4 ms: 1.23x slower                                             |
| hexiom                     | 6.01 ms                                                                | 7.38 ms: 1.23x slower                                             |
| raytrace                   | 265 ms                                                                 | 326 ms: 1.23x slower                                              |
| genshi_xml                 | 48.6 ms                                                                | 59.7 ms: 1.23x slower                                             |
| logging_format             | 6.61 us                                                                | 8.14 us: 1.23x slower                                             |
| sympy_sum                  | 152 ms                                                                 | 188 ms: 1.23x slower                                              |
| scimark_fft                | 314 ms                                                                 | 390 ms: 1.24x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.6 ms: 1.25x slower                                             |
| deepcopy_memo              | 30.3 us                                                                | 38.0 us: 1.25x slower                                             |
| sqlglot_parse              | 1.29 ms                                                                | 1.63 ms: 1.26x slower                                             |
| sympy_str                  | 269 ms                                                                 | 340 ms: 1.26x slower                                              |
| richards                   | 43.8 ms                                                                | 55.7 ms: 1.27x slower                                             |
| shortest_path              | 431 ms                                                                 | 550 ms: 1.27x slower                                              |
| deltablue                  | 3.22 ms                                                                | 4.10 ms: 1.27x slower                                             |
| sqlalchemy_imperative      | 19.2 ms                                                                | 24.5 ms: 1.28x slower                                             |
| connected_components       | 388 ms                                                                 | 497 ms: 1.28x slower                                              |
| fannkuch                   | 380 ms                                                                 | 487 ms: 1.28x slower                                              |
| python_startup_no_site     | 7.48 ms                                                                | 9.64 ms: 1.29x slower                                             |
| scimark_monte_carlo        | 65.1 ms                                                                | 84.5 ms: 1.30x slower                                             |
| crypto_pyaes               | 68.7 ms                                                                | 89.7 ms: 1.31x slower                                             |
| meteor_contest             | 99.4 ms                                                                | 130 ms: 1.31x slower                                              |
| genshi_text                | 21.6 ms                                                                | 28.4 ms: 1.31x slower                                             |
| scimark_sparse_mat_mult    | 4.40 ms                                                                | 5.78 ms: 1.31x slower                                             |
| typing_runtime_protocols   | 155 us                                                                 | 203 us: 1.31x slower                                              |
| richards_super             | 49.3 ms                                                                | 65.0 ms: 1.32x slower                                             |
| mako                       | 11.7 ms                                                                | 16.0 ms: 1.37x slower                                             |
| nbody                      | 91.6 ms                                                                | 129 ms: 1.41x slower                                              |
| bench_thread_pool          | 1.03 ms                                                                | 3.34 ms: 3.26x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                      |

Benchmark hidden because not significant (3): async_tree_memoization_tg, asyncio_websockets, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250213-3.14.0a5+-3f7871b-NOGIL/bm-20250213-vultr-x86_64-DinoV-local_type_cache-3.14.0a5+-3f7871b.json: html5lib

- Geometric mean (including insignificant results): 1.127x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.21x