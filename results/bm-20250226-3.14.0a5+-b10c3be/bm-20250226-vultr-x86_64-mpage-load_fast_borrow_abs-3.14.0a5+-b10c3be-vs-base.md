# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: b10c3be
- commit date: 2025-02-26
- overall geometric mean: 1.006x faster
- HPT reliability: 84.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 250 ms: 1.00x faster                                                  |
| docutils       | 2.54 sec                                                               | 2.52 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 487 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 476 ms: 1.21x faster                                                  |
| async_tree_memoization     | 311 ms                                                                 | 309 ms: 1.01x faster                                                  |
| async_generators           | 316 ms                                                                 | 319 ms: 1.01x slower                                                  |
| coroutines                 | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, asyncio_websockets, async_tree_io_tg, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 189 ms: 1.31x faster                                                  |
| float          | 70.7 ms                                                                | 68.8 ms: 1.03x faster                                                 |
| nbody          | 84.7 ms                                                                | 86.4 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 24.2 ms: 1.01x faster                                                 |
| regex_dna      | 170 ms                                                                 | 176 ms: 1.04x slower                                                  |
| regex_effbot   | 2.68 ms                                                                | 2.86 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| xml_etree_process    | 57.1 ms                                                                | 56.8 ms: 1.01x faster                                                 |
| xml_etree_generate   | 82.0 ms                                                                | 81.6 ms: 1.00x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| pickle_pure_python   | 303 us                                                                 | 307 us: 1.01x slower                                                  |
| tomli_loads          | 1.82 sec                                                               | 1.89 sec: 1.04x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.54 ms                                                                | 7.49 ms: 1.01x faster                                                 |
| python_startup         | 14.8 ms                                                                | 14.8 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.8 ms                                                                | 46.5 ms: 1.03x faster                                                 |
| django_template | 33.5 ms                                                                | 32.8 ms: 1.02x faster                                                 |
| genshi_text     | 20.6 ms                                                                | 20.2 ms: 1.02x faster                                                 |
| mako            | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5+-9e474a9 | bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-b10c3be |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 247 ms                                                                 | 189 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 487 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 576 ms                                                                 | 476 ms: 1.21x faster                                                  |
| genshi_xml                 | 47.8 ms                                                                | 46.5 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 2.60 us                                                                | 2.53 us: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 4.13 ms                                                                | 4.02 ms: 1.03x faster                                                 |
| float                      | 70.7 ms                                                                | 68.8 ms: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                                 | 100 ns: 1.02x faster                                                  |
| scimark_lu                 | 109 ms                                                                 | 107 ms: 1.02x faster                                                  |
| nqueens                    | 74.9 ms                                                                | 73.3 ms: 1.02x faster                                                 |
| django_template            | 33.5 ms                                                                | 32.8 ms: 1.02x faster                                                 |
| genshi_text                | 20.6 ms                                                                | 20.2 ms: 1.02x faster                                                 |
| subparsers                 | 21.9 ms                                                                | 21.5 ms: 1.02x faster                                                 |
| regex_v8                   | 24.5 ms                                                                | 24.2 ms: 1.01x faster                                                 |
| sqlglot_parse              | 1.23 ms                                                                | 1.22 ms: 1.01x faster                                                 |
| deepcopy                   | 252 us                                                                 | 248 us: 1.01x faster                                                  |
| logging_format             | 6.68 us                                                                | 6.59 us: 1.01x faster                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 152 us: 1.01x faster                                                  |
| richards                   | 42.0 ms                                                                | 41.6 ms: 1.01x faster                                                 |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| sympy_str                  | 269 ms                                                                 | 266 ms: 1.01x faster                                                  |
| sympy_expand               | 453 ms                                                                 | 449 ms: 1.01x faster                                                  |
| pycparser                  | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                                |
| sqlite_synth               | 2.18 us                                                                | 2.16 us: 1.01x faster                                                 |
| richards_super             | 47.7 ms                                                                | 47.4 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 278 ms                                                                 | 276 ms: 1.01x faster                                                  |
| xml_etree_process          | 57.1 ms                                                                | 56.8 ms: 1.01x faster                                                 |
| sympy_integrate            | 19.4 ms                                                                | 19.2 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.54 ms                                                                | 7.49 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 1.53 ms                                                                | 1.52 ms: 1.01x faster                                                 |
| bench_mp_pool              | 88.5 ms                                                                | 88.0 ms: 1.01x faster                                                 |
| async_tree_memoization     | 311 ms                                                                 | 309 ms: 1.01x faster                                                  |
| docutils                   | 2.54 sec                                                               | 2.52 sec: 1.01x faster                                                |
| deepcopy_memo              | 29.1 us                                                                | 29.0 us: 1.01x faster                                                 |
| sqlalchemy_declarative     | 126 ms                                                                 | 125 ms: 1.01x faster                                                  |
| comprehensions             | 15.9 us                                                                | 15.8 us: 1.00x faster                                                 |
| xml_etree_generate         | 82.0 ms                                                                | 81.6 ms: 1.00x faster                                                 |
| crypto_pyaes               | 65.6 ms                                                                | 65.3 ms: 1.00x faster                                                 |
| 2to3                       | 251 ms                                                                 | 250 ms: 1.00x faster                                                  |
| hexiom                     | 5.65 ms                                                                | 5.62 ms: 1.00x faster                                                 |
| python_startup             | 14.8 ms                                                                | 14.8 ms: 1.00x faster                                                 |
| unpickle_pure_python       | 208 us                                                                 | 208 us: 1.00x faster                                                  |
| sqlglot_optimize           | 50.5 ms                                                                | 50.4 ms: 1.00x faster                                                 |
| mdp                        | 2.29 sec                                                               | 2.30 sec: 1.00x slower                                                |
| bpe_tokeniser              | 4.12 sec                                                               | 4.14 sec: 1.00x slower                                                |
| many_optionals             | 1.01 ms                                                                | 1.01 ms: 1.00x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.01x slower                                                 |
| raytrace                   | 254 ms                                                                 | 256 ms: 1.01x slower                                                  |
| fannkuch                   | 367 ms                                                                 | 369 ms: 1.01x slower                                                  |
| go                         | 110 ms                                                                 | 111 ms: 1.01x slower                                                  |
| async_generators           | 316 ms                                                                 | 319 ms: 1.01x slower                                                  |
| mako                       | 11.5 ms                                                                | 11.6 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.83 ms                                                                | 1.85 ms: 1.01x slower                                                 |
| scimark_fft                | 303 ms                                                                 | 307 ms: 1.01x slower                                                  |
| meteor_contest             | 97.8 ms                                                                | 99.1 ms: 1.01x slower                                                 |
| pickle_pure_python         | 303 us                                                                 | 307 us: 1.01x slower                                                  |
| spectral_norm              | 88.1 ms                                                                | 89.5 ms: 1.02x slower                                                 |
| generators                 | 26.3 ms                                                                | 26.8 ms: 1.02x slower                                                 |
| nbody                      | 84.7 ms                                                                | 86.4 ms: 1.02x slower                                                 |
| scimark_sor                | 109 ms                                                                 | 111 ms: 1.02x slower                                                  |
| regex_dna                  | 170 ms                                                                 | 176 ms: 1.04x slower                                                  |
| tomli_loads                | 1.82 sec                                                               | 1.89 sec: 1.04x slower                                                |
| pyflate                    | 393 ms                                                                 | 409 ms: 1.04x slower                                                  |
| coroutines                 | 20.8 ms                                                                | 21.7 ms: 1.04x slower                                                 |
| regex_effbot               | 2.68 ms                                                                | 2.86 ms: 1.07x slower                                                 |
| gc_traversal               | 4.26 ms                                                                | 4.80 ms: 1.13x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (29): pylint, async_tree_memoization_tg, async_tree_none_tg, sqlalchemy_imperative, connected_components, pprint_safe_repr, sympy_sum, sphinx, logging_simple, coverage, json_dumps, asyncio_websockets, thrift, pprint_pformat, shortest_path, xml_etree_iterparse, async_tree_io_tg, k_core, async_tree_io, scimark_monte_carlo, regex_compile, json_loads, pathlib, chaos, deltablue, async_tree_none, dulwich_log, json, telco

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 84.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x