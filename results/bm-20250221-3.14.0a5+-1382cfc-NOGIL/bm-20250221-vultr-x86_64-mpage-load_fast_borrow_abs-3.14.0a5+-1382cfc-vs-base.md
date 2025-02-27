# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 1382cfc
- commit date: 2025-02-21
- overall geometric mean: 1.053x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 285 ms: 1.06x faster                                                  |
| docutils       | 2.80 sec                                                               | 2.71 sec: 1.03x faster                                                |
| html5lib       | 72.2 ms                                                                | 65.4 ms: 1.10x faster                                                 |
| sphinx         | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 240 ms                                                                 | 230 ms: 1.05x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 324 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 293 ms: 1.04x faster                                                  |
| async_tree_io              | 588 ms                                                                 | 564 ms: 1.04x faster                                                  |
| async_tree_none            | 277 ms                                                                 | 267 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 555 ms                                                                 | 535 ms: 1.04x faster                                                  |
| coroutines                 | 23.1 ms                                                                | 22.4 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 514 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 484 ms: 1.01x faster                                                  |
| async_generators           | 370 ms                                                                 | 365 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 131 ms                                                                 | 114 ms: 1.15x faster                                                  |
| float          | 75.9 ms                                                                | 67.9 ms: 1.12x faster                                                 |
| pidigits       | 193 ms                                                                 | 191 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                 | 143 ms: 1.08x faster                                                  |
| regex_dna      | 183 ms                                                                 | 183 ms: 1.00x faster                                                  |
| regex_effbot   | 2.76 ms                                                                | 2.87 ms: 1.04x slower                                                 |
| regex_v8       | 23.7 ms                                                                | 24.6 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 250 us                                                                 | 223 us: 1.12x faster                                                  |
| tomli_loads          | 2.34 sec                                                               | 2.11 sec: 1.11x faster                                                |
| pickle_pure_python   | 363 us                                                                 | 328 us: 1.11x faster                                                  |
| xml_etree_process    | 69.4 ms                                                                | 66.4 ms: 1.05x faster                                                 |
| xml_etree_generate   | 95.8 ms                                                                | 92.3 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 88.5 ms                                                                | 85.9 ms: 1.03x faster                                                 |
| json_loads           | 31.4 us                                                                | 31.3 us: 1.00x faster                                                 |
| json_dumps           | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.7 ms                                                                | 25.4 ms: 1.09x faster                                                 |
| genshi_xml      | 59.3 ms                                                                | 54.7 ms: 1.08x faster                                                 |
| django_template | 42.6 ms                                                                | 39.9 ms: 1.07x faster                                                 |
| mako            | 15.8 ms                                                                | 15.0 ms: 1.05x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.07x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1382cfc |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_fft                | 389 ms                                                                 | 332 ms: 1.17x faster                                                  |
| go                         | 140 ms                                                                 | 121 ms: 1.16x faster                                                  |
| nbody                      | 131 ms                                                                 | 114 ms: 1.15x faster                                                  |
| scimark_monte_carlo        | 82.3 ms                                                                | 72.0 ms: 1.14x faster                                                 |
| scimark_sor                | 132 ms                                                                 | 116 ms: 1.14x faster                                                  |
| richards                   | 55.0 ms                                                                | 48.5 ms: 1.13x faster                                                 |
| richards_super             | 63.9 ms                                                                | 56.8 ms: 1.12x faster                                                 |
| logging_silent             | 114 ns                                                                 | 102 ns: 1.12x faster                                                  |
| deepcopy_memo              | 38.7 us                                                                | 34.5 us: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.09 ms: 1.12x faster                                                 |
| unpickle_pure_python       | 250 us                                                                 | 223 us: 1.12x faster                                                  |
| pyflate                    | 499 ms                                                                 | 446 ms: 1.12x faster                                                  |
| float                      | 75.9 ms                                                                | 67.9 ms: 1.12x faster                                                 |
| raytrace                   | 319 ms                                                                 | 286 ms: 1.12x faster                                                  |
| chaos                      | 69.0 ms                                                                | 62.0 ms: 1.11x faster                                                 |
| tomli_loads                | 2.34 sec                                                               | 2.11 sec: 1.11x faster                                                |
| pickle_pure_python         | 363 us                                                                 | 328 us: 1.11x faster                                                  |
| deltablue                  | 3.82 ms                                                                | 3.44 ms: 1.11x faster                                                 |
| html5lib                   | 72.2 ms                                                                | 65.4 ms: 1.10x faster                                                 |
| hexiom                     | 7.34 ms                                                                | 6.66 ms: 1.10x faster                                                 |
| fannkuch                   | 492 ms                                                                 | 448 ms: 1.10x faster                                                  |
| pprint_pformat             | 1.71 sec                                                               | 1.56 sec: 1.09x faster                                                |
| pprint_safe_repr           | 829 ms                                                                 | 758 ms: 1.09x faster                                                  |
| genshi_text                | 27.7 ms                                                                | 25.4 ms: 1.09x faster                                                 |
| deepcopy                   | 314 us                                                                 | 289 us: 1.09x faster                                                  |
| genshi_xml                 | 59.3 ms                                                                | 54.7 ms: 1.08x faster                                                 |
| regex_compile              | 154 ms                                                                 | 143 ms: 1.08x faster                                                  |
| sqlglot_parse              | 1.58 ms                                                                | 1.47 ms: 1.08x faster                                                 |
| sqlglot_transpile          | 1.91 ms                                                                | 1.77 ms: 1.08x faster                                                 |
| scimark_lu                 | 138 ms                                                                 | 129 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 3.18 us                                                                | 2.97 us: 1.07x faster                                                 |
| django_template            | 42.6 ms                                                                | 39.9 ms: 1.07x faster                                                 |
| comprehensions             | 19.6 us                                                                | 18.4 us: 1.07x faster                                                 |
| bpe_tokeniser              | 4.70 sec                                                               | 4.42 sec: 1.06x faster                                                |
| many_optionals             | 1.18 ms                                                                | 1.11 ms: 1.06x faster                                                 |
| nqueens                    | 97.0 ms                                                                | 91.5 ms: 1.06x faster                                                 |
| sqlglot_normalize          | 121 ms                                                                 | 114 ms: 1.06x faster                                                  |
| logging_format             | 8.15 us                                                                | 7.72 us: 1.06x faster                                                 |
| 2to3                       | 301 ms                                                                 | 285 ms: 1.06x faster                                                  |
| crypto_pyaes               | 87.5 ms                                                                | 83.0 ms: 1.05x faster                                                 |
| mako                       | 15.8 ms                                                                | 15.0 ms: 1.05x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 58.4 ms: 1.05x faster                                                 |
| xml_etree_process          | 69.4 ms                                                                | 66.4 ms: 1.05x faster                                                 |
| async_tree_none_tg         | 240 ms                                                                 | 230 ms: 1.05x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 324 ms: 1.05x faster                                                  |
| logging_simple             | 7.07 us                                                                | 6.78 us: 1.04x faster                                                 |
| async_tree_memoization_tg  | 305 ms                                                                 | 293 ms: 1.04x faster                                                  |
| async_tree_io              | 588 ms                                                                 | 564 ms: 1.04x faster                                                  |
| pycparser                  | 1.18 sec                                                               | 1.14 sec: 1.04x faster                                                |
| sympy_integrate            | 23.9 ms                                                                | 23.0 ms: 1.04x faster                                                 |
| subparsers                 | 25.6 ms                                                                | 24.7 ms: 1.04x faster                                                 |
| xml_etree_generate         | 95.8 ms                                                                | 92.3 ms: 1.04x faster                                                 |
| async_tree_none            | 277 ms                                                                 | 267 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 555 ms                                                                 | 535 ms: 1.04x faster                                                  |
| meteor_contest             | 129 ms                                                                 | 124 ms: 1.04x faster                                                  |
| mdp                        | 2.68 sec                                                               | 2.59 sec: 1.03x faster                                                |
| docutils                   | 2.80 sec                                                               | 2.71 sec: 1.03x faster                                                |
| sympy_expand               | 546 ms                                                                 | 530 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 88.5 ms                                                                | 85.9 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 197 us                                                                 | 191 us: 1.03x faster                                                  |
| sqlalchemy_declarative     | 158 ms                                                                 | 153 ms: 1.03x faster                                                  |
| dulwich_log                | 83.1 ms                                                                | 80.7 ms: 1.03x faster                                                 |
| coroutines                 | 23.1 ms                                                                | 22.4 ms: 1.03x faster                                                 |
| sphinx                     | 1.09 sec                                                               | 1.06 sec: 1.03x faster                                                |
| k_core                     | 2.31 sec                                                               | 2.25 sec: 1.03x faster                                                |
| connected_components       | 493 ms                                                                 | 480 ms: 1.03x faster                                                  |
| sympy_str                  | 332 ms                                                                 | 323 ms: 1.03x faster                                                  |
| pylint                     | 315 ms                                                                 | 308 ms: 1.02x faster                                                  |
| shortest_path              | 545 ms                                                                 | 533 ms: 1.02x faster                                                  |
| generators                 | 31.7 ms                                                                | 31.0 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.05 us                                                                | 2.01 us: 1.02x faster                                                 |
| sympy_sum                  | 185 ms                                                                 | 182 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 514 ms: 1.02x faster                                                  |
| telco                      | 8.72 ms                                                                | 8.58 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 484 ms: 1.01x faster                                                  |
| pidigits                   | 193 ms                                                                 | 191 ms: 1.01x faster                                                  |
| pathlib                    | 19.6 ms                                                                | 19.3 ms: 1.01x faster                                                 |
| async_generators           | 370 ms                                                                 | 365 ms: 1.01x faster                                                  |
| json                       | 5.30 ms                                                                | 5.24 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.30 ms                                                                | 3.27 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.30 ms                                                                | 1.30 ms: 1.01x faster                                                 |
| json_loads                 | 31.4 us                                                                | 31.3 us: 1.00x faster                                                 |
| regex_dna                  | 183 ms                                                                 | 183 ms: 1.00x faster                                                  |
| json_dumps                 | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| regex_effbot               | 2.76 ms                                                                | 2.87 ms: 1.04x slower                                                 |
| regex_v8                   | 23.7 ms                                                                | 24.6 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (8): coverage, thrift, xml_etree_parse, gc_traversal, bench_mp_pool, python_startup_no_site, python_startup, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.053x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.03x