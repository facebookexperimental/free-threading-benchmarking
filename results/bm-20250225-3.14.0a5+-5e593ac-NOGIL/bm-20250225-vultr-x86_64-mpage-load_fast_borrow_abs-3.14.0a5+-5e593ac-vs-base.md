# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 5e593ac
- commit date: 2025-02-25
- overall geometric mean: 1.031x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| docutils       | 2.79 sec                                                               | 2.76 sec: 1.01x faster                                                |
| html5lib       | 73.0 ms                                                                | 71.0 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 484 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 599 ms                                                                 | 515 ms: 1.16x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 570 ms: 1.02x faster                                                  |
| async_tree_io_tg           | 551 ms                                                                 | 539 ms: 1.02x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 269 ms: 1.02x faster                                                  |
| async_tree_none_tg         | 236 ms                                                                 | 232 ms: 1.02x faster                                                  |
| async_tree_memoization     | 336 ms                                                                 | 331 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 304 ms                                                                 | 299 ms: 1.02x faster                                                  |
| async_generators           | 367 ms                                                                 | 368 ms: 1.00x slower                                                  |
| asyncio_websockets         | 511 ms                                                                 | 519 ms: 1.02x slower                                                  |
| coroutines                 | 22.8 ms                                                                | 23.5 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 244 ms                                                                 | 191 ms: 1.28x faster                                                  |
| nbody          | 132 ms                                                                 | 117 ms: 1.13x faster                                                  |
| float          | 76.4 ms                                                                | 70.7 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.16x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 155 ms                                                                 | 151 ms: 1.03x faster                                                  |
| regex_dna      | 184 ms                                                                 | 186 ms: 1.01x slower                                                  |
| regex_effbot   | 2.78 ms                                                                | 2.82 ms: 1.01x slower                                                 |
| regex_v8       | 23.4 ms                                                                | 24.4 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 247 us                                                                 | 237 us: 1.04x faster                                                  |
| pickle_pure_python   | 360 us                                                                 | 345 us: 1.04x faster                                                  |
| tomli_loads          | 2.36 sec                                                               | 2.28 sec: 1.04x faster                                                |
| json_dumps           | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 69.5 ms                                                                | 68.2 ms: 1.02x faster                                                 |
| xml_etree_generate   | 95.7 ms                                                                | 95.1 ms: 1.01x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| json_loads           | 29.2 us                                                                | 30.3 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.64 ms                                                                | 9.62 ms: 1.00x faster                                                 |
| python_startup         | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 28.0 ms                                                                | 27.0 ms: 1.04x faster                                                 |
| django_template | 42.2 ms                                                                | 41.2 ms: 1.02x faster                                                 |
| genshi_xml      | 59.6 ms                                                                | 58.3 ms: 1.02x faster                                                 |
| mako            | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-5e593ac |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 244 ms                                                                 | 191 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 570 ms                                                                 | 484 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 599 ms                                                                 | 515 ms: 1.16x faster                                                  |
| scimark_fft                | 397 ms                                                                 | 344 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult    | 5.95 ms                                                                | 5.22 ms: 1.14x faster                                                 |
| nbody                      | 132 ms                                                                 | 117 ms: 1.13x faster                                                  |
| mdp                        | 2.79 sec                                                               | 2.55 sec: 1.09x faster                                                |
| float                      | 76.4 ms                                                                | 70.7 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 82.4 ms                                                                | 76.3 ms: 1.08x faster                                                 |
| spectral_norm              | 113 ms                                                                 | 105 ms: 1.07x faster                                                  |
| fannkuch                   | 497 ms                                                                 | 464 ms: 1.07x faster                                                  |
| sqlglot_parse              | 1.60 ms                                                                | 1.50 ms: 1.07x faster                                                 |
| scimark_sor                | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| pyflate                    | 495 ms                                                                 | 465 ms: 1.06x faster                                                  |
| go                         | 138 ms                                                                 | 129 ms: 1.06x faster                                                  |
| chaos                      | 69.1 ms                                                                | 65.4 ms: 1.06x faster                                                 |
| sqlglot_transpile          | 1.92 ms                                                                | 1.82 ms: 1.06x faster                                                 |
| pprint_pformat             | 1.73 sec                                                               | 1.64 sec: 1.05x faster                                                |
| raytrace                   | 315 ms                                                                 | 299 ms: 1.05x faster                                                  |
| deepcopy_memo              | 37.9 us                                                                | 36.1 us: 1.05x faster                                                 |
| deepcopy                   | 310 us                                                                 | 295 us: 1.05x faster                                                  |
| deltablue                  | 3.77 ms                                                                | 3.60 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 835 ms                                                                 | 798 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 247 us                                                                 | 237 us: 1.04x faster                                                  |
| pickle_pure_python         | 360 us                                                                 | 345 us: 1.04x faster                                                  |
| logging_format             | 8.33 us                                                                | 8.01 us: 1.04x faster                                                 |
| genshi_text                | 28.0 ms                                                                | 27.0 ms: 1.04x faster                                                 |
| richards                   | 54.7 ms                                                                | 52.7 ms: 1.04x faster                                                 |
| tomli_loads                | 2.36 sec                                                               | 2.28 sec: 1.04x faster                                                |
| scimark_lu                 | 140 ms                                                                 | 134 ms: 1.04x faster                                                  |
| meteor_contest             | 131 ms                                                                 | 126 ms: 1.04x faster                                                  |
| richards_super             | 63.4 ms                                                                | 61.3 ms: 1.03x faster                                                 |
| logging_simple             | 7.25 us                                                                | 7.01 us: 1.03x faster                                                 |
| hexiom                     | 7.38 ms                                                                | 7.14 ms: 1.03x faster                                                 |
| bpe_tokeniser              | 4.75 sec                                                               | 4.62 sec: 1.03x faster                                                |
| html5lib                   | 73.0 ms                                                                | 71.0 ms: 1.03x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 118 ms: 1.03x faster                                                  |
| telco                      | 8.67 ms                                                                | 8.44 ms: 1.03x faster                                                 |
| regex_compile              | 155 ms                                                                 | 151 ms: 1.03x faster                                                  |
| comprehensions             | 19.8 us                                                                | 19.3 us: 1.03x faster                                                 |
| crypto_pyaes               | 86.6 ms                                                                | 84.4 ms: 1.03x faster                                                 |
| logging_silent             | 109 ns                                                                 | 106 ns: 1.03x faster                                                  |
| 2to3                       | 303 ms                                                                 | 296 ms: 1.02x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.16 sec: 1.02x faster                                                |
| django_template            | 42.2 ms                                                                | 41.2 ms: 1.02x faster                                                 |
| async_tree_io              | 583 ms                                                                 | 570 ms: 1.02x faster                                                  |
| many_optionals             | 1.17 ms                                                                | 1.14 ms: 1.02x faster                                                 |
| async_tree_io_tg           | 551 ms                                                                 | 539 ms: 1.02x faster                                                  |
| json_dumps                 | 13.0 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 200 us                                                                 | 196 us: 1.02x faster                                                  |
| genshi_xml                 | 59.6 ms                                                                | 58.3 ms: 1.02x faster                                                 |
| nqueens                    | 97.4 ms                                                                | 95.3 ms: 1.02x faster                                                 |
| connected_components       | 494 ms                                                                 | 483 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 61.3 ms                                                                | 60.2 ms: 1.02x faster                                                 |
| k_core                     | 2.30 sec                                                               | 2.26 sec: 1.02x faster                                                |
| xml_etree_process          | 69.5 ms                                                                | 68.2 ms: 1.02x faster                                                 |
| async_tree_none            | 274 ms                                                                 | 269 ms: 1.02x faster                                                  |
| mako                       | 15.7 ms                                                                | 15.5 ms: 1.02x faster                                                 |
| async_tree_none_tg         | 236 ms                                                                 | 232 ms: 1.02x faster                                                  |
| async_tree_memoization     | 336 ms                                                                 | 331 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.07 us: 1.02x faster                                                 |
| shortest_path              | 544 ms                                                                 | 536 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 304 ms                                                                 | 299 ms: 1.02x faster                                                  |
| sympy_integrate            | 24.0 ms                                                                | 23.6 ms: 1.01x faster                                                 |
| create_gc_cycles           | 1.31 ms                                                                | 1.29 ms: 1.01x faster                                                 |
| docutils                   | 2.79 sec                                                               | 2.76 sec: 1.01x faster                                                |
| sympy_str                  | 335 ms                                                                 | 332 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.31 ms                                                                | 3.29 ms: 1.01x faster                                                 |
| xml_etree_generate         | 95.7 ms                                                                | 95.1 ms: 1.01x faster                                                 |
| gc_traversal               | 1.72 ms                                                                | 1.71 ms: 1.00x faster                                                 |
| coverage                   | 96.5 ms                                                                | 96.2 ms: 1.00x faster                                                 |
| python_startup_no_site     | 9.64 ms                                                                | 9.62 ms: 1.00x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.6 ms: 1.00x faster                                                 |
| async_generators           | 367 ms                                                                 | 368 ms: 1.00x slower                                                  |
| sqlalchemy_declarative     | 156 ms                                                                 | 157 ms: 1.01x slower                                                  |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                                  |
| regex_dna                  | 184 ms                                                                 | 186 ms: 1.01x slower                                                  |
| generators                 | 32.5 ms                                                                | 32.9 ms: 1.01x slower                                                 |
| regex_effbot               | 2.78 ms                                                                | 2.82 ms: 1.01x slower                                                 |
| asyncio_websockets         | 511 ms                                                                 | 519 ms: 1.02x slower                                                  |
| coroutines                 | 22.8 ms                                                                | 23.5 ms: 1.03x slower                                                 |
| json                       | 5.09 ms                                                                | 5.24 ms: 1.03x slower                                                 |
| sqlite_synth               | 2.00 us                                                                | 2.07 us: 1.03x slower                                                 |
| json_loads                 | 29.2 us                                                                | 30.3 us: 1.04x slower                                                 |
| regex_v8                   | 23.4 ms                                                                | 24.4 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (11): sphinx, thrift, sympy_sum, bench_mp_pool, sympy_expand, pylint, xml_etree_iterparse, sqlalchemy_imperative, subparsers, pathlib, dulwich_log

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x