# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 1998b35
- commit date: 2025-02-21
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 301 ms                                                                 | 287 ms: 1.05x faster                                                  |
| docutils       | 2.80 sec                                                               | 2.72 sec: 1.03x faster                                                |
| html5lib       | 72.2 ms                                                                | 67.1 ms: 1.08x faster                                                 |
| sphinx         | 1.09 sec                                                               | 1.07 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 240 ms                                                                 | 226 ms: 1.06x faster                                                  |
| async_tree_io              | 588 ms                                                                 | 557 ms: 1.06x faster                                                  |
| async_tree_io_tg           | 555 ms                                                                 | 528 ms: 1.05x faster                                                  |
| async_tree_none            | 277 ms                                                                 | 265 ms: 1.05x faster                                                  |
| async_tree_memoization     | 339 ms                                                                 | 325 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 293 ms: 1.04x faster                                                  |
| async_generators           | 370 ms                                                                 | 360 ms: 1.03x faster                                                  |
| coroutines                 | 23.1 ms                                                                | 22.5 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 559 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 527 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 131 ms                                                                 | 114 ms: 1.15x faster                                                  |
| float          | 75.9 ms                                                                | 68.9 ms: 1.10x faster                                                 |
| pidigits       | 193 ms                                                                 | 240 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 154 ms                                                                 | 144 ms: 1.07x faster                                                  |
| regex_v8       | 23.7 ms                                                                | 23.3 ms: 1.01x faster                                                 |
| regex_dna      | 183 ms                                                                 | 182 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.34 sec                                                               | 2.09 sec: 1.12x faster                                                |
| pickle_pure_python   | 363 us                                                                 | 330 us: 1.10x faster                                                  |
| unpickle_pure_python | 250 us                                                                 | 229 us: 1.09x faster                                                  |
| xml_etree_process    | 69.4 ms                                                                | 66.4 ms: 1.05x faster                                                 |
| xml_etree_generate   | 95.8 ms                                                                | 92.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 88.5 ms                                                                | 85.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                                  |
| json_loads           | 31.4 us                                                                | 31.5 us: 1.01x slower                                                 |
| json_dumps           | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                                | 9.65 ms: 1.01x slower                                                 |
| python_startup         | 15.5 ms                                                                | 15.6 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.7 ms                                                                | 25.3 ms: 1.09x faster                                                 |
| genshi_xml      | 59.3 ms                                                                | 55.7 ms: 1.06x faster                                                 |
| django_template | 42.6 ms                                                                | 40.2 ms: 1.06x faster                                                 |
| mako            | 15.8 ms                                                                | 15.1 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.07x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250220-vultr-x86_64-python-6c450f44c283c61d0e1a-3.14.0a5+-6c450f4 | bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-1998b35 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 131 ms                                                                 | 114 ms: 1.15x faster                                                  |
| go                         | 140 ms                                                                 | 123 ms: 1.14x faster                                                  |
| tomli_loads                | 2.34 sec                                                               | 2.09 sec: 1.12x faster                                                |
| scimark_sparse_mat_mult    | 5.70 ms                                                                | 5.11 ms: 1.12x faster                                                 |
| richards                   | 55.0 ms                                                                | 49.5 ms: 1.11x faster                                                 |
| deepcopy_memo              | 38.7 us                                                                | 34.9 us: 1.11x faster                                                 |
| scimark_fft                | 389 ms                                                                 | 351 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 82.3 ms                                                                | 74.3 ms: 1.11x faster                                                 |
| richards_super             | 63.9 ms                                                                | 57.7 ms: 1.11x faster                                                 |
| pyflate                    | 499 ms                                                                 | 452 ms: 1.10x faster                                                  |
| raytrace                   | 319 ms                                                                 | 290 ms: 1.10x faster                                                  |
| float                      | 75.9 ms                                                                | 68.9 ms: 1.10x faster                                                 |
| pickle_pure_python         | 363 us                                                                 | 330 us: 1.10x faster                                                  |
| scimark_sor                | 132 ms                                                                 | 120 ms: 1.10x faster                                                  |
| deltablue                  | 3.82 ms                                                                | 3.48 ms: 1.10x faster                                                 |
| genshi_text                | 27.7 ms                                                                | 25.3 ms: 1.09x faster                                                 |
| logging_silent             | 114 ns                                                                 | 105 ns: 1.09x faster                                                  |
| pprint_safe_repr           | 829 ms                                                                 | 761 ms: 1.09x faster                                                  |
| unpickle_pure_python       | 250 us                                                                 | 229 us: 1.09x faster                                                  |
| pprint_pformat             | 1.71 sec                                                               | 1.57 sec: 1.09x faster                                                |
| chaos                      | 69.0 ms                                                                | 63.5 ms: 1.09x faster                                                 |
| fannkuch                   | 492 ms                                                                 | 455 ms: 1.08x faster                                                  |
| sqlglot_parse              | 1.58 ms                                                                | 1.47 ms: 1.08x faster                                                 |
| deepcopy                   | 314 us                                                                 | 292 us: 1.08x faster                                                  |
| html5lib                   | 72.2 ms                                                                | 67.1 ms: 1.08x faster                                                 |
| hexiom                     | 7.34 ms                                                                | 6.82 ms: 1.07x faster                                                 |
| sqlglot_transpile          | 1.91 ms                                                                | 1.78 ms: 1.07x faster                                                 |
| regex_compile              | 154 ms                                                                 | 144 ms: 1.07x faster                                                  |
| generators                 | 31.7 ms                                                                | 29.6 ms: 1.07x faster                                                 |
| nqueens                    | 97.0 ms                                                                | 91.0 ms: 1.07x faster                                                 |
| genshi_xml                 | 59.3 ms                                                                | 55.7 ms: 1.06x faster                                                 |
| async_tree_none_tg         | 240 ms                                                                 | 226 ms: 1.06x faster                                                  |
| scimark_lu                 | 138 ms                                                                 | 130 ms: 1.06x faster                                                  |
| django_template            | 42.6 ms                                                                | 40.2 ms: 1.06x faster                                                 |
| async_tree_io              | 588 ms                                                                 | 557 ms: 1.06x faster                                                  |
| many_optionals             | 1.18 ms                                                                | 1.12 ms: 1.06x faster                                                 |
| comprehensions             | 19.6 us                                                                | 18.6 us: 1.05x faster                                                 |
| async_tree_io_tg           | 555 ms                                                                 | 528 ms: 1.05x faster                                                  |
| 2to3                       | 301 ms                                                                 | 287 ms: 1.05x faster                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 115 ms: 1.05x faster                                                  |
| crypto_pyaes               | 87.5 ms                                                                | 83.4 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.70 sec                                                               | 4.48 sec: 1.05x faster                                                |
| async_tree_none            | 277 ms                                                                 | 265 ms: 1.05x faster                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 58.7 ms: 1.05x faster                                                 |
| xml_etree_process          | 69.4 ms                                                                | 66.4 ms: 1.05x faster                                                 |
| mako                       | 15.8 ms                                                                | 15.1 ms: 1.04x faster                                                 |
| async_tree_memoization     | 339 ms                                                                 | 325 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 293 ms: 1.04x faster                                                  |
| subparsers                 | 25.6 ms                                                                | 24.6 ms: 1.04x faster                                                 |
| typing_runtime_protocols   | 197 us                                                                 | 190 us: 1.04x faster                                                  |
| pycparser                  | 1.18 sec                                                               | 1.14 sec: 1.04x faster                                                |
| xml_etree_generate         | 95.8 ms                                                                | 92.4 ms: 1.04x faster                                                 |
| sympy_integrate            | 23.9 ms                                                                | 23.1 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 88.5 ms                                                                | 85.6 ms: 1.03x faster                                                 |
| sympy_str                  | 332 ms                                                                 | 321 ms: 1.03x faster                                                  |
| sympy_expand               | 546 ms                                                                 | 529 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.18 us                                                                | 3.09 us: 1.03x faster                                                 |
| docutils                   | 2.80 sec                                                               | 2.72 sec: 1.03x faster                                                |
| k_core                     | 2.31 sec                                                               | 2.25 sec: 1.03x faster                                                |
| async_generators           | 370 ms                                                                 | 360 ms: 1.03x faster                                                  |
| meteor_contest             | 129 ms                                                                 | 125 ms: 1.03x faster                                                  |
| coroutines                 | 23.1 ms                                                                | 22.5 ms: 1.03x faster                                                 |
| sphinx                     | 1.09 sec                                                               | 1.07 sec: 1.03x faster                                                |
| shortest_path              | 545 ms                                                                 | 532 ms: 1.02x faster                                                  |
| logging_format             | 8.15 us                                                                | 7.96 us: 1.02x faster                                                 |
| connected_components       | 493 ms                                                                 | 482 ms: 1.02x faster                                                  |
| pylint                     | 315 ms                                                                 | 308 ms: 1.02x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.02x faster                                                  |
| pathlib                    | 19.6 ms                                                                | 19.2 ms: 1.02x faster                                                 |
| sqlalchemy_declarative     | 158 ms                                                                 | 154 ms: 1.02x faster                                                  |
| dulwich_log                | 83.1 ms                                                                | 81.6 ms: 1.02x faster                                                 |
| sympy_sum                  | 185 ms                                                                 | 182 ms: 1.02x faster                                                  |
| coverage                   | 97.3 ms                                                                | 95.7 ms: 1.02x faster                                                 |
| logging_simple             | 7.07 us                                                                | 6.96 us: 1.02x faster                                                 |
| telco                      | 8.72 ms                                                                | 8.59 ms: 1.01x faster                                                 |
| regex_v8                   | 23.7 ms                                                                | 23.3 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.30 ms                                                                | 3.26 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.05 us                                                                | 2.03 us: 1.01x faster                                                 |
| regex_dna                  | 183 ms                                                                 | 182 ms: 1.01x faster                                                  |
| bench_mp_pool              | 94.6 ms                                                                | 95.1 ms: 1.01x slower                                                 |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                                  |
| json_loads                 | 31.4 us                                                                | 31.5 us: 1.01x slower                                                 |
| python_startup_no_site     | 9.59 ms                                                                | 9.65 ms: 1.01x slower                                                 |
| python_startup             | 15.5 ms                                                                | 15.6 ms: 1.01x slower                                                 |
| mdp                        | 2.68 sec                                                               | 2.70 sec: 1.01x slower                                                |
| json_dumps                 | 12.7 ms                                                                | 12.8 ms: 1.01x slower                                                 |
| gc_traversal               | 1.73 ms                                                                | 1.75 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.30 ms                                                                | 1.34 ms: 1.03x slower                                                 |
| async_tree_cpu_io_mixed    | 522 ms                                                                 | 559 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed_tg | 491 ms                                                                 | 527 ms: 1.07x slower                                                  |
| pidigits                   | 193 ms                                                                 | 240 ms: 1.24x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (5): json, asyncio_websockets, regex_effbot, thrift, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x