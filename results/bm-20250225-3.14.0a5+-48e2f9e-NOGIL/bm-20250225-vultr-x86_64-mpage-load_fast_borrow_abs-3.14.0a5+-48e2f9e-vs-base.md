# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.026x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| html5lib       | 73.0 ms                                                                | 71.7 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 485 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 599 ms                                                                 | 518 ms: 1.16x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 270 ms: 1.01x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 575 ms: 1.01x faster                                                  |
| async_tree_io_tg           | 551 ms                                                                 | 544 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 304 ms                                                                 | 301 ms: 1.01x faster                                                  |
| asyncio_websockets         | 511 ms                                                                 | 518 ms: 1.01x slower                                                  |
| coroutines                 | 22.8 ms                                                                | 23.8 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 244 ms                                                                 | 208 ms: 1.18x faster                                                  |
| nbody          | 132 ms                                                                 | 118 ms: 1.12x faster                                                  |
| float          | 76.4 ms                                                                | 69.9 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.78 ms                                                                | 2.73 ms: 1.02x faster                                                 |
| regex_compile  | 155 ms                                                                 | 152 ms: 1.02x faster                                                  |
| regex_dna      | 184 ms                                                                 | 185 ms: 1.00x slower                                                  |
| regex_v8       | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 360 us                                                                 | 345 us: 1.04x faster                                                  |
| tomli_loads          | 2.36 sec                                                               | 2.27 sec: 1.04x faster                                                |
| unpickle_pure_python | 247 us                                                                 | 238 us: 1.04x faster                                                  |
| json_dumps           | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                 |
| xml_etree_process    | 69.5 ms                                                                | 69.1 ms: 1.01x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| xml_etree_generate   | 95.7 ms                                                                | 95.4 ms: 1.00x faster                                                 |
| json_loads           | 29.2 us                                                                | 29.8 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.64 ms                                                                | 9.65 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 28.0 ms                                                                | 26.8 ms: 1.05x faster                                                 |
| genshi_xml     | 59.6 ms                                                                | 57.7 ms: 1.03x faster                                                 |
| mako           | 15.7 ms                                                                | 15.4 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 244 ms                                                                 | 208 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 485 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 599 ms                                                                 | 518 ms: 1.16x faster                                                  |
| scimark_sparse_mat_mult    | 5.95 ms                                                                | 5.16 ms: 1.15x faster                                                 |
| nbody                      | 132 ms                                                                 | 118 ms: 1.12x faster                                                  |
| scimark_fft                | 397 ms                                                                 | 356 ms: 1.11x faster                                                  |
| float                      | 76.4 ms                                                                | 69.9 ms: 1.09x faster                                                 |
| mdp                        | 2.79 sec                                                               | 2.57 sec: 1.09x faster                                                |
| scimark_monte_carlo        | 82.4 ms                                                                | 76.0 ms: 1.08x faster                                                 |
| fannkuch                   | 497 ms                                                                 | 465 ms: 1.07x faster                                                  |
| go                         | 138 ms                                                                 | 129 ms: 1.06x faster                                                  |
| scimark_sor                | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| sqlglot_parse              | 1.60 ms                                                                | 1.52 ms: 1.05x faster                                                 |
| deepcopy_memo              | 37.9 us                                                                | 36.1 us: 1.05x faster                                                 |
| richards                   | 54.7 ms                                                                | 52.3 ms: 1.05x faster                                                 |
| genshi_text                | 28.0 ms                                                                | 26.8 ms: 1.05x faster                                                 |
| spectral_norm              | 113 ms                                                                 | 108 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.92 ms                                                                | 1.84 ms: 1.04x faster                                                 |
| chaos                      | 69.1 ms                                                                | 66.2 ms: 1.04x faster                                                 |
| pickle_pure_python         | 360 us                                                                 | 345 us: 1.04x faster                                                  |
| tomli_loads                | 2.36 sec                                                               | 2.27 sec: 1.04x faster                                                |
| raytrace                   | 315 ms                                                                 | 303 ms: 1.04x faster                                                  |
| deltablue                  | 3.77 ms                                                                | 3.62 ms: 1.04x faster                                                 |
| richards_super             | 63.4 ms                                                                | 61.1 ms: 1.04x faster                                                 |
| unpickle_pure_python       | 247 us                                                                 | 238 us: 1.04x faster                                                  |
| pyflate                    | 495 ms                                                                 | 478 ms: 1.04x faster                                                  |
| nqueens                    | 97.4 ms                                                                | 94.2 ms: 1.03x faster                                                 |
| genshi_xml                 | 59.6 ms                                                                | 57.7 ms: 1.03x faster                                                 |
| comprehensions             | 19.8 us                                                                | 19.2 us: 1.03x faster                                                 |
| bpe_tokeniser              | 4.75 sec                                                               | 4.61 sec: 1.03x faster                                                |
| hexiom                     | 7.38 ms                                                                | 7.18 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.73 sec                                                               | 1.68 sec: 1.03x faster                                                |
| meteor_contest             | 131 ms                                                                 | 128 ms: 1.02x faster                                                  |
| many_optionals             | 1.17 ms                                                                | 1.14 ms: 1.02x faster                                                 |
| 2to3                       | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 835 ms                                                                 | 816 ms: 1.02x faster                                                  |
| mako                       | 15.7 ms                                                                | 15.4 ms: 1.02x faster                                                 |
| crypto_pyaes               | 86.6 ms                                                                | 84.8 ms: 1.02x faster                                                 |
| regex_effbot               | 2.78 ms                                                                | 2.73 ms: 1.02x faster                                                 |
| regex_compile              | 155 ms                                                                 | 152 ms: 1.02x faster                                                  |
| logging_format             | 8.33 us                                                                | 8.17 us: 1.02x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 119 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 61.3 ms                                                                | 60.2 ms: 1.02x faster                                                 |
| connected_components       | 494 ms                                                                 | 484 ms: 1.02x faster                                                  |
| scimark_lu                 | 140 ms                                                                 | 137 ms: 1.02x faster                                                  |
| deepcopy                   | 310 us                                                                 | 304 us: 1.02x faster                                                  |
| html5lib                   | 73.0 ms                                                                | 71.7 ms: 1.02x faster                                                 |
| sympy_integrate            | 24.0 ms                                                                | 23.6 ms: 1.02x faster                                                 |
| shortest_path              | 544 ms                                                                 | 536 ms: 1.02x faster                                                  |
| k_core                     | 2.30 sec                                                               | 2.27 sec: 1.02x faster                                                |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.01x faster                                                |
| async_tree_none            | 274 ms                                                                 | 270 ms: 1.01x faster                                                  |
| sympy_str                  | 335 ms                                                                 | 330 ms: 1.01x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 575 ms: 1.01x faster                                                  |
| async_tree_io_tg           | 551 ms                                                                 | 544 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.31 ms                                                                | 1.29 ms: 1.01x faster                                                 |
| async_tree_memoization_tg  | 304 ms                                                                 | 301 ms: 1.01x faster                                                  |
| sympy_expand               | 546 ms                                                                 | 541 ms: 1.01x faster                                                  |
| json_dumps                 | 13.0 ms                                                                | 12.9 ms: 1.01x faster                                                 |
| logging_simple             | 7.25 us                                                                | 7.19 us: 1.01x faster                                                 |
| bench_thread_pool          | 3.31 ms                                                                | 3.29 ms: 1.01x faster                                                 |
| logging_silent             | 109 ns                                                                 | 108 ns: 1.01x faster                                                  |
| xml_etree_process          | 69.5 ms                                                                | 69.1 ms: 1.01x faster                                                 |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| gc_traversal               | 1.72 ms                                                                | 1.71 ms: 1.00x faster                                                 |
| json                       | 5.09 ms                                                                | 5.07 ms: 1.00x faster                                                 |
| coverage                   | 96.5 ms                                                                | 96.2 ms: 1.00x faster                                                 |
| xml_etree_generate         | 95.7 ms                                                                | 95.4 ms: 1.00x faster                                                 |
| python_startup_no_site     | 9.64 ms                                                                | 9.65 ms: 1.00x slower                                                 |
| regex_dna                  | 184 ms                                                                 | 185 ms: 1.00x slower                                                  |
| thrift                     | 873 us                                                                 | 879 us: 1.01x slower                                                  |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                                  |
| generators                 | 32.5 ms                                                                | 32.8 ms: 1.01x slower                                                 |
| telco                      | 8.67 ms                                                                | 8.77 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.00 us                                                                | 2.03 us: 1.01x slower                                                 |
| asyncio_websockets         | 511 ms                                                                 | 518 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.17 us: 1.02x slower                                                 |
| json_loads                 | 29.2 us                                                                | 29.8 us: 1.02x slower                                                 |
| regex_v8                   | 23.4 ms                                                                | 23.9 ms: 1.02x slower                                                 |
| pathlib                    | 19.6 ms                                                                | 20.1 ms: 1.03x slower                                                 |
| coroutines                 | 22.8 ms                                                                | 23.8 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (15): typing_runtime_protocols, async_tree_none_tg, docutils, sphinx, async_tree_memoization, bench_mp_pool, xml_etree_iterparse, subparsers, async_generators, sympy_sum, python_startup, pylint, sqlalchemy_imperative, django_template, dulwich_log

- Geometric mean (including insignificant results): 1.026x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x