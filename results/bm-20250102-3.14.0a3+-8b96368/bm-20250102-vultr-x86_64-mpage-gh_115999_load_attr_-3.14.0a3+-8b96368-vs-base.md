# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.003x faster
- HPT reliability: 66.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 254 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 483 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 464 ms: 1.03x faster                                                  |
| async_tree_none            | 272 ms                                                                 | 267 ms: 1.02x faster                                                  |
| async_tree_memoization     | 327 ms                                                                 | 321 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 298 ms                                                                 | 295 ms: 1.01x faster                                                  |
| async_generators           | 355 ms                                                                 | 352 ms: 1.01x faster                                                  |
| coroutines                 | 20.8 ms                                                                | 21.0 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_io, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 184 ms: 1.04x faster                                                  |
| nbody          | 92.1 ms                                                                | 91.4 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 169 ms: 1.07x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.9 ms: 1.05x faster                                                 |
| regex_effbot   | 2.83 ms                                                                | 2.74 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle_pure_python | 211 us                                                                 | 209 us: 1.01x faster                                                  |
| xml_etree_process    | 58.0 ms                                                                | 57.6 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 90.4 ms                                                                | 90.6 ms: 1.00x slower                                                 |
| json_loads           | 25.9 us                                                                | 26.0 us: 1.00x slower                                                 |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                                  |
| tomli_loads          | 1.88 sec                                                               | 1.93 sec: 1.03x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.51 ms                                                                | 7.48 ms: 1.00x faster                                                 |
| python_startup         | 14.7 ms                                                                | 14.7 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                | 34.6 ms: 1.01x faster                                                 |
| genshi_text     | 21.1 ms                                                                | 21.0 ms: 1.00x faster                                                 |
| mako            | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna                  | 182 ms                                                                 | 169 ms: 1.07x faster                                                  |
| mdp                        | 2.44 sec                                                               | 2.32 sec: 1.05x faster                                                |
| regex_v8                   | 25.0 ms                                                                | 23.9 ms: 1.05x faster                                                 |
| pidigits                   | 192 ms                                                                 | 184 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 483 ms: 1.03x faster                                                  |
| regex_effbot               | 2.83 ms                                                                | 2.74 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 464 ms: 1.03x faster                                                  |
| gc_traversal               | 4.29 ms                                                                | 4.19 ms: 1.02x faster                                                 |
| deepcopy                   | 255 us                                                                 | 250 us: 1.02x faster                                                  |
| async_tree_none            | 272 ms                                                                 | 267 ms: 1.02x faster                                                  |
| async_tree_memoization     | 327 ms                                                                 | 321 ms: 1.02x faster                                                  |
| hexiom                     | 5.93 ms                                                                | 5.84 ms: 1.02x faster                                                 |
| coverage                   | 79.8 ms                                                                | 78.6 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                |
| subparsers                 | 22.0 ms                                                                | 21.8 ms: 1.01x faster                                                 |
| async_tree_memoization_tg  | 298 ms                                                                 | 295 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 211 us                                                                 | 209 us: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                                 | 102 ns: 1.01x faster                                                  |
| async_generators           | 355 ms                                                                 | 352 ms: 1.01x faster                                                  |
| thrift                     | 729 us                                                                 | 723 us: 1.01x faster                                                  |
| django_template            | 34.8 ms                                                                | 34.6 ms: 1.01x faster                                                 |
| create_gc_cycles           | 1.84 ms                                                                | 1.83 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 1.55 ms                                                                | 1.54 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.43 ms                                                                | 4.40 ms: 1.01x faster                                                 |
| nbody                      | 92.1 ms                                                                | 91.4 ms: 1.01x faster                                                 |
| xml_etree_process          | 58.0 ms                                                                | 57.6 ms: 1.01x faster                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 102 ms: 1.01x faster                                                  |
| sqlglot_parse              | 1.24 ms                                                                | 1.23 ms: 1.01x faster                                                 |
| bench_mp_pool              | 89.5 ms                                                                | 89.0 ms: 1.01x faster                                                 |
| nqueens                    | 78.1 ms                                                                | 77.8 ms: 1.00x faster                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 51.9 ms: 1.00x faster                                                 |
| genshi_text                | 21.1 ms                                                                | 21.0 ms: 1.00x faster                                                 |
| python_startup_no_site     | 7.51 ms                                                                | 7.48 ms: 1.00x faster                                                 |
| 2to3                       | 254 ms                                                                 | 254 ms: 1.00x faster                                                  |
| python_startup             | 14.7 ms                                                                | 14.7 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 90.4 ms                                                                | 90.6 ms: 1.00x slower                                                 |
| scimark_sor                | 113 ms                                                                 | 114 ms: 1.00x slower                                                  |
| json_loads                 | 25.9 us                                                                | 26.0 us: 1.00x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 128 ms: 1.00x slower                                                  |
| fannkuch                   | 364 ms                                                                 | 366 ms: 1.01x slower                                                  |
| bpe_tokeniser              | 4.23 sec                                                               | 4.26 sec: 1.01x slower                                                |
| crypto_pyaes               | 66.5 ms                                                                | 66.9 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 685 ms                                                                 | 689 ms: 1.01x slower                                                  |
| dulwich_log                | 74.6 ms                                                                | 75.1 ms: 1.01x slower                                                 |
| generators                 | 27.3 ms                                                                | 27.4 ms: 1.01x slower                                                 |
| connected_components       | 389 ms                                                                 | 391 ms: 1.01x slower                                                  |
| meteor_contest             | 99.3 ms                                                                | 100.0 ms: 1.01x slower                                                |
| richards                   | 41.9 ms                                                                | 42.2 ms: 1.01x slower                                                 |
| sympy_integrate            | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                 |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 1.04 ms: 1.01x slower                                                 |
| coroutines                 | 20.8 ms                                                                | 21.0 ms: 1.01x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 112 ms: 1.01x slower                                                  |
| chaos                      | 57.7 ms                                                                | 58.1 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 156 us: 1.01x slower                                                  |
| sympy_str                  | 270 ms                                                                 | 272 ms: 1.01x slower                                                  |
| pathlib                    | 18.0 ms                                                                | 18.1 ms: 1.01x slower                                                 |
| mako                       | 11.7 ms                                                                | 11.8 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.40 sec                                                               | 1.41 sec: 1.01x slower                                                |
| deltablue                  | 3.11 ms                                                                | 3.14 ms: 1.01x slower                                                 |
| deepcopy_memo              | 29.4 us                                                                | 29.8 us: 1.01x slower                                                 |
| logging_simple             | 5.94 us                                                                | 6.02 us: 1.01x slower                                                 |
| richards_super             | 48.0 ms                                                                | 48.6 ms: 1.01x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 19.3 ms: 1.02x slower                                                 |
| spectral_norm              | 93.8 ms                                                                | 96.0 ms: 1.02x slower                                                 |
| go                         | 115 ms                                                                 | 118 ms: 1.02x slower                                                  |
| tomli_loads                | 1.88 sec                                                               | 1.93 sec: 1.03x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (28): async_tree_none_tg, genshi_xml, pickle_pure_python, sqlite_synth, async_tree_io, comprehensions, raytrace, sphinx, scimark_monte_carlo, asyncio_websockets, deepcopy_reduce, docutils, logging_format, regex_compile, async_tree_io_tg, shortest_path, pyflate, k_core, json, json_dumps, sympy_sum, many_optionals, pylint, telco, float, sympy_expand, scimark_fft, xml_etree_generate

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 66.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x