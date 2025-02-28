# Results vs. base

- fork: colesbury
- ref: gh_130382_reftracer_
- machine: linux-x86_64
- commit hash: d15b422
- commit date: 2025-02-28
- overall geometric mean: 1.002x slower
- HPT reliability: 86.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 250 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 471 ms: 1.03x faster                                                      |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 484 ms: 1.02x faster                                                      |
| async_tree_io_tg           | 603 ms                                                                 | 593 ms: 1.02x faster                                                      |
| async_tree_io              | 604 ms                                                                 | 594 ms: 1.02x faster                                                      |
| async_tree_memoization_tg  | 309 ms                                                                 | 304 ms: 1.02x faster                                                      |
| async_tree_none            | 261 ms                                                                 | 258 ms: 1.02x faster                                                      |
| async_tree_none_tg         | 254 ms                                                                 | 251 ms: 1.01x faster                                                      |
| async_generators           | 323 ms                                                                 | 320 ms: 1.01x faster                                                      |
| async_tree_memoization     | 314 ms                                                                 | 312 ms: 1.01x faster                                                      |
| coroutines                 | 21.2 ms                                                                | 22.3 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                 | 186 ms: 1.00x faster                                                      |
| nbody          | 85.6 ms                                                                | 93.2 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 25.4 ms                                                                | 23.4 ms: 1.08x faster                                                     |
| regex_effbot   | 2.85 ms                                                                | 2.68 ms: 1.06x faster                                                     |
| regex_dna      | 175 ms                                                                 | 169 ms: 1.03x faster                                                      |
| regex_compile  | 123 ms                                                                 | 126 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                      |
| unpickle_pure_python | 209 us                                                                 | 208 us: 1.00x faster                                                      |
| pickle_pure_python   | 305 us                                                                 | 307 us: 1.01x slower                                                      |
| xml_etree_process    | 57.0 ms                                                                | 57.5 ms: 1.01x slower                                                     |
| json_loads           | 28.3 us                                                                | 28.6 us: 1.01x slower                                                     |
| tomli_loads          | 1.85 sec                                                               | 1.88 sec: 1.01x slower                                                    |
| json_dumps           | 10.9 ms                                                                | 11.1 ms: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                | 14.8 ms: 1.00x faster                                                     |
| python_startup_no_site | 7.54 ms                                                                | 7.53 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                                     |
| genshi_xml      | 47.0 ms                                                                | 47.5 ms: 1.01x slower                                                     |
| django_template | 32.7 ms                                                                | 33.6 ms: 1.03x slower                                                     |
| genshi_text     | 20.1 ms                                                                | 20.7 ms: 1.03x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-ab11c097052757b79060-3.14.0a5+-ab11c09 | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8                   | 25.4 ms                                                                | 23.4 ms: 1.08x faster                                                     |
| regex_effbot               | 2.85 ms                                                                | 2.68 ms: 1.06x faster                                                     |
| regex_dna                  | 175 ms                                                                 | 169 ms: 1.03x faster                                                      |
| logging_silent             | 102 ns                                                                 | 99.5 ns: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 471 ms: 1.03x faster                                                      |
| gc_traversal               | 4.27 ms                                                                | 4.18 ms: 1.02x faster                                                     |
| hexiom                     | 5.75 ms                                                                | 5.63 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 484 ms: 1.02x faster                                                      |
| mdp                        | 2.46 sec                                                               | 2.41 sec: 1.02x faster                                                    |
| subparsers                 | 21.9 ms                                                                | 21.5 ms: 1.02x faster                                                     |
| async_tree_io_tg           | 603 ms                                                                 | 593 ms: 1.02x faster                                                      |
| async_tree_io              | 604 ms                                                                 | 594 ms: 1.02x faster                                                      |
| async_tree_memoization_tg  | 309 ms                                                                 | 304 ms: 1.02x faster                                                      |
| async_tree_none            | 261 ms                                                                 | 258 ms: 1.02x faster                                                      |
| pycparser                  | 1.11 sec                                                               | 1.10 sec: 1.01x faster                                                    |
| mako                       | 11.4 ms                                                                | 11.3 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.38 sec                                                               | 1.37 sec: 1.01x faster                                                    |
| async_tree_none_tg         | 254 ms                                                                 | 251 ms: 1.01x faster                                                      |
| async_generators           | 323 ms                                                                 | 320 ms: 1.01x faster                                                      |
| typing_runtime_protocols   | 153 us                                                                 | 152 us: 1.01x faster                                                      |
| deepcopy                   | 248 us                                                                 | 246 us: 1.01x faster                                                      |
| async_tree_memoization     | 314 ms                                                                 | 312 ms: 1.01x faster                                                      |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                      |
| pidigits                   | 187 ms                                                                 | 186 ms: 1.00x faster                                                      |
| richards                   | 42.0 ms                                                                | 41.9 ms: 1.00x faster                                                     |
| sqlalchemy_declarative     | 126 ms                                                                 | 126 ms: 1.00x faster                                                      |
| unpickle_pure_python       | 209 us                                                                 | 208 us: 1.00x faster                                                      |
| python_startup             | 14.8 ms                                                                | 14.8 ms: 1.00x faster                                                     |
| python_startup_no_site     | 7.54 ms                                                                | 7.53 ms: 1.00x faster                                                     |
| richards_super             | 47.7 ms                                                                | 47.9 ms: 1.00x slower                                                     |
| many_optionals             | 1.01 ms                                                                | 1.01 ms: 1.00x slower                                                     |
| comprehensions             | 15.9 us                                                                | 16.0 us: 1.01x slower                                                     |
| scimark_sor                | 112 ms                                                                 | 112 ms: 1.01x slower                                                      |
| go                         | 111 ms                                                                 | 111 ms: 1.01x slower                                                      |
| raytrace                   | 255 ms                                                                 | 256 ms: 1.01x slower                                                      |
| dulwich_log                | 74.8 ms                                                                | 75.2 ms: 1.01x slower                                                     |
| create_gc_cycles           | 1.81 ms                                                                | 1.83 ms: 1.01x slower                                                     |
| pickle_pure_python         | 305 us                                                                 | 307 us: 1.01x slower                                                      |
| sqlglot_transpile          | 1.52 ms                                                                | 1.53 ms: 1.01x slower                                                     |
| scimark_monte_carlo        | 63.7 ms                                                                | 64.1 ms: 1.01x slower                                                     |
| nqueens                    | 74.9 ms                                                                | 75.4 ms: 1.01x slower                                                     |
| sqlglot_parse              | 1.23 ms                                                                | 1.24 ms: 1.01x slower                                                     |
| telco                      | 7.22 ms                                                                | 7.27 ms: 1.01x slower                                                     |
| sympy_sum                  | 150 ms                                                                 | 151 ms: 1.01x slower                                                      |
| sqlglot_optimize           | 50.5 ms                                                                | 50.9 ms: 1.01x slower                                                     |
| xml_etree_process          | 57.0 ms                                                                | 57.5 ms: 1.01x slower                                                     |
| sympy_str                  | 266 ms                                                                 | 268 ms: 1.01x slower                                                      |
| 2to3                       | 248 ms                                                                 | 250 ms: 1.01x slower                                                      |
| generators                 | 27.2 ms                                                                | 27.5 ms: 1.01x slower                                                     |
| json_loads                 | 28.3 us                                                                | 28.6 us: 1.01x slower                                                     |
| bpe_tokeniser              | 4.12 sec                                                               | 4.17 sec: 1.01x slower                                                    |
| scimark_lu                 | 113 ms                                                                 | 114 ms: 1.01x slower                                                      |
| sqlglot_normalize          | 100.0 ms                                                               | 101 ms: 1.01x slower                                                      |
| genshi_xml                 | 47.0 ms                                                                | 47.5 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                     |
| sqlite_synth               | 2.16 us                                                                | 2.18 us: 1.01x slower                                                     |
| tomli_loads                | 1.85 sec                                                               | 1.88 sec: 1.01x slower                                                    |
| regex_compile              | 123 ms                                                                 | 126 ms: 1.02x slower                                                      |
| crypto_pyaes               | 65.7 ms                                                                | 67.2 ms: 1.02x slower                                                     |
| json_dumps                 | 10.9 ms                                                                | 11.1 ms: 1.02x slower                                                     |
| chaos                      | 54.1 ms                                                                | 55.3 ms: 1.02x slower                                                     |
| scimark_fft                | 322 ms                                                                 | 330 ms: 1.02x slower                                                      |
| django_template            | 32.7 ms                                                                | 33.6 ms: 1.03x slower                                                     |
| fannkuch                   | 363 ms                                                                 | 372 ms: 1.03x slower                                                      |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 4.44 ms: 1.03x slower                                                     |
| genshi_text                | 20.1 ms                                                                | 20.7 ms: 1.03x slower                                                     |
| pyflate                    | 395 ms                                                                 | 409 ms: 1.04x slower                                                      |
| spectral_norm              | 85.8 ms                                                                | 89.4 ms: 1.04x slower                                                     |
| coroutines                 | 21.2 ms                                                                | 22.3 ms: 1.05x slower                                                     |
| nbody                      | 85.6 ms                                                                | 93.2 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (25): connected_components, pprint_safe_repr, json, float, shortest_path, meteor_contest, pathlib, asyncio_websockets, bench_mp_pool, docutils, bench_thread_pool, logging_format, sympy_expand, thrift, deepcopy_memo, sphinx, k_core, deltablue, sqlalchemy_imperative, coverage, xml_etree_iterparse, xml_etree_generate, deepcopy_reduce, logging_simple, pylint

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 86.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x