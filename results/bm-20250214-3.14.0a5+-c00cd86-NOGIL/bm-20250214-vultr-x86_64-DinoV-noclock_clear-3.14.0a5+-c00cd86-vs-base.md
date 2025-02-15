# Results vs. base

- fork: DinoV
- ref: noclock_clear
- machine: linux-x86_64
- commit hash: c00cd86
- commit date: 2025-02-14
- overall geometric mean: 1.000x faster
- HPT reliability: 95.30%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 302 ms                                                                 | 304 ms: 1.01x slower                                           |
| html5lib       | 71.5 ms                                                                | 70.3 ms: 1.02x faster                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 557 ms                                                                 | 507 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 537 ms: 1.10x faster                                           |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                           |
| asyncio_websockets         | 516 ms                                                                 | 518 ms: 1.01x slower                                           |
| async_tree_none            | 289 ms                                                                 | 292 ms: 1.01x slower                                           |
| coroutines                 | 23.6 ms                                                                | 24.2 ms: 1.03x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg, async_tree_io, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 218 ms                                                                 | 199 ms: 1.10x faster                                           |
| float          | 76.3 ms                                                                | 76.2 ms: 1.00x faster                                          |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                   |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 182 ms: 1.03x faster                                           |
| regex_effbot   | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                          |
| regex_compile  | 151 ms                                                                 | 152 ms: 1.01x slower                                           |
| regex_v8       | 23.6 ms                                                                | 25.1 ms: 1.07x slower                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                 | 127 ms: 1.02x faster                                           |
| unpickle_pure_python | 250 us                                                                 | 250 us: 1.00x slower                                           |
| json_loads           | 31.3 us                                                                | 31.6 us: 1.01x slower                                          |
| xml_etree_generate   | 95.9 ms                                                                | 96.8 ms: 1.01x slower                                          |
| xml_etree_process    | 69.9 ms                                                                | 70.6 ms: 1.01x slower                                          |
| json_dumps           | 12.8 ms                                                                | 13.0 ms: 1.01x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 9.60 ms                                                                | 9.66 ms: 1.01x slower                                          |
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                          |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| mako            | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                          |
| django_template | 41.8 ms                                                                | 42.0 ms: 1.01x slower                                          |
| genshi_xml      | 59.1 ms                                                                | 59.8 ms: 1.01x slower                                          |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5+-39cd972 | bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5+-c00cd86 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 557 ms                                                                 | 507 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed    | 589 ms                                                                 | 537 ms: 1.10x faster                                           |
| pidigits                   | 218 ms                                                                 | 199 ms: 1.10x faster                                           |
| regex_dna                  | 187 ms                                                                 | 182 ms: 1.03x faster                                           |
| create_gc_cycles           | 1.39 ms                                                                | 1.35 ms: 1.03x faster                                          |
| xml_etree_parse            | 130 ms                                                                 | 127 ms: 1.02x faster                                           |
| html5lib                   | 71.5 ms                                                                | 70.3 ms: 1.02x faster                                          |
| typing_runtime_protocols   | 199 us                                                                 | 196 us: 1.01x faster                                           |
| logging_simple             | 7.19 us                                                                | 7.10 us: 1.01x faster                                          |
| meteor_contest             | 132 ms                                                                 | 130 ms: 1.01x faster                                           |
| fannkuch                   | 492 ms                                                                 | 487 ms: 1.01x faster                                           |
| mako                       | 15.8 ms                                                                | 15.7 ms: 1.01x faster                                          |
| regex_effbot               | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                          |
| chaos                      | 70.0 ms                                                                | 69.4 ms: 1.01x faster                                          |
| pyflate                    | 499 ms                                                                 | 495 ms: 1.01x faster                                           |
| subparsers                 | 25.4 ms                                                                | 25.2 ms: 1.01x faster                                          |
| raytrace                   | 327 ms                                                                 | 325 ms: 1.01x faster                                           |
| async_generators           | 376 ms                                                                 | 374 ms: 1.01x faster                                           |
| scimark_monte_carlo        | 82.8 ms                                                                | 82.4 ms: 1.01x faster                                          |
| scimark_fft                | 389 ms                                                                 | 388 ms: 1.00x faster                                           |
| pprint_safe_repr           | 820 ms                                                                 | 817 ms: 1.00x faster                                           |
| deepcopy                   | 310 us                                                                 | 308 us: 1.00x faster                                           |
| float                      | 76.3 ms                                                                | 76.2 ms: 1.00x faster                                          |
| unpickle_pure_python       | 250 us                                                                 | 250 us: 1.00x slower                                           |
| sqlalchemy_declarative     | 155 ms                                                                 | 156 ms: 1.00x slower                                           |
| pprint_pformat             | 1.68 sec                                                               | 1.69 sec: 1.00x slower                                         |
| go                         | 139 ms                                                                 | 140 ms: 1.00x slower                                           |
| django_template            | 41.8 ms                                                                | 42.0 ms: 1.01x slower                                          |
| asyncio_websockets         | 516 ms                                                                 | 518 ms: 1.01x slower                                           |
| 2to3                       | 302 ms                                                                 | 304 ms: 1.01x slower                                           |
| crypto_pyaes               | 87.1 ms                                                                | 87.6 ms: 1.01x slower                                          |
| many_optionals             | 1.17 ms                                                                | 1.18 ms: 1.01x slower                                          |
| bench_mp_pool              | 94.6 ms                                                                | 95.1 ms: 1.01x slower                                          |
| deltablue                  | 3.90 ms                                                                | 3.92 ms: 1.01x slower                                          |
| spectral_norm              | 107 ms                                                                 | 108 ms: 1.01x slower                                           |
| python_startup_no_site     | 9.60 ms                                                                | 9.66 ms: 1.01x slower                                          |
| sympy_str                  | 331 ms                                                                 | 333 ms: 1.01x slower                                           |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                          |
| generators                 | 31.9 ms                                                                | 32.1 ms: 1.01x slower                                          |
| deepcopy_memo              | 38.4 us                                                                | 38.7 us: 1.01x slower                                          |
| json_loads                 | 31.3 us                                                                | 31.6 us: 1.01x slower                                          |
| sympy_integrate            | 23.9 ms                                                                | 24.1 ms: 1.01x slower                                          |
| shortest_path              | 545 ms                                                                 | 550 ms: 1.01x slower                                           |
| regex_compile              | 151 ms                                                                 | 152 ms: 1.01x slower                                           |
| async_tree_none            | 289 ms                                                                 | 292 ms: 1.01x slower                                           |
| xml_etree_generate         | 95.9 ms                                                                | 96.8 ms: 1.01x slower                                          |
| json                       | 5.37 ms                                                                | 5.42 ms: 1.01x slower                                          |
| sqlite_synth               | 2.02 us                                                                | 2.04 us: 1.01x slower                                          |
| xml_etree_process          | 69.9 ms                                                                | 70.6 ms: 1.01x slower                                          |
| sympy_expand               | 541 ms                                                                 | 547 ms: 1.01x slower                                           |
| genshi_xml                 | 59.1 ms                                                                | 59.8 ms: 1.01x slower                                          |
| richards                   | 54.8 ms                                                                | 55.5 ms: 1.01x slower                                          |
| json_dumps                 | 12.8 ms                                                                | 13.0 ms: 1.01x slower                                          |
| telco                      | 8.53 ms                                                                | 8.65 ms: 1.01x slower                                          |
| richards_super             | 63.7 ms                                                                | 64.7 ms: 1.02x slower                                          |
| gc_traversal               | 1.73 ms                                                                | 1.76 ms: 1.02x slower                                          |
| hexiom                     | 7.26 ms                                                                | 7.39 ms: 1.02x slower                                          |
| scimark_lu                 | 137 ms                                                                 | 140 ms: 1.02x slower                                           |
| coroutines                 | 23.6 ms                                                                | 24.2 ms: 1.03x slower                                          |
| scimark_sparse_mat_mult    | 5.62 ms                                                                | 5.87 ms: 1.04x slower                                          |
| logging_silent             | 113 ns                                                                 | 120 ns: 1.06x slower                                           |
| regex_v8                   | 23.6 ms                                                                | 25.1 ms: 1.07x slower                                          |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                   |

Benchmark hidden because not significant (34): async_tree_memoization, pathlib, nbody, sqlglot_normalize, bench_thread_pool, mdp, pickle_pure_python, xml_etree_iterparse, sqlglot_optimize, sqlglot_transpile, nqueens, async_tree_memoization_tg, deepcopy_reduce, async_tree_io_tg, bpe_tokeniser, comprehensions, dulwich_log, k_core, sympy_sum, tomli_loads, scimark_sor, async_tree_io, genshi_text, coverage, logging_format, docutils, sqlglot_parse, pylint, pycparser, sphinx, thrift, sqlalchemy_imperative, connected_components, async_tree_none_tg

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 95.30% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x