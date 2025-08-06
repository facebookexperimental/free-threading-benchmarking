# Results vs. base

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: linux-x86_64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| docutils       | 2.56 sec                                                                                                        | 2.71 sec: 1.06x slower                                                                                                |
| html5lib       | 61.1 ms                                                                                                         | 68.3 ms: 1.12x slower                                                                                                 |
| sphinx         | 979 ms                                                                                                          | 1.05 sec: 1.07x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 610 ms                                                                                                          | 520 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 229 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 601 ms                                                                                                          | 542 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 285 ms: 1.10x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 474 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 508 ms                                                                                                          | 497 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 309 ms: 1.01x slower                                                                                                  |
| coroutines                 | 23.0 ms                                                                                                         | 24.5 ms: 1.06x slower                                                                                                 |
| async_generators           | 335 ms                                                                                                          | 374 ms: 1.12x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 71.1 ms                                                                                                         | 69.8 ms: 1.02x faster                                                                                                 |
| pidigits       | 202 ms                                                                                                          | 202 ms: 1.00x faster                                                                                                  |
| nbody          | 88.8 ms                                                                                                         | 124 ms: 1.39x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                                                         | 20.9 ms: 1.05x faster                                                                                                 |
| regex_dna      | 174 ms                                                                                                          | 179 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 2.70 ms                                                                                                         | 2.92 ms: 1.08x slower                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 131 ms: 1.02x faster                                                                                                  |
| json_loads           | 28.8 us                                                                                                         | 31.2 us: 1.09x slower                                                                                                 |
| pickle_pure_python   | 313 us                                                                                                          | 346 us: 1.11x slower                                                                                                  |
| json_dumps           | 10.8 ms                                                                                                         | 12.0 ms: 1.11x slower                                                                                                 |
| unpickle_pure_python | 209 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| tomli_loads          | 1.92 sec                                                                                                        | 2.17 sec: 1.13x slower                                                                                                |
| xml_etree_generate   | 83.7 ms                                                                                                         | 96.6 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 58.3 ms                                                                                                         | 70.1 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.25 ms                                                                                                         | 9.52 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                                                                         | 40.5 ms: 1.17x slower                                                                                                 |
| genshi_xml      | 48.6 ms                                                                                                         | 57.1 ms: 1.17x slower                                                                                                 |
| genshi_text     | 20.4 ms                                                                                                         | 26.8 ms: 1.31x slower                                                                                                 |
| mako            | 11.6 ms                                                                                                         | 16.0 ms: 1.39x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.26x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json | results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.35 ms                                                                                                         | 1.94 ms: 2.25x faster                                                                                                 |
| create_gc_cycles           | 1.94 ms                                                                                                         | 1.52 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 610 ms                                                                                                          | 520 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 257 ms                                                                                                          | 229 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 601 ms                                                                                                          | 542 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.27 us                                                                                                         | 2.05 us: 1.11x faster                                                                                                 |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 285 ms: 1.10x faster                                                                                                  |
| xml_etree_iterparse        | 93.0 ms                                                                                                         | 87.1 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 505 ms                                                                                                          | 474 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 22.0 ms                                                                                                         | 20.9 ms: 1.05x faster                                                                                                 |
| async_tree_none            | 266 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 134 ms                                                                                                          | 131 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 508 ms                                                                                                          | 497 ms: 1.02x faster                                                                                                  |
| float                      | 71.1 ms                                                                                                         | 69.8 ms: 1.02x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| pidigits                   | 202 ms                                                                                                          | 202 ms: 1.00x faster                                                                                                  |
| pathlib                    | 18.9 ms                                                                                                         | 19.0 ms: 1.01x slower                                                                                                 |
| async_tree_memoization     | 307 ms                                                                                                          | 309 ms: 1.01x slower                                                                                                  |
| json                       | 5.24 ms                                                                                                         | 5.36 ms: 1.02x slower                                                                                                 |
| regex_dna                  | 174 ms                                                                                                          | 179 ms: 1.03x slower                                                                                                  |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 109 ms: 1.06x slower                                                                                                  |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.42 sec: 1.06x slower                                                                                                |
| docutils                   | 2.56 sec                                                                                                        | 2.71 sec: 1.06x slower                                                                                                |
| coroutines                 | 23.0 ms                                                                                                         | 24.5 ms: 1.06x slower                                                                                                 |
| sphinx                     | 979 ms                                                                                                          | 1.05 sec: 1.07x slower                                                                                                |
| dulwich_log                | 66.4 ms                                                                                                         | 71.5 ms: 1.08x slower                                                                                                 |
| generators                 | 28.3 ms                                                                                                         | 30.5 ms: 1.08x slower                                                                                                 |
| regex_effbot               | 2.70 ms                                                                                                         | 2.92 ms: 1.08x slower                                                                                                 |
| json_loads                 | 28.8 us                                                                                                         | 31.2 us: 1.09x slower                                                                                                 |
| pylint                     | 282 ms                                                                                                          | 308 ms: 1.09x slower                                                                                                  |
| k_core                     | 2.04 sec                                                                                                        | 2.25 sec: 1.10x slower                                                                                                |
| pickle_pure_python         | 313 us                                                                                                          | 346 us: 1.11x slower                                                                                                  |
| logging_silent             | 95.9 ns                                                                                                         | 106 ns: 1.11x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 177 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 333 ms                                                                                                          | 369 ms: 1.11x slower                                                                                                  |
| many_optionals             | 1.21 ms                                                                                                         | 1.35 ms: 1.11x slower                                                                                                 |
| json_dumps                 | 10.8 ms                                                                                                         | 12.0 ms: 1.11x slower                                                                                                 |
| deltablue                  | 3.30 ms                                                                                                         | 3.68 ms: 1.12x slower                                                                                                 |
| async_generators           | 335 ms                                                                                                          | 374 ms: 1.12x slower                                                                                                  |
| html5lib                   | 61.1 ms                                                                                                         | 68.3 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 209 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| nqueens                    | 78.2 ms                                                                                                         | 87.5 ms: 1.12x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 17.7 us: 1.13x slower                                                                                                 |
| pprint_safe_repr           | 704 ms                                                                                                          | 797 ms: 1.13x slower                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                        | 2.17 sec: 1.13x slower                                                                                                |
| 2to3                       | 250 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| chaos                      | 55.7 ms                                                                                                         | 63.6 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| deepcopy_memo              | 30.8 us                                                                                                         | 35.2 us: 1.14x slower                                                                                                 |
| hexiom                     | 5.67 ms                                                                                                         | 6.49 ms: 1.14x slower                                                                                                 |
| pyflate                    | 402 ms                                                                                                          | 461 ms: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.43 sec                                                                                                        | 1.65 sec: 1.15x slower                                                                                                |
| mdp                        | 1.16 sec                                                                                                        | 1.33 sec: 1.15x slower                                                                                                |
| sympy_expand               | 458 ms                                                                                                          | 527 ms: 1.15x slower                                                                                                  |
| scimark_sor                | 108 ms                                                                                                          | 125 ms: 1.15x slower                                                                                                  |
| xml_etree_generate         | 83.7 ms                                                                                                         | 96.6 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.4 ms                                                                                                         | 58.2 ms: 1.16x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 121 ms: 1.16x slower                                                                                                  |
| deepcopy_reduce            | 2.68 us                                                                                                         | 3.10 us: 1.16x slower                                                                                                 |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| subparsers                 | 42.7 ms                                                                                                         | 49.6 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 257 us                                                                                                          | 300 us: 1.16x slower                                                                                                  |
| sympy_str                  | 271 ms                                                                                                          | 316 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 19.0 ms                                                                                                         | 22.2 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 155 ms                                                                                                          | 181 ms: 1.17x slower                                                                                                  |
| django_template            | 34.7 ms                                                                                                         | 40.5 ms: 1.17x slower                                                                                                 |
| thrift                     | 759 us                                                                                                          | 888 us: 1.17x slower                                                                                                  |
| spectral_norm              | 97.2 ms                                                                                                         | 114 ms: 1.17x slower                                                                                                  |
| genshi_xml                 | 48.6 ms                                                                                                         | 57.1 ms: 1.17x slower                                                                                                 |
| scimark_lu                 | 111 ms                                                                                                          | 131 ms: 1.18x slower                                                                                                  |
| fannkuch                   | 380 ms                                                                                                          | 452 ms: 1.19x slower                                                                                                  |
| meteor_contest             | 99.9 ms                                                                                                         | 119 ms: 1.19x slower                                                                                                  |
| logging_simple             | 5.83 us                                                                                                         | 6.99 us: 1.20x slower                                                                                                 |
| xml_etree_process          | 58.3 ms                                                                                                         | 70.1 ms: 1.20x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.79 ms                                                                                                         | 5.77 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.52 ms                                                                                                         | 1.85 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.49 ms: 1.21x slower                                                                                                 |
| connected_components       | 402 ms                                                                                                          | 490 ms: 1.22x slower                                                                                                  |
| raytrace                   | 249 ms                                                                                                          | 304 ms: 1.22x slower                                                                                                  |
| logging_format             | 6.46 us                                                                                                         | 7.89 us: 1.22x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 541 ms: 1.22x slower                                                                                                  |
| typing_runtime_protocols   | 153 us                                                                                                          | 187 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 62.9 ms                                                                                                         | 77.9 ms: 1.24x slower                                                                                                 |
| richards                   | 41.4 ms                                                                                                         | 51.3 ms: 1.24x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| richards_super             | 47.2 ms                                                                                                         | 59.1 ms: 1.25x slower                                                                                                 |
| crypto_pyaes               | 68.7 ms                                                                                                         | 86.1 ms: 1.25x slower                                                                                                 |
| genshi_text                | 20.4 ms                                                                                                         | 26.8 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 7.25 ms                                                                                                         | 9.52 ms: 1.31x slower                                                                                                 |
| coverage                   | 82.0 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| mako                       | 11.6 ms                                                                                                         | 16.0 ms: 1.39x slower                                                                                                 |
| nbody                      | 88.8 ms                                                                                                         | 124 ms: 1.39x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.15 ms: 3.01x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x