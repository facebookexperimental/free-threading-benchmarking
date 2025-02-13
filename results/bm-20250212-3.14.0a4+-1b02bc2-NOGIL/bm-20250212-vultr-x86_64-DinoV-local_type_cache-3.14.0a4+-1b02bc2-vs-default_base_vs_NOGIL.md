# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 1b02bc2
- commit date: 2025-02-12
- overall geometric mean: 1.134x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 304 ms: 1.21x slower                                              |
| docutils       | 2.55 sec                                                               | 2.83 sec: 1.11x slower                                            |
| sphinx         | 976 ms                                                                 | 1.11 sec: 1.14x slower                                            |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 630 ms                                                                 | 579 ms: 1.09x faster                                              |
| async_tree_io              | 623 ms                                                                 | 608 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 509 ms: 1.04x slower                                              |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 541 ms: 1.08x slower                                              |
| coroutines                 | 21.4 ms                                                                | 23.4 ms: 1.09x slower                                             |
| async_tree_memoization     | 321 ms                                                                 | 352 ms: 1.10x slower                                              |
| async_generators           | 325 ms                                                                 | 376 ms: 1.16x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                      |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 187 ms                                                                 | 203 ms: 1.09x slower                                              |
| float          | 70.0 ms                                                                | 76.4 ms: 1.09x slower                                             |
| nbody          | 89.8 ms                                                                | 131 ms: 1.46x slower                                              |
| Geometric mean | (ref)                                                                  | 1.20x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.73 ms                                                                | 2.74 ms: 1.00x slower                                             |
| regex_v8       | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                             |
| regex_dna      | 164 ms                                                                 | 180 ms: 1.10x slower                                              |
| regex_compile  | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.1 ms                                                                | 88.3 ms: 1.03x faster                                             |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                              |
| json_loads           | 28.6 us                                                                | 31.0 us: 1.08x slower                                             |
| json_dumps           | 11.5 ms                                                                | 12.8 ms: 1.11x slower                                             |
| unpickle_pure_python | 212 us                                                                 | 247 us: 1.16x slower                                              |
| xml_etree_generate   | 82.6 ms                                                                | 96.3 ms: 1.17x slower                                             |
| xml_etree_process    | 57.6 ms                                                                | 68.1 ms: 1.18x slower                                             |
| pickle_pure_python   | 311 us                                                                 | 372 us: 1.20x slower                                              |
| tomli_loads          | 1.90 sec                                                               | 2.36 sec: 1.24x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| python_startup_no_site | 7.47 ms                                                                | 9.63 ms: 1.29x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| genshi_xml      | 47.0 ms                                                                | 58.9 ms: 1.25x slower                                             |
| genshi_text     | 20.9 ms                                                                | 28.0 ms: 1.34x slower                                             |
| mako            | 11.8 ms                                                                | 15.8 ms: 1.34x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.25 ms                                                                | 1.75 ms: 2.43x faster                                             |
| create_gc_cycles           | 1.86 ms                                                                | 1.40 ms: 1.33x faster                                             |
| async_tree_io_tg           | 630 ms                                                                 | 579 ms: 1.09x faster                                              |
| sqlite_synth               | 2.19 us                                                                | 2.05 us: 1.07x faster                                             |
| xml_etree_iterparse        | 91.1 ms                                                                | 88.3 ms: 1.03x faster                                             |
| async_tree_io              | 623 ms                                                                 | 608 ms: 1.02x faster                                              |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                              |
| regex_effbot               | 2.73 ms                                                                | 2.74 ms: 1.00x slower                                             |
| regex_v8                   | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                             |
| pathlib                    | 18.7 ms                                                                | 19.1 ms: 1.02x slower                                             |
| async_tree_cpu_io_mixed_tg | 489 ms                                                                 | 509 ms: 1.04x slower                                              |
| python_startup             | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                             |
| logging_silent             | 104 ns                                                                 | 110 ns: 1.05x slower                                              |
| json                       | 5.13 ms                                                                | 5.41 ms: 1.05x slower                                             |
| pycparser                  | 1.11 sec                                                               | 1.19 sec: 1.06x slower                                            |
| bench_mp_pool              | 88.5 ms                                                                | 95.2 ms: 1.08x slower                                             |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.08x slower                                              |
| json_loads                 | 28.6 us                                                                | 31.0 us: 1.08x slower                                             |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 541 ms: 1.08x slower                                              |
| pidigits                   | 187 ms                                                                 | 203 ms: 1.09x slower                                              |
| coroutines                 | 21.4 ms                                                                | 23.4 ms: 1.09x slower                                             |
| float                      | 70.0 ms                                                                | 76.4 ms: 1.09x slower                                             |
| dulwich_log                | 75.4 ms                                                                | 82.4 ms: 1.09x slower                                             |
| generators                 | 28.9 ms                                                                | 31.7 ms: 1.10x slower                                             |
| async_tree_memoization     | 321 ms                                                                 | 352 ms: 1.10x slower                                              |
| regex_dna                  | 164 ms                                                                 | 180 ms: 1.10x slower                                              |
| json_dumps                 | 11.5 ms                                                                | 12.8 ms: 1.11x slower                                             |
| docutils                   | 2.55 sec                                                               | 2.83 sec: 1.11x slower                                            |
| mdp                        | 2.45 sec                                                               | 2.76 sec: 1.13x slower                                            |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                            |
| bpe_tokeniser              | 4.14 sec                                                               | 4.69 sec: 1.13x slower                                            |
| sphinx                     | 976 ms                                                                 | 1.11 sec: 1.14x slower                                            |
| pylint                     | 277 ms                                                                 | 317 ms: 1.15x slower                                              |
| telco                      | 7.36 ms                                                                | 8.45 ms: 1.15x slower                                             |
| many_optionals             | 1.02 ms                                                                | 1.17 ms: 1.15x slower                                             |
| async_generators           | 325 ms                                                                 | 376 ms: 1.16x slower                                              |
| spectral_norm              | 91.1 ms                                                                | 106 ms: 1.16x slower                                              |
| unpickle_pure_python       | 212 us                                                                 | 247 us: 1.16x slower                                              |
| xml_etree_generate         | 82.6 ms                                                                | 96.3 ms: 1.17x slower                                             |
| subparsers                 | 22.2 ms                                                                | 25.9 ms: 1.17x slower                                             |
| sqlglot_normalize          | 101 ms                                                                 | 119 ms: 1.17x slower                                              |
| pprint_safe_repr           | 693 ms                                                                 | 815 ms: 1.18x slower                                              |
| scimark_sor                | 112 ms                                                                 | 132 ms: 1.18x slower                                              |
| xml_etree_process          | 57.6 ms                                                                | 68.1 ms: 1.18x slower                                             |
| sqlglot_optimize           | 51.0 ms                                                                | 60.9 ms: 1.19x slower                                             |
| pprint_pformat             | 1.41 sec                                                               | 1.69 sec: 1.20x slower                                            |
| pickle_pure_python         | 311 us                                                                 | 372 us: 1.20x slower                                              |
| pyflate                    | 410 ms                                                                 | 493 ms: 1.20x slower                                              |
| regex_compile              | 126 ms                                                                 | 151 ms: 1.20x slower                                              |
| logging_simple             | 5.92 us                                                                | 7.15 us: 1.21x slower                                             |
| 2to3                       | 252 ms                                                                 | 304 ms: 1.21x slower                                              |
| scimark_lu                 | 113 ms                                                                 | 137 ms: 1.21x slower                                              |
| deepcopy                   | 252 us                                                                 | 305 us: 1.21x slower                                              |
| sympy_expand               | 450 ms                                                                 | 546 ms: 1.21x slower                                              |
| thrift                     | 741 us                                                                 | 901 us: 1.22x slower                                              |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| scimark_fft                | 319 ms                                                                 | 388 ms: 1.22x slower                                              |
| go                         | 114 ms                                                                 | 139 ms: 1.22x slower                                              |
| comprehensions             | 16.3 us                                                                | 19.9 us: 1.22x slower                                             |
| deepcopy_reduce            | 2.60 us                                                                | 3.18 us: 1.23x slower                                             |
| nqueens                    | 78.2 ms                                                                | 96.1 ms: 1.23x slower                                             |
| sympy_integrate            | 19.6 ms                                                                | 24.1 ms: 1.23x slower                                             |
| sqlalchemy_declarative     | 127 ms                                                                 | 157 ms: 1.23x slower                                              |
| sympy_sum                  | 151 ms                                                                 | 186 ms: 1.24x slower                                              |
| tomli_loads                | 1.90 sec                                                               | 2.36 sec: 1.24x slower                                            |
| coverage                   | 78.8 ms                                                                | 98.0 ms: 1.24x slower                                             |
| chaos                      | 55.6 ms                                                                | 69.3 ms: 1.25x slower                                             |
| logging_format             | 6.63 us                                                                | 8.28 us: 1.25x slower                                             |
| sqlglot_transpile          | 1.53 ms                                                                | 1.92 ms: 1.25x slower                                             |
| hexiom                     | 5.87 ms                                                                | 7.36 ms: 1.25x slower                                             |
| sympy_str                  | 267 ms                                                                 | 334 ms: 1.25x slower                                              |
| genshi_xml                 | 47.0 ms                                                                | 58.9 ms: 1.25x slower                                             |
| connected_components       | 395 ms                                                                 | 496 ms: 1.26x slower                                              |
| deepcopy_memo              | 29.8 us                                                                | 37.6 us: 1.26x slower                                             |
| shortest_path              | 431 ms                                                                 | 547 ms: 1.27x slower                                              |
| sqlalchemy_imperative      | 19.0 ms                                                                | 24.3 ms: 1.28x slower                                             |
| raytrace                   | 256 ms                                                                 | 328 ms: 1.28x slower                                              |
| sqlglot_parse              | 1.23 ms                                                                | 1.59 ms: 1.29x slower                                             |
| python_startup_no_site     | 7.47 ms                                                                | 9.63 ms: 1.29x slower                                             |
| typing_runtime_protocols   | 152 us                                                                 | 197 us: 1.30x slower                                              |
| scimark_monte_carlo        | 62.8 ms                                                                | 83.4 ms: 1.33x slower                                             |
| fannkuch                   | 368 ms                                                                 | 490 ms: 1.33x slower                                              |
| genshi_text                | 20.9 ms                                                                | 28.0 ms: 1.34x slower                                             |
| crypto_pyaes               | 65.6 ms                                                                | 87.8 ms: 1.34x slower                                             |
| mako                       | 11.8 ms                                                                | 15.8 ms: 1.34x slower                                             |
| meteor_contest             | 96.7 ms                                                                | 130 ms: 1.35x slower                                              |
| scimark_sparse_mat_mult    | 4.24 ms                                                                | 5.76 ms: 1.36x slower                                             |
| richards                   | 41.5 ms                                                                | 56.5 ms: 1.36x slower                                             |
| richards_super             | 47.5 ms                                                                | 65.3 ms: 1.37x slower                                             |
| nbody                      | 89.8 ms                                                                | 131 ms: 1.46x slower                                              |
| deltablue                  | 3.10 ms                                                                | 4.72 ms: 1.52x slower                                             |
| bench_thread_pool          | 1.03 ms                                                                | 3.32 ms: 3.24x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                      |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_none_tg, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20250212-3.14.0a4+-1b02bc2-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2.json: html5lib

- Geometric mean (including insignificant results): 1.134x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x