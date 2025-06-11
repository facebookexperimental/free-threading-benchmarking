# Results vs. base

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: linux-x86_64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.088x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                                                          | 281 ms: 1.13x slower                                                                                                  |
| docutils       | 2.51 sec                                                                                                        | 2.68 sec: 1.07x slower                                                                                                |
| html5lib       | 61.8 ms                                                                                                         | 66.5 ms: 1.08x slower                                                                                                 |
| sphinx         | 971 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 622 ms                                                                                                          | 523 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 225 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 549 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 467 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 308 ms                                                                                                          | 284 ms: 1.08x faster                                                                                                  |
| async_tree_none            | 269 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 508 ms                                                                                                          | 494 ms: 1.03x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 515 ms: 1.00x faster                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 311 ms: 1.01x slower                                                                                                  |
| coroutines                 | 23.3 ms                                                                                                         | 24.0 ms: 1.03x slower                                                                                                 |
| async_generators           | 330 ms                                                                                                          | 370 ms: 1.12x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                                                          | 182 ms: 1.09x faster                                                                                                  |
| float          | 72.2 ms                                                                                                         | 68.7 ms: 1.05x faster                                                                                                 |
| nbody          | 88.2 ms                                                                                                         | 119 ms: 1.35x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 20.4 ms: 1.06x faster                                                                                                 |
| regex_dna      | 172 ms                                                                                                          | 177 ms: 1.03x slower                                                                                                  |
| regex_effbot   | 2.58 ms                                                                                                         | 2.70 ms: 1.04x slower                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.9 ms                                                                                                         | 86.9 ms: 1.06x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 129 ms: 1.02x faster                                                                                                  |
| pickle_pure_python   | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 209 us                                                                                                          | 228 us: 1.09x slower                                                                                                  |
| json_loads           | 28.3 us                                                                                                         | 30.9 us: 1.09x slower                                                                                                 |
| tomli_loads          | 1.92 sec                                                                                                        | 2.14 sec: 1.12x slower                                                                                                |
| json_dumps           | 10.7 ms                                                                                                         | 12.1 ms: 1.12x slower                                                                                                 |
| xml_etree_generate   | 83.4 ms                                                                                                         | 95.2 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 58.9 ms                                                                                                         | 68.4 ms: 1.16x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.32 ms                                                                                                         | 9.56 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                                                                         | 39.4 ms: 1.16x slower                                                                                                 |
| genshi_xml      | 47.9 ms                                                                                                         | 58.7 ms: 1.22x slower                                                                                                 |
| genshi_text     | 20.6 ms                                                                                                         | 26.8 ms: 1.30x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.9 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json | results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.08 ms                                                                                                         | 1.90 ms: 2.15x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.47 ms: 1.32x faster                                                                                                 |
| async_tree_io_tg           | 622 ms                                                                                                          | 523 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 225 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 609 ms                                                                                                          | 549 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.24 us                                                                                                         | 2.03 us: 1.10x faster                                                                                                 |
| pidigits                   | 198 ms                                                                                                          | 182 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 467 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 308 ms                                                                                                          | 284 ms: 1.08x faster                                                                                                  |
| regex_v8                   | 21.7 ms                                                                                                         | 20.4 ms: 1.06x faster                                                                                                 |
| xml_etree_iterparse        | 91.9 ms                                                                                                         | 86.9 ms: 1.06x faster                                                                                                 |
| float                      | 72.2 ms                                                                                                         | 68.7 ms: 1.05x faster                                                                                                 |
| async_tree_none            | 269 ms                                                                                                          | 257 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 508 ms                                                                                                          | 494 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 132 ms                                                                                                          | 129 ms: 1.02x faster                                                                                                  |
| pathlib                    | 19.3 ms                                                                                                         | 19.2 ms: 1.01x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 515 ms: 1.00x faster                                                                                                  |
| async_tree_memoization     | 307 ms                                                                                                          | 311 ms: 1.01x slower                                                                                                  |
| json                       | 5.13 ms                                                                                                         | 5.24 ms: 1.02x slower                                                                                                 |
| regex_dna                  | 172 ms                                                                                                          | 177 ms: 1.03x slower                                                                                                  |
| coroutines                 | 23.3 ms                                                                                                         | 24.0 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.13 sec: 1.04x slower                                                                                                |
| regex_effbot               | 2.58 ms                                                                                                         | 2.70 ms: 1.04x slower                                                                                                 |
| bench_mp_pool              | 98.9 ms                                                                                                         | 104 ms: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.15 sec                                                                                                        | 4.39 sec: 1.06x slower                                                                                                |
| dulwich_log                | 66.6 ms                                                                                                         | 71.1 ms: 1.07x slower                                                                                                 |
| docutils                   | 2.51 sec                                                                                                        | 2.68 sec: 1.07x slower                                                                                                |
| html5lib                   | 61.8 ms                                                                                                         | 66.5 ms: 1.08x slower                                                                                                 |
| pickle_pure_python         | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| many_optionals             | 1.04 ms                                                                                                         | 1.13 ms: 1.09x slower                                                                                                 |
| deltablue                  | 3.31 ms                                                                                                         | 3.60 ms: 1.09x slower                                                                                                 |
| unpickle_pure_python       | 209 us                                                                                                          | 228 us: 1.09x slower                                                                                                  |
| sphinx                     | 971 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| json_loads                 | 28.3 us                                                                                                         | 30.9 us: 1.09x slower                                                                                                 |
| k_core                     | 2.04 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| scimark_fft                | 329 ms                                                                                                          | 363 ms: 1.10x slower                                                                                                  |
| pylint                     | 278 ms                                                                                                          | 307 ms: 1.10x slower                                                                                                  |
| scimark_sor                | 112 ms                                                                                                          | 125 ms: 1.11x slower                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                        | 2.14 sec: 1.12x slower                                                                                                |
| deepcopy_reduce            | 2.64 us                                                                                                         | 2.95 us: 1.12x slower                                                                                                 |
| hexiom                     | 5.67 ms                                                                                                         | 6.34 ms: 1.12x slower                                                                                                 |
| async_generators           | 330 ms                                                                                                          | 370 ms: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 768 ms                                                                                                          | 860 ms: 1.12x slower                                                                                                  |
| comprehensions             | 15.7 us                                                                                                         | 17.6 us: 1.12x slower                                                                                                 |
| chaos                      | 56.0 ms                                                                                                         | 62.8 ms: 1.12x slower                                                                                                 |
| logging_silent             | 469 ns                                                                                                          | 527 ns: 1.12x slower                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 12.1 ms: 1.12x slower                                                                                                 |
| nqueens                    | 76.0 ms                                                                                                         | 85.7 ms: 1.13x slower                                                                                                 |
| subparsers                 | 25.0 ms                                                                                                         | 28.3 ms: 1.13x slower                                                                                                 |
| 2to3                       | 248 ms                                                                                                          | 281 ms: 1.13x slower                                                                                                  |
| mdp                        | 1.16 sec                                                                                                        | 1.31 sec: 1.13x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.62 ms                                                                                                         | 5.24 ms: 1.13x slower                                                                                                 |
| deepcopy                   | 251 us                                                                                                          | 286 us: 1.14x slower                                                                                                  |
| xml_etree_generate         | 83.4 ms                                                                                                         | 95.2 ms: 1.14x slower                                                                                                 |
| go                         | 107 ms                                                                                                          | 122 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.6 ms                                                                                                         | 56.7 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.55 sec                                                                                                        | 1.78 sec: 1.14x slower                                                                                                |
| generators                 | 27.7 ms                                                                                                         | 31.7 ms: 1.15x slower                                                                                                 |
| spectral_norm              | 96.9 ms                                                                                                         | 111 ms: 1.15x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| scimark_lu                 | 110 ms                                                                                                          | 127 ms: 1.15x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.1 ms                                                                                                         | 113 ms: 1.15x slower                                                                                                  |
| django_template            | 34.1 ms                                                                                                         | 39.4 ms: 1.16x slower                                                                                                 |
| logging_simple             | 6.50 us                                                                                                         | 7.52 us: 1.16x slower                                                                                                 |
| raytrace                   | 254 ms                                                                                                          | 294 ms: 1.16x slower                                                                                                  |
| xml_etree_process          | 58.9 ms                                                                                                         | 68.4 ms: 1.16x slower                                                                                                 |
| sympy_expand               | 446 ms                                                                                                          | 520 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.7 ms                                                                                                         | 21.9 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 152 ms                                                                                                          | 179 ms: 1.17x slower                                                                                                  |
| sympy_str                  | 265 ms                                                                                                          | 311 ms: 1.17x slower                                                                                                  |
| telco                      | 7.21 ms                                                                                                         | 8.47 ms: 1.17x slower                                                                                                 |
| logging_format             | 7.30 us                                                                                                         | 8.58 us: 1.18x slower                                                                                                 |
| deepcopy_memo              | 29.2 us                                                                                                         | 34.4 us: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.78 ms: 1.18x slower                                                                                                 |
| pyflate                    | 405 ms                                                                                                          | 479 ms: 1.18x slower                                                                                                  |
| thrift                     | 736 us                                                                                                          | 877 us: 1.19x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.45 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 381 ms                                                                                                          | 462 ms: 1.21x slower                                                                                                  |
| connected_components       | 401 ms                                                                                                          | 490 ms: 1.22x slower                                                                                                  |
| genshi_xml                 | 47.9 ms                                                                                                         | 58.7 ms: 1.22x slower                                                                                                 |
| shortest_path              | 439 ms                                                                                                          | 539 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 151 us                                                                                                          | 186 us: 1.23x slower                                                                                                  |
| meteor_contest             | 99.7 ms                                                                                                         | 123 ms: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 62.2 ms                                                                                                         | 77.0 ms: 1.24x slower                                                                                                 |
| richards                   | 41.3 ms                                                                                                         | 52.0 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.7 ms                                                                                                         | 59.7 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 67.1 ms                                                                                                         | 86.0 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.6 ms                                                                                                         | 26.8 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.32 ms                                                                                                         | 9.56 ms: 1.31x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.9 ms: 1.34x slower                                                                                                 |
| nbody                      | 88.2 ms                                                                                                         | 119 ms: 1.35x slower                                                                                                  |
| coverage                   | 81.3 ms                                                                                                         | 110 ms: 1.35x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.10 ms: 2.97x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.088x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.22x