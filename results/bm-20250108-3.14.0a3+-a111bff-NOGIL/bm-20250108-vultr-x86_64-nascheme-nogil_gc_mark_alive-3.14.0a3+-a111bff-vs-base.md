# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.002x slower
- HPT reliability: 98.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 345 ms                                                                 | 342 ms: 1.01x faster                                                    |
| docutils       | 2.98 sec                                                               | 3.00 sec: 1.01x slower                                                  |
| html5lib       | 88.3 ms                                                                | 89.1 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 431 ms                                                                 | 429 ms: 1.00x faster                                                    |
| async_tree_io              | 757 ms                                                                 | 762 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 568 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 729 ms                                                                 | 734 ms: 1.01x slower                                                    |
| coroutines                 | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                                   |
| async_tree_none_tg         | 316 ms                                                                 | 319 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 397 ms                                                                 | 402 ms: 1.01x slower                                                    |
| async_generators           | 430 ms                                                                 | 446 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| pidigits       | 197 ms                                                                 | 198 ms: 1.00x slower                                                    |
| nbody          | 129 ms                                                                 | 131 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 166 ms                                                                 | 167 ms: 1.01x slower                                                    |
| regex_dna      | 181 ms                                                                 | 185 ms: 1.02x slower                                                    |
| regex_v8       | 23.4 ms                                                                | 24.6 ms: 1.05x slower                                                   |
| regex_effbot   | 2.69 ms                                                                | 2.83 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                 | 129 ms: 1.01x faster                                                    |
| json_dumps           | 14.1 ms                                                                | 14.1 ms: 1.01x faster                                                   |
| xml_etree_process    | 73.3 ms                                                                | 73.1 ms: 1.00x faster                                                   |
| unpickle_pure_python | 320 us                                                                 | 323 us: 1.01x slower                                                    |
| tomli_loads          | 2.32 sec                                                               | 2.35 sec: 1.01x slower                                                  |
| json_loads           | 28.6 us                                                                | 29.0 us: 1.02x slower                                                   |
| xml_etree_generate   | 97.3 ms                                                                | 98.8 ms: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                   |
| python_startup_no_site | 9.82 ms                                                                | 9.72 ms: 1.01x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 49.4 ms                                                                | 48.5 ms: 1.02x faster                                                   |
| mako            | 17.1 ms                                                                | 17.0 ms: 1.00x faster                                                   |
| genshi_xml      | 62.7 ms                                                                | 63.0 ms: 1.01x slower                                                   |
| genshi_text     | 30.3 ms                                                                | 30.7 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles           | 1.84 ms                                                                | 1.43 ms: 1.28x faster                                                   |
| bench_mp_pool              | 100 ms                                                                 | 94.2 ms: 1.07x faster                                                   |
| logging_silent             | 187 ns                                                                 | 180 ns: 1.04x faster                                                    |
| thrift                     | 1.01 ms                                                                | 988 us: 1.02x faster                                                    |
| django_template            | 49.4 ms                                                                | 48.5 ms: 1.02x faster                                                   |
| comprehensions             | 27.6 us                                                                | 27.1 us: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 5.45 ms                                                                | 5.36 ms: 1.02x faster                                                   |
| sqlglot_optimize           | 66.5 ms                                                                | 65.5 ms: 1.02x faster                                                   |
| deepcopy_reduce            | 3.46 us                                                                | 3.41 us: 1.02x faster                                                   |
| python_startup             | 15.7 ms                                                                | 15.5 ms: 1.01x faster                                                   |
| python_startup_no_site     | 9.82 ms                                                                | 9.72 ms: 1.01x faster                                                   |
| richards                   | 67.2 ms                                                                | 66.6 ms: 1.01x faster                                                   |
| sympy_str                  | 354 ms                                                                 | 351 ms: 1.01x faster                                                    |
| sqlglot_parse              | 2.28 ms                                                                | 2.26 ms: 1.01x faster                                                   |
| 2to3                       | 345 ms                                                                 | 342 ms: 1.01x faster                                                    |
| xml_etree_parse            | 130 ms                                                                 | 129 ms: 1.01x faster                                                    |
| dulwich_log                | 90.4 ms                                                                | 89.7 ms: 1.01x faster                                                   |
| json_dumps                 | 14.1 ms                                                                | 14.1 ms: 1.01x faster                                                   |
| sqlalchemy_declarative     | 183 ms                                                                 | 182 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.98 sec                                                               | 4.95 sec: 1.01x faster                                                  |
| sqlglot_normalize          | 132 ms                                                                 | 132 ms: 1.01x faster                                                    |
| mako                       | 17.1 ms                                                                | 17.0 ms: 1.00x faster                                                   |
| sympy_integrate            | 25.0 ms                                                                | 24.9 ms: 1.00x faster                                                   |
| async_tree_memoization     | 431 ms                                                                 | 429 ms: 1.00x faster                                                    |
| crypto_pyaes               | 90.2 ms                                                                | 89.8 ms: 1.00x faster                                                   |
| many_optionals             | 1.24 ms                                                                | 1.23 ms: 1.00x faster                                                   |
| xml_etree_process          | 73.3 ms                                                                | 73.1 ms: 1.00x faster                                                   |
| deepcopy_memo              | 40.6 us                                                                | 40.7 us: 1.00x slower                                                   |
| float                      | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| pidigits                   | 197 ms                                                                 | 198 ms: 1.00x slower                                                    |
| scimark_monte_carlo        | 103 ms                                                                 | 104 ms: 1.01x slower                                                    |
| deepcopy                   | 323 us                                                                 | 325 us: 1.01x slower                                                    |
| scimark_sor                | 201 ms                                                                 | 202 ms: 1.01x slower                                                    |
| genshi_xml                 | 62.7 ms                                                                | 63.0 ms: 1.01x slower                                                   |
| async_tree_io              | 757 ms                                                                 | 762 ms: 1.01x slower                                                    |
| docutils                   | 2.98 sec                                                               | 3.00 sec: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 564 ms                                                                 | 568 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 729 ms                                                                 | 734 ms: 1.01x slower                                                    |
| subparsers                 | 28.6 ms                                                                | 28.8 ms: 1.01x slower                                                   |
| nqueens                    | 95.3 ms                                                                | 96.1 ms: 1.01x slower                                                   |
| pprint_safe_repr           | 961 ms                                                                 | 969 ms: 1.01x slower                                                    |
| regex_compile              | 166 ms                                                                 | 167 ms: 1.01x slower                                                    |
| coroutines                 | 23.1 ms                                                                | 23.3 ms: 1.01x slower                                                   |
| html5lib                   | 88.3 ms                                                                | 89.1 ms: 1.01x slower                                                   |
| pprint_pformat             | 1.99 sec                                                               | 2.01 sec: 1.01x slower                                                  |
| unpickle_pure_python       | 320 us                                                                 | 323 us: 1.01x slower                                                    |
| async_tree_none_tg         | 316 ms                                                                 | 319 ms: 1.01x slower                                                    |
| tomli_loads                | 2.32 sec                                                               | 2.35 sec: 1.01x slower                                                  |
| pyflate                    | 620 ms                                                                 | 627 ms: 1.01x slower                                                    |
| scimark_fft                | 373 ms                                                                 | 378 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 397 ms                                                                 | 402 ms: 1.01x slower                                                    |
| genshi_text                | 30.3 ms                                                                | 30.7 ms: 1.01x slower                                                   |
| hexiom                     | 9.22 ms                                                                | 9.36 ms: 1.01x slower                                                   |
| json_loads                 | 28.6 us                                                                | 29.0 us: 1.02x slower                                                   |
| xml_etree_generate         | 97.3 ms                                                                | 98.8 ms: 1.02x slower                                                   |
| nbody                      | 129 ms                                                                 | 131 ms: 1.02x slower                                                    |
| json                       | 5.10 ms                                                                | 5.19 ms: 1.02x slower                                                   |
| regex_dna                  | 181 ms                                                                 | 185 ms: 1.02x slower                                                    |
| mdp                        | 2.73 sec                                                               | 2.79 sec: 1.02x slower                                                  |
| go                         | 231 ms                                                                 | 236 ms: 1.02x slower                                                    |
| logging_format             | 9.81 us                                                                | 10.1 us: 1.03x slower                                                   |
| generators                 | 38.4 ms                                                                | 39.4 ms: 1.03x slower                                                   |
| pathlib                    | 19.2 ms                                                                | 19.8 ms: 1.03x slower                                                   |
| async_generators           | 430 ms                                                                 | 446 ms: 1.04x slower                                                    |
| richards_super             | 74.6 ms                                                                | 77.7 ms: 1.04x slower                                                   |
| gc_traversal               | 3.52 ms                                                                | 3.67 ms: 1.04x slower                                                   |
| regex_v8                   | 23.4 ms                                                                | 24.6 ms: 1.05x slower                                                   |
| regex_effbot               | 2.69 ms                                                                | 2.83 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (28): pylint, meteor_contest, sqlite_synth, sphinx, deltablue, shortest_path, coverage, xml_etree_iterparse, pickle_pure_python, logging_simple, sympy_expand, bench_thread_pool, connected_components, async_tree_cpu_io_mixed, raytrace, asyncio_websockets, fannkuch, sympy_sum, spectral_norm, typing_runtime_protocols, k_core, async_tree_none, pycparser, scimark_lu, sqlglot_transpile, telco, chaos, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 98.39% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.02x