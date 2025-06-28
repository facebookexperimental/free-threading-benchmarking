# Results vs. base

- fork: python
- ref: c419af9e277bea7dd78f
- machine: linux-x86_64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| docutils       | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib       | 61.4 ms                                                                                                         | 65.4 ms: 1.07x slower                                                                                                 |
| sphinx         | 961 ms                                                                                                          | 1.03 sec: 1.07x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                                                          | 519 ms: 1.21x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 225 ms: 1.12x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 517 ms                                                                                                          | 462 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 613 ms                                                                                                          | 547 ms: 1.12x faster                                                                                                  |
| async_tree_memoization_tg  | 309 ms                                                                                                          | 282 ms: 1.10x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 519 ms                                                                                                          | 487 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 270 ms                                                                                                          | 257 ms: 1.05x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 23.7 ms: 1.01x slower                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 368 ms: 1.08x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.1 ms                                                                                                         | 69.7 ms: 1.03x faster                                                                                                 |
| pidigits       | 196 ms                                                                                                          | 190 ms: 1.03x faster                                                                                                  |
| nbody          | 89.6 ms                                                                                                         | 123 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 20.1 ms: 1.08x faster                                                                                                 |
| regex_dna      | 172 ms                                                                                                          | 163 ms: 1.06x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.3 ms                                                                                                         | 86.6 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 130 ms                                                                                                          | 129 ms: 1.01x faster                                                                                                  |
| pickle_pure_python   | 307 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| json_dumps           | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python | 207 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| tomli_loads          | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| json_loads           | 27.8 us                                                                                                         | 31.3 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 83.2 ms                                                                                                         | 95.0 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 58.1 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.34 ms                                                                                                         | 9.58 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.4 ms                                                                                                         | 39.3 ms: 1.14x slower                                                                                                 |
| genshi_xml      | 47.8 ms                                                                                                         | 58.2 ms: 1.22x slower                                                                                                 |
| genshi_text     | 20.7 ms                                                                                                         | 26.5 ms: 1.28x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 16.0 ms: 1.35x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json | results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.51 ms                                                                                                         | 1.92 ms: 2.36x faster                                                                                                 |
| create_gc_cycles           | 1.92 ms                                                                                                         | 1.48 ms: 1.30x faster                                                                                                 |
| async_tree_io_tg           | 628 ms                                                                                                          | 519 ms: 1.21x faster                                                                                                  |
| sqlite_synth               | 2.31 us                                                                                                         | 2.05 us: 1.12x faster                                                                                                 |
| async_tree_none_tg         | 253 ms                                                                                                          | 225 ms: 1.12x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 517 ms                                                                                                          | 462 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 613 ms                                                                                                          | 547 ms: 1.12x faster                                                                                                  |
| async_tree_memoization_tg  | 309 ms                                                                                                          | 282 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.7 ms                                                                                                         | 20.1 ms: 1.08x faster                                                                                                 |
| xml_etree_iterparse        | 92.3 ms                                                                                                         | 86.6 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 519 ms                                                                                                          | 487 ms: 1.06x faster                                                                                                  |
| regex_dna                  | 172 ms                                                                                                          | 163 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 270 ms                                                                                                          | 257 ms: 1.05x faster                                                                                                  |
| float                      | 72.1 ms                                                                                                         | 69.7 ms: 1.03x faster                                                                                                 |
| pidigits                   | 196 ms                                                                                                          | 190 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 130 ms                                                                                                          | 129 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| pathlib                    | 19.5 ms                                                                                                         | 19.3 ms: 1.01x faster                                                                                                 |
| coroutines                 | 23.4 ms                                                                                                         | 23.7 ms: 1.01x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.13 sec: 1.04x slower                                                                                                |
| bpe_tokeniser              | 4.17 sec                                                                                                        | 4.36 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 98.8 ms                                                                                                         | 104 ms: 1.06x slower                                                                                                  |
| generators                 | 27.7 ms                                                                                                         | 29.5 ms: 1.07x slower                                                                                                 |
| html5lib                   | 61.4 ms                                                                                                         | 65.4 ms: 1.07x slower                                                                                                 |
| json                       | 5.01 ms                                                                                                         | 5.35 ms: 1.07x slower                                                                                                 |
| sphinx                     | 961 ms                                                                                                          | 1.03 sec: 1.07x slower                                                                                                |
| docutils                   | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.89 ms                                                                                                         | 5.25 ms: 1.07x slower                                                                                                 |
| dulwich_log                | 66.4 ms                                                                                                         | 71.6 ms: 1.08x slower                                                                                                 |
| async_generators           | 339 ms                                                                                                          | 368 ms: 1.08x slower                                                                                                  |
| deltablue                  | 3.21 ms                                                                                                         | 3.50 ms: 1.09x slower                                                                                                 |
| pickle_pure_python         | 307 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| many_optionals             | 1.04 ms                                                                                                         | 1.13 ms: 1.09x slower                                                                                                 |
| logging_silent             | 93.6 ns                                                                                                         | 103 ns: 1.10x slower                                                                                                  |
| scimark_fft                | 332 ms                                                                                                          | 366 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| pylint                     | 278 ms                                                                                                          | 308 ms: 1.11x slower                                                                                                  |
| subparsers                 | 25.2 ms                                                                                                         | 28.1 ms: 1.11x slower                                                                                                 |
| chaos                      | 56.6 ms                                                                                                         | 63.1 ms: 1.11x slower                                                                                                 |
| json_dumps                 | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 17.4 us: 1.12x slower                                                                                                 |
| hexiom                     | 5.66 ms                                                                                                         | 6.34 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 207 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 691 ms                                                                                                          | 778 ms: 1.13x slower                                                                                                  |
| tomli_loads                | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| json_loads                 | 27.8 us                                                                                                         | 31.3 us: 1.13x slower                                                                                                 |
| sympy_expand               | 457 ms                                                                                                          | 517 ms: 1.13x slower                                                                                                  |
| 2to3                       | 250 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| nqueens                    | 76.4 ms                                                                                                         | 86.7 ms: 1.13x slower                                                                                                 |
| django_template            | 34.4 ms                                                                                                         | 39.3 ms: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.41 sec                                                                                                        | 1.61 sec: 1.14x slower                                                                                                |
| xml_etree_generate         | 83.2 ms                                                                                                         | 95.0 ms: 1.14x slower                                                                                                 |
| deepcopy_reduce            | 2.65 us                                                                                                         | 3.04 us: 1.14x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| sqlglot_v2_optimize        | 49.6 ms                                                                                                         | 57.0 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.6 ms                                                                                                         | 114 ms: 1.15x slower                                                                                                  |
| scimark_sor                | 107 ms                                                                                                          | 124 ms: 1.15x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.15x slower                                                                                                  |
| sympy_str                  | 268 ms                                                                                                          | 310 ms: 1.16x slower                                                                                                  |
| pyflate                    | 398 ms                                                                                                          | 461 ms: 1.16x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| scimark_lu                 | 110 ms                                                                                                          | 128 ms: 1.17x slower                                                                                                  |
| sympy_integrate            | 18.7 ms                                                                                                         | 21.8 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 152 ms                                                                                                          | 178 ms: 1.17x slower                                                                                                  |
| deepcopy                   | 251 us                                                                                                          | 295 us: 1.17x slower                                                                                                  |
| spectral_norm              | 97.3 ms                                                                                                         | 115 ms: 1.18x slower                                                                                                  |
| telco                      | 7.16 ms                                                                                                         | 8.45 ms: 1.18x slower                                                                                                 |
| xml_etree_process          | 58.1 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| logging_format             | 6.65 us                                                                                                         | 7.89 us: 1.19x slower                                                                                                 |
| logging_simple             | 5.88 us                                                                                                         | 6.98 us: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.79 ms: 1.19x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 302 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 99.4 ms                                                                                                         | 119 ms: 1.20x slower                                                                                                  |
| thrift                     | 728 us                                                                                                          | 874 us: 1.20x slower                                                                                                  |
| deepcopy_memo              | 29.0 us                                                                                                         | 34.8 us: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.45 ms: 1.21x slower                                                                                                 |
| shortest_path              | 442 ms                                                                                                          | 537 ms: 1.22x slower                                                                                                  |
| genshi_xml                 | 47.8 ms                                                                                                         | 58.2 ms: 1.22x slower                                                                                                 |
| fannkuch                   | 378 ms                                                                                                          | 464 ms: 1.23x slower                                                                                                  |
| connected_components       | 398 ms                                                                                                          | 490 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 153 us                                                                                                          | 189 us: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 61.5 ms                                                                                                         | 76.9 ms: 1.25x slower                                                                                                 |
| richards                   | 40.6 ms                                                                                                         | 51.5 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.7 ms                                                                                                         | 26.5 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 68.2 ms                                                                                                         | 87.7 ms: 1.29x slower                                                                                                 |
| richards_super             | 46.3 ms                                                                                                         | 59.6 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 7.34 ms                                                                                                         | 9.58 ms: 1.31x slower                                                                                                 |
| mako                       | 11.9 ms                                                                                                         | 16.0 ms: 1.35x slower                                                                                                 |
| coverage                   | 81.1 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| nbody                      | 89.6 ms                                                                                                         | 123 ms: 1.38x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.15 ms: 3.02x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): regex_effbot, async_tree_memoization

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x