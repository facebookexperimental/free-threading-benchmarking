# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 48e2f9e
- commit date: 2025-02-25
- overall geometric mean: 1.012x faster
- HPT reliability: 97.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 250 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators | 318 ms                                                                 | 316 ms: 1.01x faster                                                  |
| coroutines       | 21.4 ms                                                                | 21.7 ms: 1.01x slower                                                 |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (9): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 208 ms                                                                 | 197 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.7 ms                                                                | 25.1 ms: 1.02x slower                                                 |
| regex_dna      | 171 ms                                                                 | 176 ms: 1.03x slower                                                  |
| regex_effbot   | 2.65 ms                                                                | 2.87 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 307 us                                                                 | 302 us: 1.02x faster                                                  |
| unpickle_pure_python | 211 us                                                                 | 208 us: 1.01x faster                                                  |
| tomli_loads          | 1.89 sec                                                               | 1.88 sec: 1.01x faster                                                |
| xml_etree_iterparse  | 90.4 ms                                                                | 89.9 ms: 1.01x faster                                                 |
| json_loads           | 28.0 us                                                                | 28.6 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): xml_etree_generate, json_dumps, xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.51 ms                                                                | 7.52 ms: 1.00x slower                                                 |
| python_startup         | 14.7 ms                                                                | 14.8 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 47.7 ms                                                                | 46.4 ms: 1.03x faster                                                 |
| mako            | 11.6 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| django_template | 32.4 ms                                                                | 32.8 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark               | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe | bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-48e2f9e |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sqlglot_normalize       | 280 ms                                                                 | 101 ms: 2.77x faster                                                  |
| mdp                     | 2.42 sec                                                               | 2.30 sec: 1.05x faster                                                |
| pidigits                | 208 ms                                                                 | 197 ms: 1.05x faster                                                  |
| genshi_xml              | 47.7 ms                                                                | 46.4 ms: 1.03x faster                                                 |
| chaos                   | 54.8 ms                                                                | 53.7 ms: 1.02x faster                                                 |
| pathlib                 | 19.1 ms                                                                | 18.7 ms: 1.02x faster                                                 |
| logging_format          | 6.63 us                                                                | 6.52 us: 1.02x faster                                                 |
| thrift                  | 726 us                                                                 | 714 us: 1.02x faster                                                  |
| pycparser               | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| pickle_pure_python      | 307 us                                                                 | 302 us: 1.02x faster                                                  |
| subparsers              | 21.7 ms                                                                | 21.4 ms: 1.01x faster                                                 |
| richards                | 41.9 ms                                                                | 41.3 ms: 1.01x faster                                                 |
| deepcopy_memo           | 29.1 us                                                                | 28.7 us: 1.01x faster                                                 |
| unpickle_pure_python    | 211 us                                                                 | 208 us: 1.01x faster                                                  |
| go                      | 111 ms                                                                 | 110 ms: 1.01x faster                                                  |
| pprint_pformat          | 1.39 sec                                                               | 1.37 sec: 1.01x faster                                                |
| many_optionals          | 1.01 ms                                                                | 1.00 ms: 1.01x faster                                                 |
| raytrace                | 257 ms                                                                 | 254 ms: 1.01x faster                                                  |
| mako                    | 11.6 ms                                                                | 11.4 ms: 1.01x faster                                                 |
| generators              | 26.7 ms                                                                | 26.5 ms: 1.01x faster                                                 |
| sympy_expand            | 453 ms                                                                 | 449 ms: 1.01x faster                                                  |
| tomli_loads             | 1.89 sec                                                               | 1.88 sec: 1.01x faster                                                |
| richards_super          | 47.4 ms                                                                | 47.1 ms: 1.01x faster                                                 |
| scimark_monte_carlo     | 62.3 ms                                                                | 61.9 ms: 1.01x faster                                                 |
| pprint_safe_repr        | 677 ms                                                                 | 673 ms: 1.01x faster                                                  |
| logging_simple          | 5.82 us                                                                | 5.78 us: 1.01x faster                                                 |
| sqlglot_optimize        | 51.0 ms                                                                | 50.7 ms: 1.01x faster                                                 |
| async_generators        | 318 ms                                                                 | 316 ms: 1.01x faster                                                  |
| comprehensions          | 15.9 us                                                                | 15.8 us: 1.01x faster                                                 |
| xml_etree_iterparse     | 90.4 ms                                                                | 89.9 ms: 1.01x faster                                                 |
| shortest_path           | 429 ms                                                                 | 427 ms: 1.00x faster                                                  |
| coverage                | 79.5 ms                                                                | 79.2 ms: 1.00x faster                                                 |
| bench_thread_pool       | 1.03 ms                                                                | 1.03 ms: 1.00x faster                                                 |
| sympy_integrate         | 19.3 ms                                                                | 19.2 ms: 1.00x faster                                                 |
| crypto_pyaes            | 67.0 ms                                                                | 66.8 ms: 1.00x faster                                                 |
| 2to3                    | 250 ms                                                                 | 250 ms: 1.00x faster                                                  |
| python_startup_no_site  | 7.51 ms                                                                | 7.52 ms: 1.00x slower                                                 |
| deepcopy                | 245 us                                                                 | 246 us: 1.00x slower                                                  |
| python_startup          | 14.7 ms                                                                | 14.8 ms: 1.00x slower                                                 |
| deltablue               | 3.02 ms                                                                | 3.04 ms: 1.01x slower                                                 |
| dulwich_log             | 75.0 ms                                                                | 75.4 ms: 1.01x slower                                                 |
| bpe_tokeniser           | 4.15 sec                                                               | 4.18 sec: 1.01x slower                                                |
| fannkuch                | 366 ms                                                                 | 369 ms: 1.01x slower                                                  |
| sqlglot_transpile       | 1.53 ms                                                                | 1.54 ms: 1.01x slower                                                 |
| pyflate                 | 402 ms                                                                 | 406 ms: 1.01x slower                                                  |
| sqlglot_parse           | 1.23 ms                                                                | 1.24 ms: 1.01x slower                                                 |
| deepcopy_reduce         | 2.53 us                                                                | 2.56 us: 1.01x slower                                                 |
| scimark_fft             | 309 ms                                                                 | 312 ms: 1.01x slower                                                  |
| meteor_contest          | 99.2 ms                                                                | 100 ms: 1.01x slower                                                  |
| django_template         | 32.4 ms                                                                | 32.8 ms: 1.01x slower                                                 |
| coroutines              | 21.4 ms                                                                | 21.7 ms: 1.01x slower                                                 |
| nqueens                 | 74.7 ms                                                                | 75.6 ms: 1.01x slower                                                 |
| hexiom                  | 5.67 ms                                                                | 5.74 ms: 1.01x slower                                                 |
| create_gc_cycles        | 1.81 ms                                                                | 1.84 ms: 1.02x slower                                                 |
| regex_v8                | 24.7 ms                                                                | 25.1 ms: 1.02x slower                                                 |
| json_loads              | 28.0 us                                                                | 28.6 us: 1.02x slower                                                 |
| regex_dna               | 171 ms                                                                 | 176 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult | 4.15 ms                                                                | 4.34 ms: 1.05x slower                                                 |
| logging_silent          | 98.4 ns                                                                | 103 ns: 1.05x slower                                                  |
| regex_effbot            | 2.65 ms                                                                | 2.87 ms: 1.08x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (35): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, connected_components, typing_runtime_protocols, bench_mp_pool, pylint, async_tree_io_tg, sqlalchemy_declarative, float, docutils, sympy_str, async_tree_none, xml_etree_generate, sqlalchemy_imperative, asyncio_websockets, json_dumps, xml_etree_parse, genshi_text, scimark_sor, spectral_norm, async_tree_cpu_io_mixed_tg, gc_traversal, sympy_sum, scimark_lu, telco, regex_compile, k_core, async_tree_cpu_io_mixed, xml_etree_process, sphinx, nbody, sqlite_synth, json

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 97.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x