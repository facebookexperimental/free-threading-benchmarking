# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.028x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 306 ms                                                                 | 297 ms: 1.03x faster                                                  |
| html5lib       | 72.1 ms                                                                | 71.6 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 239 ms                                                                 | 229 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 485 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 555 ms                                                                 | 537 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 521 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 306 ms                                                                 | 299 ms: 1.02x faster                                                  |
| async_tree_memoization     | 338 ms                                                                 | 331 ms: 1.02x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 572 ms: 1.02x faster                                                  |
| async_tree_none            | 276 ms                                                                 | 271 ms: 1.02x faster                                                  |
| async_generators           | 373 ms                                                                 | 369 ms: 1.01x faster                                                  |
| asyncio_websockets         | 512 ms                                                                 | 517 ms: 1.01x slower                                                  |
| coroutines                 | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 78.5 ms                                                                | 69.9 ms: 1.12x faster                                                 |
| nbody          | 133 ms                                                                 | 119 ms: 1.12x faster                                                  |
| pidigits       | 196 ms                                                                 | 198 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                                 | 152 ms: 1.03x faster                                                  |
| regex_dna      | 183 ms                                                                 | 184 ms: 1.01x slower                                                  |
| regex_effbot   | 2.72 ms                                                                | 2.82 ms: 1.03x slower                                                 |
| regex_v8       | 23.5 ms                                                                | 24.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 250 us                                                                 | 234 us: 1.07x faster                                                  |
| pickle_pure_python   | 362 us                                                                 | 344 us: 1.05x faster                                                  |
| tomli_loads          | 2.35 sec                                                               | 2.25 sec: 1.05x faster                                                |
| xml_etree_process    | 70.3 ms                                                                | 68.8 ms: 1.02x faster                                                 |
| json_dumps           | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| xml_etree_generate   | 96.7 ms                                                                | 95.7 ms: 1.01x faster                                                 |
| json_loads           | 29.5 us                                                                | 29.3 us: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.66 ms                                                                | 9.67 ms: 1.00x slower                                                 |
| python_startup         | 15.6 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 28.4 ms                                                                | 26.5 ms: 1.07x faster                                                 |
| genshi_xml     | 59.8 ms                                                                | 57.4 ms: 1.04x faster                                                 |
| mako           | 15.9 ms                                                                | 15.4 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| scimark_fft                | 392 ms                                                                 | 342 ms: 1.15x faster                                                  |
| float                      | 78.5 ms                                                                | 69.9 ms: 1.12x faster                                                 |
| nbody                      | 133 ms                                                                 | 119 ms: 1.12x faster                                                  |
| scimark_sparse_mat_mult    | 5.74 ms                                                                | 5.15 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 83.8 ms                                                                | 76.4 ms: 1.10x faster                                                 |
| go                         | 141 ms                                                                 | 129 ms: 1.09x faster                                                  |
| raytrace                   | 326 ms                                                                 | 299 ms: 1.09x faster                                                  |
| deepcopy_memo              | 38.5 us                                                                | 35.4 us: 1.09x faster                                                 |
| scimark_sor                | 135 ms                                                                 | 126 ms: 1.07x faster                                                  |
| genshi_text                | 28.4 ms                                                                | 26.5 ms: 1.07x faster                                                 |
| pyflate                    | 506 ms                                                                 | 474 ms: 1.07x faster                                                  |
| fannkuch                   | 493 ms                                                                 | 462 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 250 us                                                                 | 234 us: 1.07x faster                                                  |
| sqlglot_parse              | 1.61 ms                                                                | 1.51 ms: 1.07x faster                                                 |
| deltablue                  | 3.85 ms                                                                | 3.61 ms: 1.06x faster                                                 |
| deepcopy                   | 311 us                                                                 | 293 us: 1.06x faster                                                  |
| pprint_safe_repr           | 843 ms                                                                 | 793 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.74 sec                                                               | 1.64 sec: 1.06x faster                                                |
| chaos                      | 69.7 ms                                                                | 65.9 ms: 1.06x faster                                                 |
| sqlglot_transpile          | 1.93 ms                                                                | 1.83 ms: 1.06x faster                                                 |
| logging_silent             | 113 ns                                                                 | 107 ns: 1.05x faster                                                  |
| pickle_pure_python         | 362 us                                                                 | 344 us: 1.05x faster                                                  |
| hexiom                     | 7.43 ms                                                                | 7.10 ms: 1.05x faster                                                 |
| tomli_loads                | 2.35 sec                                                               | 2.25 sec: 1.05x faster                                                |
| comprehensions             | 20.0 us                                                                | 19.2 us: 1.04x faster                                                 |
| async_tree_none_tg         | 239 ms                                                                 | 229 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.15 us                                                                | 3.02 us: 1.04x faster                                                 |
| genshi_xml                 | 59.8 ms                                                                | 57.4 ms: 1.04x faster                                                 |
| scimark_lu                 | 142 ms                                                                 | 137 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 200 us                                                                 | 192 us: 1.04x faster                                                  |
| bpe_tokeniser              | 4.77 sec                                                               | 4.60 sec: 1.04x faster                                                |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 485 ms: 1.04x faster                                                  |
| richards                   | 54.6 ms                                                                | 52.8 ms: 1.03x faster                                                 |
| mako                       | 15.9 ms                                                                | 15.4 ms: 1.03x faster                                                 |
| crypto_pyaes               | 87.9 ms                                                                | 85.0 ms: 1.03x faster                                                 |
| richards_super             | 63.2 ms                                                                | 61.2 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 555 ms                                                                 | 537 ms: 1.03x faster                                                  |
| nqueens                    | 97.1 ms                                                                | 94.0 ms: 1.03x faster                                                 |
| telco                      | 8.65 ms                                                                | 8.39 ms: 1.03x faster                                                 |
| 2to3                       | 306 ms                                                                 | 297 ms: 1.03x faster                                                  |
| spectral_norm              | 110 ms                                                                 | 107 ms: 1.03x faster                                                  |
| regex_compile              | 156 ms                                                                 | 152 ms: 1.03x faster                                                  |
| connected_components       | 498 ms                                                                 | 484 ms: 1.03x faster                                                  |
| many_optionals             | 1.17 ms                                                                | 1.14 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 534 ms                                                                 | 521 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.17 sec: 1.03x faster                                                |
| async_tree_memoization_tg  | 306 ms                                                                 | 299 ms: 1.02x faster                                                  |
| k_core                     | 2.31 sec                                                               | 2.26 sec: 1.02x faster                                                |
| sqlglot_optimize           | 61.8 ms                                                                | 60.4 ms: 1.02x faster                                                 |
| shortest_path              | 548 ms                                                                 | 536 ms: 1.02x faster                                                  |
| xml_etree_process          | 70.3 ms                                                                | 68.8 ms: 1.02x faster                                                 |
| async_tree_memoization     | 338 ms                                                                 | 331 ms: 1.02x faster                                                  |
| async_tree_io              | 583 ms                                                                 | 572 ms: 1.02x faster                                                  |
| async_tree_none            | 276 ms                                                                 | 271 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 121 ms                                                                 | 119 ms: 1.02x faster                                                  |
| json_dumps                 | 12.9 ms                                                                | 12.7 ms: 1.02x faster                                                 |
| sympy_str                  | 337 ms                                                                 | 331 ms: 1.02x faster                                                  |
| coverage                   | 99.1 ms                                                                | 97.5 ms: 1.02x faster                                                 |
| sympy_integrate            | 24.0 ms                                                                | 23.6 ms: 1.02x faster                                                 |
| json                       | 5.12 ms                                                                | 5.04 ms: 1.02x faster                                                 |
| thrift                     | 872 us                                                                 | 859 us: 1.02x faster                                                  |
| sqlite_synth               | 2.04 us                                                                | 2.01 us: 1.01x faster                                                 |
| xml_etree_generate         | 96.7 ms                                                                | 95.7 ms: 1.01x faster                                                 |
| async_generators           | 373 ms                                                                 | 369 ms: 1.01x faster                                                  |
| bench_thread_pool          | 3.32 ms                                                                | 3.29 ms: 1.01x faster                                                 |
| html5lib                   | 72.1 ms                                                                | 71.6 ms: 1.01x faster                                                 |
| dulwich_log                | 83.4 ms                                                                | 82.8 ms: 1.01x faster                                                 |
| json_loads                 | 29.5 us                                                                | 29.3 us: 1.01x faster                                                 |
| python_startup_no_site     | 9.66 ms                                                                | 9.67 ms: 1.00x slower                                                 |
| python_startup             | 15.6 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| regex_dna                  | 183 ms                                                                 | 184 ms: 1.01x slower                                                  |
| gc_traversal               | 1.72 ms                                                                | 1.74 ms: 1.01x slower                                                 |
| subparsers                 | 25.2 ms                                                                | 25.4 ms: 1.01x slower                                                 |
| pidigits                   | 196 ms                                                                 | 198 ms: 1.01x slower                                                  |
| asyncio_websockets         | 512 ms                                                                 | 517 ms: 1.01x slower                                                  |
| logging_format             | 8.11 us                                                                | 8.20 us: 1.01x slower                                                 |
| create_gc_cycles           | 1.30 ms                                                                | 1.33 ms: 1.02x slower                                                 |
| generators                 | 31.9 ms                                                                | 32.7 ms: 1.02x slower                                                 |
| mdp                        | 2.65 sec                                                               | 2.72 sec: 1.03x slower                                                |
| coroutines                 | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                                 |
| regex_effbot               | 2.72 ms                                                                | 2.82 ms: 1.03x slower                                                 |
| regex_v8                   | 23.5 ms                                                                | 24.3 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (14): meteor_contest, pathlib, sympy_expand, sympy_sum, docutils, xml_etree_parse, logging_simple, django_template, bench_mp_pool, xml_etree_iterparse, pylint, sqlalchemy_declarative, sphinx, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x