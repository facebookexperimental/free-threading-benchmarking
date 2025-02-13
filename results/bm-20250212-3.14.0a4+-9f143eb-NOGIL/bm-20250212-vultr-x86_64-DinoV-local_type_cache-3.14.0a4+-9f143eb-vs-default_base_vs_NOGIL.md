# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 9f143eb
- commit date: 2025-02-12
- overall geometric mean: 1.133x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 305 ms: 1.21x slower                                              |
| docutils       | 2.55 sec                                                               | 2.80 sec: 1.10x slower                                            |
| sphinx         | 976 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 630 ms                                                                 | 574 ms: 1.10x faster                                              |
| async_tree_io              | 623 ms                                                                 | 602 ms: 1.04x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 503 ms: 1.03x slower                                              |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 534 ms: 1.07x slower                                              |
| async_tree_none            | 269 ms                                                                 | 287 ms: 1.07x slower                                              |
| coroutines                 | 21.4 ms                                                                | 23.3 ms: 1.09x slower                                             |
| async_tree_memoization     | 321 ms                                                                 | 352 ms: 1.10x slower                                              |
| async_generators           | 325 ms                                                                 | 370 ms: 1.14x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                      |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 187 ms                                                                 | 199 ms: 1.07x slower                                              |
| float          | 70.0 ms                                                                | 75.3 ms: 1.08x slower                                             |
| nbody          | 89.8 ms                                                                | 132 ms: 1.47x slower                                              |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                             |
| regex_effbot   | 2.73 ms                                                                | 2.80 ms: 1.03x slower                                             |
| regex_dna      | 164 ms                                                                 | 178 ms: 1.08x slower                                              |
| regex_compile  | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.1 ms                                                                | 87.0 ms: 1.05x faster                                             |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                              |
| json_loads           | 28.6 us                                                                | 31.2 us: 1.09x slower                                             |
| json_dumps           | 11.5 ms                                                                | 12.7 ms: 1.10x slower                                             |
| pickle_pure_python   | 311 us                                                                 | 358 us: 1.15x slower                                              |
| unpickle_pure_python | 212 us                                                                 | 245 us: 1.16x slower                                              |
| xml_etree_generate   | 82.6 ms                                                                | 97.6 ms: 1.18x slower                                             |
| xml_etree_process    | 57.6 ms                                                                | 68.8 ms: 1.20x slower                                             |
| tomli_loads          | 1.90 sec                                                               | 2.33 sec: 1.22x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                             |
| python_startup_no_site | 7.47 ms                                                                | 9.69 ms: 1.30x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| genshi_xml      | 47.0 ms                                                                | 59.2 ms: 1.26x slower                                             |
| genshi_text     | 20.9 ms                                                                | 27.9 ms: 1.33x slower                                             |
| mako            | 11.8 ms                                                                | 15.8 ms: 1.34x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.25 ms                                                                | 1.78 ms: 2.39x faster                                             |
| create_gc_cycles           | 1.86 ms                                                                | 1.42 ms: 1.30x faster                                             |
| async_tree_io_tg           | 630 ms                                                                 | 574 ms: 1.10x faster                                              |
| sqlite_synth               | 2.19 us                                                                | 2.00 us: 1.10x faster                                             |
| xml_etree_iterparse        | 91.1 ms                                                                | 87.0 ms: 1.05x faster                                             |
| async_tree_io              | 623 ms                                                                 | 602 ms: 1.04x faster                                              |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| regex_v8                   | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                             |
| pathlib                    | 18.7 ms                                                                | 19.2 ms: 1.03x slower                                             |
| regex_effbot               | 2.73 ms                                                                | 2.80 ms: 1.03x slower                                             |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 503 ms: 1.03x slower                                              |
| logging_silent             | 104 ns                                                                 | 108 ns: 1.04x slower                                              |
| mdp                        | 2.45 sec                                                               | 2.57 sec: 1.05x slower                                            |
| python_startup             | 14.7 ms                                                                | 15.5 ms: 1.05x slower                                             |
| json                       | 5.13 ms                                                                | 5.41 ms: 1.05x slower                                             |
| pidigits                   | 187 ms                                                                 | 199 ms: 1.07x slower                                              |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 534 ms: 1.07x slower                                              |
| async_tree_none            | 269 ms                                                                 | 287 ms: 1.07x slower                                              |
| float                      | 70.0 ms                                                                | 75.3 ms: 1.08x slower                                             |
| pycparser                  | 1.11 sec                                                               | 1.20 sec: 1.08x slower                                            |
| bench_mp_pool              | 88.5 ms                                                                | 95.6 ms: 1.08x slower                                             |
| regex_dna                  | 164 ms                                                                 | 178 ms: 1.08x slower                                              |
| coroutines                 | 21.4 ms                                                                | 23.3 ms: 1.09x slower                                             |
| json_loads                 | 28.6 us                                                                | 31.2 us: 1.09x slower                                             |
| async_tree_memoization     | 321 ms                                                                 | 352 ms: 1.10x slower                                              |
| docutils                   | 2.55 sec                                                               | 2.80 sec: 1.10x slower                                            |
| json_dumps                 | 11.5 ms                                                                | 12.7 ms: 1.10x slower                                             |
| dulwich_log                | 75.4 ms                                                                | 82.9 ms: 1.10x slower                                             |
| generators                 | 28.9 ms                                                                | 32.1 ms: 1.11x slower                                             |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.12x slower                                            |
| bpe_tokeniser              | 4.14 sec                                                               | 4.68 sec: 1.13x slower                                            |
| sphinx                     | 976 ms                                                                 | 1.11 sec: 1.13x slower                                            |
| async_generators           | 325 ms                                                                 | 370 ms: 1.14x slower                                              |
| pickle_pure_python         | 311 us                                                                 | 358 us: 1.15x slower                                              |
| unpickle_pure_python       | 212 us                                                                 | 245 us: 1.16x slower                                              |
| pprint_safe_repr           | 693 ms                                                                 | 804 ms: 1.16x slower                                              |
| pylint                     | 277 ms                                                                 | 322 ms: 1.16x slower                                              |
| subparsers                 | 22.2 ms                                                                | 25.9 ms: 1.17x slower                                             |
| many_optionals             | 1.02 ms                                                                | 1.19 ms: 1.17x slower                                             |
| spectral_norm              | 91.1 ms                                                                | 107 ms: 1.17x slower                                              |
| telco                      | 7.36 ms                                                                | 8.64 ms: 1.17x slower                                             |
| sqlglot_normalize          | 101 ms                                                                 | 120 ms: 1.18x slower                                              |
| xml_etree_generate         | 82.6 ms                                                                | 97.6 ms: 1.18x slower                                             |
| pprint_pformat             | 1.41 sec                                                               | 1.68 sec: 1.18x slower                                            |
| scimark_sor                | 112 ms                                                                 | 133 ms: 1.19x slower                                              |
| thrift                     | 741 us                                                                 | 884 us: 1.19x slower                                              |
| sqlglot_optimize           | 51.0 ms                                                                | 60.9 ms: 1.19x slower                                             |
| xml_etree_process          | 57.6 ms                                                                | 68.8 ms: 1.20x slower                                             |
| regex_compile              | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| 2to3                       | 252 ms                                                                 | 305 ms: 1.21x slower                                              |
| comprehensions             | 16.3 us                                                                | 19.8 us: 1.22x slower                                             |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| deepcopy                   | 252 us                                                                 | 307 us: 1.22x slower                                              |
| tomli_loads                | 1.90 sec                                                               | 2.33 sec: 1.22x slower                                            |
| go                         | 114 ms                                                                 | 140 ms: 1.22x slower                                              |
| sqlalchemy_declarative     | 127 ms                                                                 | 156 ms: 1.22x slower                                              |
| logging_simple             | 5.92 us                                                                | 7.26 us: 1.23x slower                                             |
| coverage                   | 78.8 ms                                                                | 97.1 ms: 1.23x slower                                             |
| sympy_expand               | 450 ms                                                                 | 555 ms: 1.23x slower                                              |
| pyflate                    | 410 ms                                                                 | 507 ms: 1.23x slower                                              |
| nqueens                    | 78.2 ms                                                                | 96.8 ms: 1.24x slower                                             |
| logging_format             | 6.63 us                                                                | 8.22 us: 1.24x slower                                             |
| connected_components       | 395 ms                                                                 | 492 ms: 1.25x slower                                              |
| sympy_integrate            | 19.6 ms                                                                | 24.5 ms: 1.25x slower                                             |
| sympy_sum                  | 151 ms                                                                 | 188 ms: 1.25x slower                                              |
| sqlglot_transpile          | 1.53 ms                                                                | 1.91 ms: 1.25x slower                                             |
| scimark_lu                 | 113 ms                                                                 | 142 ms: 1.25x slower                                              |
| deepcopy_reduce            | 2.60 us                                                                | 3.25 us: 1.25x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                             |
| scimark_fft                | 319 ms                                                                 | 399 ms: 1.25x slower                                              |
| shortest_path              | 431 ms                                                                 | 543 ms: 1.26x slower                                              |
| genshi_xml                 | 47.0 ms                                                                | 59.2 ms: 1.26x slower                                             |
| chaos                      | 55.6 ms                                                                | 70.3 ms: 1.26x slower                                             |
| hexiom                     | 5.87 ms                                                                | 7.42 ms: 1.26x slower                                             |
| raytrace                   | 256 ms                                                                 | 324 ms: 1.26x slower                                              |
| deepcopy_memo              | 29.8 us                                                                | 37.7 us: 1.27x slower                                             |
| sympy_str                  | 267 ms                                                                 | 338 ms: 1.27x slower                                              |
| sqlalchemy_imperative      | 19.0 ms                                                                | 24.3 ms: 1.28x slower                                             |
| typing_runtime_protocols   | 152 us                                                                 | 196 us: 1.29x slower                                              |
| sqlglot_parse              | 1.23 ms                                                                | 1.60 ms: 1.29x slower                                             |
| python_startup_no_site     | 7.47 ms                                                                | 9.69 ms: 1.30x slower                                             |
| genshi_text                | 20.9 ms                                                                | 27.9 ms: 1.33x slower                                             |
| fannkuch                   | 368 ms                                                                 | 493 ms: 1.34x slower                                              |
| mako                       | 11.8 ms                                                                | 15.8 ms: 1.34x slower                                             |
| meteor_contest             | 96.7 ms                                                                | 130 ms: 1.34x slower                                              |
| richards                   | 41.5 ms                                                                | 55.9 ms: 1.35x slower                                             |
| scimark_monte_carlo        | 62.8 ms                                                                | 85.1 ms: 1.36x slower                                             |
| richards_super             | 47.5 ms                                                                | 64.7 ms: 1.36x slower                                             |
| scimark_sparse_mat_mult    | 4.24 ms                                                                | 5.84 ms: 1.38x slower                                             |
| crypto_pyaes               | 65.6 ms                                                                | 90.5 ms: 1.38x slower                                             |
| nbody                      | 89.8 ms                                                                | 132 ms: 1.47x slower                                              |
| bench_thread_pool          | 1.03 ms                                                                | 3.33 ms: 3.24x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                      |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg
Ignored benchmarks (1) of results/bm-20250212-3.14.0a4+-9f143eb-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb.json: html5lib

- Geometric mean (including insignificant results): 1.133x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x