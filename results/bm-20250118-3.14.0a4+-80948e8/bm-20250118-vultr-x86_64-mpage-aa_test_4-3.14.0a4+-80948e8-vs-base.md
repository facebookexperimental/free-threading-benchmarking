# Results vs. base

- fork: mpage
- ref: aa_test_4
- machine: linux-x86_64
- commit hash: 80948e8
- commit date: 2025-01-18
- overall geometric mean: 1.000x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 251 ms                                                                 | 252 ms: 1.01x slower                                       |
| docutils       | 2.55 sec                                                               | 2.57 sec: 1.01x slower                                     |
| sphinx         | 973 ms                                                                 | 988 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 557 ms                                                                 | 475 ms: 1.17x faster                                       |
| async_tree_cpu_io_mixed    | 577 ms                                                                 | 492 ms: 1.17x faster                                       |
| asyncio_websockets         | 522 ms                                                                 | 523 ms: 1.00x slower                                       |
| coroutines                 | 21.8 ms                                                                | 22.0 ms: 1.01x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (7): async_generators, async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 226 ms                                                                 | 191 ms: 1.18x faster                                       |
| Geometric mean | (ref)                                                                  | 1.06x faster                                               |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_dna      | 170 ms                                                                 | 169 ms: 1.01x faster                                       |
| regex_compile  | 125 ms                                                                 | 126 ms: 1.01x slower                                       |
| regex_v8       | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                      |
| regex_effbot   | 2.66 ms                                                                | 2.79 ms: 1.05x slower                                      |
| Geometric mean | (ref)                                                                  | 1.02x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| json_loads           | 28.3 us                                                                | 27.5 us: 1.03x faster                                      |
| json_dumps           | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                      |
| tomli_loads          | 1.89 sec                                                               | 1.89 sec: 1.00x slower                                     |
| xml_etree_iterparse  | 90.3 ms                                                                | 91.0 ms: 1.01x slower                                      |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                       |
| xml_etree_generate   | 83.6 ms                                                                | 84.3 ms: 1.01x slower                                      |
| pickle_pure_python   | 305 us                                                                 | 310 us: 1.01x slower                                       |
| xml_etree_process    | 58.6 ms                                                                | 59.5 ms: 1.02x slower                                      |
| unpickle_pure_python | 209 us                                                                 | 214 us: 1.03x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.44 ms                                                                | 7.42 ms: 1.00x faster                                      |
| python_startup         | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                      |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mako            | 11.6 ms                                                                | 11.7 ms: 1.00x slower                                      |
| django_template | 34.9 ms                                                                | 35.1 ms: 1.01x slower                                      |
| genshi_xml      | 48.1 ms                                                                | 48.6 ms: 1.01x slower                                      |
| genshi_text     | 20.7 ms                                                                | 21.1 ms: 1.02x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20250118-vultr-x86_64-python-e8092e5cdcd6707ac0b1-3.14.0a4+-e8092e5 | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits                   | 226 ms                                                                 | 191 ms: 1.18x faster                                       |
| async_tree_cpu_io_mixed_tg | 557 ms                                                                 | 475 ms: 1.17x faster                                       |
| async_tree_cpu_io_mixed    | 577 ms                                                                 | 492 ms: 1.17x faster                                       |
| json_loads                 | 28.3 us                                                                | 27.5 us: 1.03x faster                                      |
| telco                      | 7.32 ms                                                                | 7.13 ms: 1.03x faster                                      |
| crypto_pyaes               | 66.7 ms                                                                | 65.1 ms: 1.02x faster                                      |
| pyflate                    | 419 ms                                                                 | 411 ms: 1.02x faster                                       |
| scimark_sor                | 114 ms                                                                 | 112 ms: 1.02x faster                                       |
| scimark_fft                | 311 ms                                                                 | 307 ms: 1.01x faster                                       |
| json                       | 5.00 ms                                                                | 4.93 ms: 1.01x faster                                      |
| sqlglot_parse              | 1.25 ms                                                                | 1.23 ms: 1.01x faster                                      |
| json_dumps                 | 11.5 ms                                                                | 11.4 ms: 1.01x faster                                      |
| meteor_contest             | 99.5 ms                                                                | 98.6 ms: 1.01x faster                                      |
| create_gc_cycles           | 1.85 ms                                                                | 1.83 ms: 1.01x faster                                      |
| regex_dna                  | 170 ms                                                                 | 169 ms: 1.01x faster                                       |
| many_optionals             | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                      |
| sqlglot_transpile          | 1.54 ms                                                                | 1.54 ms: 1.00x faster                                      |
| python_startup_no_site     | 7.44 ms                                                                | 7.42 ms: 1.00x faster                                      |
| richards                   | 42.4 ms                                                                | 42.3 ms: 1.00x faster                                      |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x faster                                      |
| asyncio_websockets         | 522 ms                                                                 | 523 ms: 1.00x slower                                       |
| mako                       | 11.6 ms                                                                | 11.7 ms: 1.00x slower                                      |
| tomli_loads                | 1.89 sec                                                               | 1.89 sec: 1.00x slower                                     |
| bench_thread_pool          | 1.03 ms                                                                | 1.04 ms: 1.00x slower                                      |
| raytrace                   | 259 ms                                                                 | 260 ms: 1.00x slower                                       |
| 2to3                       | 251 ms                                                                 | 252 ms: 1.01x slower                                       |
| bpe_tokeniser              | 4.18 sec                                                               | 4.20 sec: 1.01x slower                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.8 ms: 1.01x slower                                      |
| sympy_expand               | 455 ms                                                                 | 457 ms: 1.01x slower                                       |
| nqueens                    | 77.4 ms                                                                | 77.9 ms: 1.01x slower                                      |
| django_template            | 34.9 ms                                                                | 35.1 ms: 1.01x slower                                      |
| sympy_sum                  | 152 ms                                                                 | 153 ms: 1.01x slower                                       |
| deepcopy_reduce            | 2.59 us                                                                | 2.60 us: 1.01x slower                                      |
| xml_etree_iterparse        | 90.3 ms                                                                | 91.0 ms: 1.01x slower                                      |
| coroutines                 | 21.8 ms                                                                | 22.0 ms: 1.01x slower                                      |
| deltablue                  | 3.09 ms                                                                | 3.11 ms: 1.01x slower                                      |
| pprint_pformat             | 1.41 sec                                                               | 1.42 sec: 1.01x slower                                     |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.01x slower                                       |
| pprint_safe_repr           | 694 ms                                                                 | 700 ms: 1.01x slower                                       |
| xml_etree_generate         | 83.6 ms                                                                | 84.3 ms: 1.01x slower                                      |
| pycparser                  | 1.10 sec                                                               | 1.11 sec: 1.01x slower                                     |
| sqlalchemy_imperative      | 19.2 ms                                                                | 19.3 ms: 1.01x slower                                      |
| scimark_lu                 | 110 ms                                                                 | 111 ms: 1.01x slower                                       |
| sympy_str                  | 270 ms                                                                 | 273 ms: 1.01x slower                                       |
| genshi_xml                 | 48.1 ms                                                                | 48.6 ms: 1.01x slower                                      |
| dulwich_log                | 74.6 ms                                                                | 75.4 ms: 1.01x slower                                      |
| richards_super             | 48.3 ms                                                                | 48.8 ms: 1.01x slower                                      |
| hexiom                     | 5.68 ms                                                                | 5.74 ms: 1.01x slower                                      |
| docutils                   | 2.55 sec                                                               | 2.57 sec: 1.01x slower                                     |
| logging_simple             | 6.10 us                                                                | 6.18 us: 1.01x slower                                      |
| regex_compile              | 125 ms                                                                 | 126 ms: 1.01x slower                                       |
| scimark_monte_carlo        | 62.5 ms                                                                | 63.3 ms: 1.01x slower                                      |
| pickle_pure_python         | 305 us                                                                 | 310 us: 1.01x slower                                       |
| shortest_path              | 427 ms                                                                 | 433 ms: 1.01x slower                                       |
| sphinx                     | 973 ms                                                                 | 988 ms: 1.01x slower                                       |
| spectral_norm              | 86.8 ms                                                                | 88.1 ms: 1.01x slower                                      |
| xml_etree_process          | 58.6 ms                                                                | 59.5 ms: 1.02x slower                                      |
| sqlglot_optimize           | 51.8 ms                                                                | 52.6 ms: 1.02x slower                                      |
| genshi_text                | 20.7 ms                                                                | 21.1 ms: 1.02x slower                                      |
| comprehensions             | 16.6 us                                                                | 16.9 us: 1.02x slower                                      |
| sqlglot_normalize          | 103 ms                                                                 | 105 ms: 1.02x slower                                       |
| gc_traversal               | 4.19 ms                                                                | 4.28 ms: 1.02x slower                                      |
| generators                 | 27.4 ms                                                                | 28.0 ms: 1.02x slower                                      |
| deepcopy_memo              | 29.4 us                                                                | 30.1 us: 1.02x slower                                      |
| logging_format             | 6.81 us                                                                | 6.99 us: 1.03x slower                                      |
| unpickle_pure_python       | 209 us                                                                 | 214 us: 1.03x slower                                       |
| deepcopy                   | 253 us                                                                 | 260 us: 1.03x slower                                       |
| thrift                     | 723 us                                                                 | 748 us: 1.03x slower                                       |
| logging_silent             | 103 ns                                                                 | 107 ns: 1.04x slower                                       |
| scimark_sparse_mat_mult    | 4.12 ms                                                                | 4.29 ms: 1.04x slower                                      |
| regex_v8                   | 23.2 ms                                                                | 24.2 ms: 1.04x slower                                      |
| regex_effbot               | 2.66 ms                                                                | 2.79 ms: 1.05x slower                                      |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (23): async_generators, nbody, chaos, async_tree_memoization_tg, async_tree_io, sqlalchemy_declarative, mdp, fannkuch, async_tree_none_tg, k_core, bench_mp_pool, async_tree_memoization, pathlib, async_tree_io_tg, go, async_tree_none, float, typing_runtime_protocols, connected_components, subparsers, pylint, sqlite_synth, coverage

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x