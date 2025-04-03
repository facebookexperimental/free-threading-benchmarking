# Results vs. base

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 311 ms                                                                 | 289 ms: 1.07x faster                                                  |
| docutils       | 2.88 sec                                                               | 2.77 sec: 1.04x faster                                                |
| html5lib       | 74.0 ms                                                                | 70.6 ms: 1.05x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.10 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 27.0 ms                                                                | 23.1 ms: 1.17x faster                                                 |
| async_tree_memoization_tg  | 314 ms                                                                 | 292 ms: 1.08x faster                                                  |
| async_tree_io_tg           | 575 ms                                                                 | 535 ms: 1.07x faster                                                  |
| async_tree_none_tg         | 248 ms                                                                 | 232 ms: 1.07x faster                                                  |
| async_generators           | 391 ms                                                                 | 365 ms: 1.07x faster                                                  |
| async_tree_io              | 603 ms                                                                 | 564 ms: 1.07x faster                                                  |
| async_tree_memoization     | 344 ms                                                                 | 322 ms: 1.07x faster                                                  |
| async_tree_none            | 284 ms                                                                 | 268 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 482 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 526 ms                                                                 | 511 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 113 ms: 1.20x faster                                                  |
| float          | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| pidigits       | 192 ms                                                                 | 195 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 171 ms                                                                 | 152 ms: 1.12x faster                                                  |
| regex_dna      | 176 ms                                                                 | 182 ms: 1.03x slower                                                  |
| regex_effbot   | 2.73 ms                                                                | 2.83 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.23 sec: 1.14x faster                                                |
| unpickle_pure_python | 268 us                                                                 | 240 us: 1.12x faster                                                  |
| pickle_pure_python   | 381 us                                                                 | 343 us: 1.11x faster                                                  |
| xml_etree_process    | 74.1 ms                                                                | 69.3 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 92.9 ms                                                                | 87.3 ms: 1.06x faster                                                 |
| xml_etree_generate   | 101 ms                                                                 | 95.5 ms: 1.06x faster                                                 |
| json_dumps           | 13.3 ms                                                                | 12.8 ms: 1.03x faster                                                 |
| json_loads           | 29.2 us                                                                | 30.7 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                                | 26.5 ms: 1.20x faster                                                 |
| genshi_xml      | 68.6 ms                                                                | 57.6 ms: 1.19x faster                                                 |
| django_template | 44.5 ms                                                                | 40.8 ms: 1.09x faster                                                 |
| mako            | 16.4 ms                                                                | 15.5 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.13x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 43.8 ms                                                                | 32.1 ms: 1.37x faster                                                 |
| deltablue                  | 4.48 ms                                                                | 3.72 ms: 1.21x faster                                                 |
| scimark_sor                | 151 ms                                                                 | 126 ms: 1.20x faster                                                  |
| genshi_text                | 31.7 ms                                                                | 26.5 ms: 1.20x faster                                                 |
| nbody                      | 136 ms                                                                 | 113 ms: 1.20x faster                                                  |
| genshi_xml                 | 68.6 ms                                                                | 57.6 ms: 1.19x faster                                                 |
| logging_format             | 9.68 us                                                                | 8.16 us: 1.19x faster                                                 |
| logging_simple             | 8.45 us                                                                | 7.18 us: 1.18x faster                                                 |
| coroutines                 | 27.0 ms                                                                | 23.1 ms: 1.17x faster                                                 |
| scimark_monte_carlo        | 87.1 ms                                                                | 75.6 ms: 1.15x faster                                                 |
| go                         | 153 ms                                                                 | 133 ms: 1.15x faster                                                  |
| hexiom                     | 8.14 ms                                                                | 7.11 ms: 1.14x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.23 sec: 1.14x faster                                                |
| spectral_norm              | 120 ms                                                                 | 106 ms: 1.13x faster                                                  |
| chaos                      | 72.0 ms                                                                | 63.9 ms: 1.13x faster                                                 |
| nqueens                    | 102 ms                                                                 | 90.4 ms: 1.12x faster                                                 |
| fannkuch                   | 519 ms                                                                 | 461 ms: 1.12x faster                                                  |
| pyflate                    | 529 ms                                                                 | 471 ms: 1.12x faster                                                  |
| regex_compile              | 171 ms                                                                 | 152 ms: 1.12x faster                                                  |
| raytrace                   | 338 ms                                                                 | 302 ms: 1.12x faster                                                  |
| richards                   | 60.1 ms                                                                | 53.7 ms: 1.12x faster                                                 |
| logging_silent             | 125 ns                                                                 | 112 ns: 1.12x faster                                                  |
| unpickle_pure_python       | 268 us                                                                 | 240 us: 1.12x faster                                                  |
| pickle_pure_python         | 381 us                                                                 | 343 us: 1.11x faster                                                  |
| sqlglot_v2_parse           | 1.68 ms                                                                | 1.52 ms: 1.11x faster                                                 |
| scimark_fft                | 383 ms                                                                 | 347 ms: 1.11x faster                                                  |
| richards_super             | 67.9 ms                                                                | 61.5 ms: 1.10x faster                                                 |
| sqlglot_v2_transpile       | 2.03 ms                                                                | 1.84 ms: 1.10x faster                                                 |
| deepcopy                   | 328 us                                                                 | 298 us: 1.10x faster                                                  |
| scimark_sparse_mat_mult    | 5.52 ms                                                                | 5.01 ms: 1.10x faster                                                 |
| sqlglot_v2_normalize       | 130 ms                                                                 | 119 ms: 1.10x faster                                                  |
| deepcopy_memo              | 40.2 us                                                                | 36.6 us: 1.10x faster                                                 |
| comprehensions             | 22.1 us                                                                | 20.2 us: 1.10x faster                                                 |
| float                      | 76.7 ms                                                                | 70.0 ms: 1.10x faster                                                 |
| pprint_pformat             | 1.84 sec                                                               | 1.68 sec: 1.09x faster                                                |
| deepcopy_reduce            | 3.31 us                                                                | 3.04 us: 1.09x faster                                                 |
| django_template            | 44.5 ms                                                                | 40.8 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 873 ms                                                                 | 802 ms: 1.09x faster                                                  |
| sqlglot_v2_optimize        | 65.4 ms                                                                | 60.1 ms: 1.09x faster                                                 |
| mdp                        | 1.46 sec                                                               | 1.35 sec: 1.09x faster                                                |
| sympy_expand               | 589 ms                                                                 | 544 ms: 1.08x faster                                                  |
| sympy_str                  | 357 ms                                                                 | 331 ms: 1.08x faster                                                  |
| scimark_lu                 | 142 ms                                                                 | 132 ms: 1.08x faster                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 292 ms: 1.08x faster                                                  |
| 2to3                       | 311 ms                                                                 | 289 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 575 ms                                                                 | 535 ms: 1.07x faster                                                  |
| async_tree_none_tg         | 248 ms                                                                 | 232 ms: 1.07x faster                                                  |
| async_generators           | 391 ms                                                                 | 365 ms: 1.07x faster                                                  |
| crypto_pyaes               | 91.9 ms                                                                | 85.8 ms: 1.07x faster                                                 |
| async_tree_io              | 603 ms                                                                 | 564 ms: 1.07x faster                                                  |
| xml_etree_process          | 74.1 ms                                                                | 69.3 ms: 1.07x faster                                                 |
| dulwich_log                | 78.5 ms                                                                | 73.5 ms: 1.07x faster                                                 |
| async_tree_memoization     | 344 ms                                                                 | 322 ms: 1.07x faster                                                  |
| subparsers                 | 27.4 ms                                                                | 25.7 ms: 1.07x faster                                                 |
| many_optionals             | 1.23 ms                                                                | 1.15 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 92.9 ms                                                                | 87.3 ms: 1.06x faster                                                 |
| async_tree_none            | 284 ms                                                                 | 268 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.87 sec                                                               | 4.58 sec: 1.06x faster                                                |
| xml_etree_generate         | 101 ms                                                                 | 95.5 ms: 1.06x faster                                                 |
| mako                       | 16.4 ms                                                                | 15.5 ms: 1.06x faster                                                 |
| sympy_integrate            | 24.4 ms                                                                | 23.1 ms: 1.06x faster                                                 |
| pycparser                  | 1.24 sec                                                               | 1.17 sec: 1.06x faster                                                |
| sympy_sum                  | 196 ms                                                                 | 186 ms: 1.06x faster                                                  |
| pylint                     | 333 ms                                                                 | 315 ms: 1.05x faster                                                  |
| sphinx                     | 1.15 sec                                                               | 1.10 sec: 1.05x faster                                                |
| typing_runtime_protocols   | 206 us                                                                 | 197 us: 1.05x faster                                                  |
| html5lib                   | 74.0 ms                                                                | 70.6 ms: 1.05x faster                                                 |
| sqlalchemy_declarative     | 165 ms                                                                 | 158 ms: 1.05x faster                                                  |
| sqlalchemy_imperative      | 25.3 ms                                                                | 24.2 ms: 1.05x faster                                                 |
| connected_components       | 511 ms                                                                 | 489 ms: 1.04x faster                                                  |
| docutils                   | 2.88 sec                                                               | 2.77 sec: 1.04x faster                                                |
| meteor_contest             | 133 ms                                                                 | 129 ms: 1.04x faster                                                  |
| json_dumps                 | 13.3 ms                                                                | 12.8 ms: 1.03x faster                                                 |
| shortest_path              | 554 ms                                                                 | 536 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 482 ms: 1.03x faster                                                  |
| telco                      | 8.84 ms                                                                | 8.58 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 526 ms                                                                 | 511 ms: 1.03x faster                                                  |
| pathlib                    | 19.7 ms                                                                | 19.2 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.38 ms                                                                | 1.35 ms: 1.02x faster                                                 |
| k_core                     | 2.30 sec                                                               | 2.26 sec: 1.02x faster                                                |
| gc_traversal               | 1.81 ms                                                                | 1.78 ms: 1.02x faster                                                 |
| bench_mp_pool              | 97.5 ms                                                                | 96.2 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.18 ms                                                                | 3.15 ms: 1.01x faster                                                 |
| python_startup             | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| coverage                   | 111 ms                                                                 | 113 ms: 1.02x slower                                                  |
| pidigits                   | 192 ms                                                                 | 195 ms: 1.02x slower                                                  |
| json                       | 5.09 ms                                                                | 5.25 ms: 1.03x slower                                                 |
| regex_dna                  | 176 ms                                                                 | 182 ms: 1.03x slower                                                  |
| regex_effbot               | 2.73 ms                                                                | 2.83 ms: 1.04x slower                                                 |
| json_loads                 | 29.2 us                                                                | 30.7 us: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (4): sqlite_synth, xml_etree_parse, asyncio_websockets, regex_v8

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.00x