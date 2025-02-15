# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: c00cd86
- commit date: 2025-02-14
- overall geometric mean: 1.126x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 304 ms: 1.19x slower                                           |
| docutils       | 2.55 sec                                                               | 2.79 sec: 1.10x slower                                         |
| sphinx         | 979 ms                                                                 | 1.10 sec: 1.12x slower                                         |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 622 ms                                                                 | 577 ms: 1.08x faster                                           |
| async_tree_cpu_io_mixed_tg | 519 ms                                                                 | 507 ms: 1.02x faster                                           |
| async_tree_io              | 623 ms                                                                 | 612 ms: 1.02x faster                                           |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 537 ms: 1.01x slower                                           |
| coroutines                 | 22.4 ms                                                                | 24.2 ms: 1.08x slower                                          |
| async_tree_none            | 269 ms                                                                 | 292 ms: 1.08x slower                                           |
| async_tree_memoization     | 324 ms                                                                 | 354 ms: 1.09x slower                                           |
| async_generators           | 325 ms                                                                 | 374 ms: 1.15x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                   |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 199 ms: 1.00x faster                                           |
| float          | 72.2 ms                                                                | 76.2 ms: 1.06x slower                                          |
| nbody          | 87.7 ms                                                                | 130 ms: 1.48x slower                                           |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 2.71 ms                                                                | 2.83 ms: 1.05x slower                                          |
| regex_v8       | 24.0 ms                                                                | 25.1 ms: 1.05x slower                                          |
| regex_dna      | 171 ms                                                                 | 182 ms: 1.06x slower                                           |
| regex_compile  | 127 ms                                                                 | 152 ms: 1.19x slower                                           |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 90.9 ms                                                                | 88.7 ms: 1.03x faster                                          |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                           |
| json_loads           | 28.7 us                                                                | 31.6 us: 1.10x slower                                          |
| json_dumps           | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                          |
| pickle_pure_python   | 312 us                                                                 | 359 us: 1.15x slower                                           |
| unpickle_pure_python | 217 us                                                                 | 250 us: 1.15x slower                                           |
| xml_etree_generate   | 83.6 ms                                                                | 96.8 ms: 1.16x slower                                          |
| tomli_loads          | 1.95 sec                                                               | 2.34 sec: 1.20x slower                                         |
| xml_etree_process    | 58.6 ms                                                                | 70.6 ms: 1.21x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                          |
| python_startup_no_site | 7.45 ms                                                                | 9.66 ms: 1.30x slower                                          |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| django_template | 34.1 ms                                                                | 42.0 ms: 1.23x slower                                          |
| genshi_xml      | 48.5 ms                                                                | 59.8 ms: 1.23x slower                                          |
| genshi_text     | 21.5 ms                                                                | 28.0 ms: 1.30x slower                                          |
| mako            | 11.9 ms                                                                | 15.7 ms: 1.32x slower                                          |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal               | 4.19 ms                                                                | 1.76 ms: 2.37x faster                                          |
| create_gc_cycles           | 1.83 ms                                                                | 1.35 ms: 1.36x faster                                          |
| sqlite_synth               | 2.20 us                                                                | 2.04 us: 1.08x faster                                          |
| async_tree_io_tg           | 622 ms                                                                 | 577 ms: 1.08x faster                                           |
| xml_etree_iterparse        | 90.9 ms                                                                | 88.7 ms: 1.03x faster                                          |
| async_tree_cpu_io_mixed_tg | 519 ms                                                                 | 507 ms: 1.02x faster                                           |
| async_tree_io              | 623 ms                                                                 | 612 ms: 1.02x faster                                           |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                           |
| pidigits                   | 199 ms                                                                 | 199 ms: 1.00x faster                                           |
| async_tree_cpu_io_mixed    | 532 ms                                                                 | 537 ms: 1.01x slower                                           |
| pathlib                    | 18.8 ms                                                                | 19.0 ms: 1.01x slower                                          |
| regex_effbot               | 2.71 ms                                                                | 2.83 ms: 1.05x slower                                          |
| regex_v8                   | 24.0 ms                                                                | 25.1 ms: 1.05x slower                                          |
| python_startup             | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                          |
| float                      | 72.2 ms                                                                | 76.2 ms: 1.06x slower                                          |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                         |
| regex_dna                  | 171 ms                                                                 | 182 ms: 1.06x slower                                           |
| json                       | 5.08 ms                                                                | 5.42 ms: 1.07x slower                                          |
| coroutines                 | 22.4 ms                                                                | 24.2 ms: 1.08x slower                                          |
| async_tree_none            | 269 ms                                                                 | 292 ms: 1.08x slower                                           |
| bench_mp_pool              | 87.7 ms                                                                | 95.1 ms: 1.08x slower                                          |
| dulwich_log                | 75.7 ms                                                                | 82.4 ms: 1.09x slower                                          |
| async_tree_memoization     | 324 ms                                                                 | 354 ms: 1.09x slower                                           |
| docutils                   | 2.55 sec                                                               | 2.79 sec: 1.10x slower                                         |
| json_loads                 | 28.7 us                                                                | 31.6 us: 1.10x slower                                          |
| generators                 | 29.0 ms                                                                | 32.1 ms: 1.11x slower                                          |
| bpe_tokeniser              | 4.18 sec                                                               | 4.68 sec: 1.12x slower                                         |
| logging_silent             | 107 ns                                                                 | 120 ns: 1.12x slower                                           |
| sphinx                     | 979 ms                                                                 | 1.10 sec: 1.12x slower                                         |
| k_core                     | 2.05 sec                                                               | 2.32 sec: 1.13x slower                                         |
| pylint                     | 278 ms                                                                 | 315 ms: 1.13x slower                                           |
| scimark_sor                | 115 ms                                                                 | 132 ms: 1.14x slower                                           |
| json_dumps                 | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                          |
| spectral_norm              | 94.3 ms                                                                | 108 ms: 1.14x slower                                           |
| pickle_pure_python         | 312 us                                                                 | 359 us: 1.15x slower                                           |
| async_generators           | 325 ms                                                                 | 374 ms: 1.15x slower                                           |
| unpickle_pure_python       | 217 us                                                                 | 250 us: 1.15x slower                                           |
| subparsers                 | 21.9 ms                                                                | 25.2 ms: 1.15x slower                                          |
| many_optionals             | 1.02 ms                                                                | 1.18 ms: 1.16x slower                                          |
| xml_etree_generate         | 83.6 ms                                                                | 96.8 ms: 1.16x slower                                          |
| mdp                        | 2.33 sec                                                               | 2.71 sec: 1.16x slower                                         |
| telco                      | 7.45 ms                                                                | 8.65 ms: 1.16x slower                                          |
| sqlglot_normalize          | 103 ms                                                                 | 120 ms: 1.16x slower                                           |
| logging_simple             | 5.99 us                                                                | 7.10 us: 1.18x slower                                          |
| pprint_safe_repr           | 688 ms                                                                 | 817 ms: 1.19x slower                                           |
| sqlglot_optimize           | 51.5 ms                                                                | 61.1 ms: 1.19x slower                                          |
| 2to3                       | 255 ms                                                                 | 304 ms: 1.19x slower                                           |
| regex_compile              | 127 ms                                                                 | 152 ms: 1.19x slower                                           |
| comprehensions             | 16.5 us                                                                | 19.8 us: 1.20x slower                                          |
| pyflate                    | 413 ms                                                                 | 495 ms: 1.20x slower                                           |
| pprint_pformat             | 1.41 sec                                                               | 1.69 sec: 1.20x slower                                         |
| tomli_loads                | 1.95 sec                                                               | 2.34 sec: 1.20x slower                                         |
| sympy_sum                  | 153 ms                                                                 | 185 ms: 1.21x slower                                           |
| xml_etree_process          | 58.6 ms                                                                | 70.6 ms: 1.21x slower                                          |
| logging_format             | 6.71 us                                                                | 8.11 us: 1.21x slower                                          |
| thrift                     | 737 us                                                                 | 890 us: 1.21x slower                                           |
| sympy_expand               | 452 ms                                                                 | 547 ms: 1.21x slower                                           |
| go                         | 116 ms                                                                 | 140 ms: 1.21x slower                                           |
| nqueens                    | 79.6 ms                                                                | 96.6 ms: 1.21x slower                                          |
| sqlglot_transpile          | 1.58 ms                                                                | 1.92 ms: 1.22x slower                                          |
| coverage                   | 79.9 ms                                                                | 97.3 ms: 1.22x slower                                          |
| scimark_fft                | 318 ms                                                                 | 388 ms: 1.22x slower                                           |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                          |
| sqlalchemy_declarative     | 127 ms                                                                 | 156 ms: 1.22x slower                                           |
| deepcopy                   | 252 us                                                                 | 308 us: 1.22x slower                                           |
| django_template            | 34.1 ms                                                                | 42.0 ms: 1.23x slower                                          |
| genshi_xml                 | 48.5 ms                                                                | 59.8 ms: 1.23x slower                                          |
| deltablue                  | 3.19 ms                                                                | 3.92 ms: 1.23x slower                                          |
| deepcopy_reduce            | 2.57 us                                                                | 3.16 us: 1.23x slower                                          |
| sympy_str                  | 270 ms                                                                 | 333 ms: 1.23x slower                                           |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.0 ms: 1.24x slower                                          |
| scimark_lu                 | 113 ms                                                                 | 140 ms: 1.24x slower                                           |
| chaos                      | 55.8 ms                                                                | 69.4 ms: 1.24x slower                                          |
| hexiom                     | 5.92 ms                                                                | 7.39 ms: 1.25x slower                                          |
| sqlglot_parse              | 1.28 ms                                                                | 1.60 ms: 1.25x slower                                          |
| raytrace                   | 259 ms                                                                 | 325 ms: 1.25x slower                                           |
| shortest_path              | 433 ms                                                                 | 550 ms: 1.27x slower                                           |
| connected_components       | 391 ms                                                                 | 497 ms: 1.27x slower                                           |
| deepcopy_memo              | 30.1 us                                                                | 38.7 us: 1.29x slower                                          |
| crypto_pyaes               | 68.0 ms                                                                | 87.6 ms: 1.29x slower                                          |
| fannkuch                   | 377 ms                                                                 | 487 ms: 1.29x slower                                           |
| python_startup_no_site     | 7.45 ms                                                                | 9.66 ms: 1.30x slower                                          |
| richards                   | 42.7 ms                                                                | 55.5 ms: 1.30x slower                                          |
| typing_runtime_protocols   | 151 us                                                                 | 196 us: 1.30x slower                                           |
| genshi_text                | 21.5 ms                                                                | 28.0 ms: 1.30x slower                                          |
| scimark_monte_carlo        | 63.2 ms                                                                | 82.4 ms: 1.30x slower                                          |
| mako                       | 11.9 ms                                                                | 15.7 ms: 1.32x slower                                          |
| richards_super             | 48.9 ms                                                                | 64.7 ms: 1.32x slower                                          |
| meteor_contest             | 97.4 ms                                                                | 130 ms: 1.34x slower                                           |
| scimark_sparse_mat_mult    | 4.27 ms                                                                | 5.87 ms: 1.38x slower                                          |
| nbody                      | 87.7 ms                                                                | 130 ms: 1.48x slower                                           |
| bench_thread_pool          | 1.03 ms                                                                | 3.32 ms: 3.21x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                   |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250214-3.14.0a5+-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86.json: html5lib

- Geometric mean (including insignificant results): 1.126x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x