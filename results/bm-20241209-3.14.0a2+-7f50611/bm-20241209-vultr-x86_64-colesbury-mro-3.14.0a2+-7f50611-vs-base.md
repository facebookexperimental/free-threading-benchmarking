# Results vs. base

- fork: colesbury
- ref: mro
- machine: linux-x86_64
- commit hash: 7f50611
- commit date: 2024-12-09
- overall geometric mean: 1.009x slower
- HPT reliability: 95.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 259 ms: 1.01x slower                                     |
| docutils       | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_generators           | 362 ms                                                                 | 364 ms: 1.01x slower                                     |
| coroutines                 | 21.8 ms                                                                | 22.6 ms: 1.03x slower                                    |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 604 ms: 1.20x slower                                     |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 600 ms: 1.20x slower                                     |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                             |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none_tg, asyncio_websockets, async_tree_none, async_tree_memoization_tg, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 95.3 ms                                                                | 93.0 ms: 1.02x faster                                    |
| pidigits       | 186 ms                                                                 | 223 ms: 1.19x slower                                     |
| Geometric mean | (ref)                                                                  | 1.05x slower                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 172 ms: 1.05x faster                                     |
| regex_effbot   | 2.78 ms                                                                | 2.76 ms: 1.01x faster                                    |
| regex_compile  | 129 ms                                                                 | 130 ms: 1.01x slower                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| json_loads           | 25.2 us                                                                | 24.9 us: 1.01x faster                                    |
| xml_etree_generate   | 85.7 ms                                                                | 85.2 ms: 1.01x faster                                    |
| unpickle_pure_python | 217 us                                                                 | 216 us: 1.01x faster                                     |
| json_dumps           | 11.5 ms                                                                | 11.5 ms: 1.00x faster                                    |
| xml_etree_parse      | 127 ms                                                                 | 128 ms: 1.01x slower                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                             |

Benchmark hidden because not significant (4): tomli_loads, xml_etree_iterparse, xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.47 ms                                                                | 7.58 ms: 1.01x slower                                    |
| python_startup         | 14.6 ms                                                                | 14.8 ms: 1.02x slower                                    |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_text    | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                    |
| genshi_xml     | 51.0 ms                                                                | 50.3 ms: 1.02x faster                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                             |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f | bm-20241209-vultr-x86_64-colesbury-mro-3.14.0a2+-7f50611 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna                  | 180 ms                                                                 | 172 ms: 1.05x faster                                     |
| json                       | 4.78 ms                                                                | 4.58 ms: 1.04x faster                                    |
| nbody                      | 95.3 ms                                                                | 93.0 ms: 1.02x faster                                    |
| meteor_contest             | 102 ms                                                                 | 99.6 ms: 1.02x faster                                    |
| logging_silent             | 110 ns                                                                 | 108 ns: 1.02x faster                                     |
| genshi_text                | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                    |
| nqueens                    | 80.0 ms                                                                | 78.6 ms: 1.02x faster                                    |
| comprehensions             | 17.6 us                                                                | 17.3 us: 1.02x faster                                    |
| fannkuch                   | 381 ms                                                                 | 376 ms: 1.02x faster                                     |
| genshi_xml                 | 51.0 ms                                                                | 50.3 ms: 1.02x faster                                    |
| hexiom                     | 6.03 ms                                                                | 5.93 ms: 1.02x faster                                    |
| sympy_integrate            | 20.0 ms                                                                | 19.8 ms: 1.01x faster                                    |
| docutils                   | 2.56 sec                                                               | 2.53 sec: 1.01x faster                                   |
| sqlglot_normalize          | 107 ms                                                                 | 106 ms: 1.01x faster                                     |
| json_loads                 | 25.2 us                                                                | 24.9 us: 1.01x faster                                    |
| bpe_tokeniser              | 4.37 sec                                                               | 4.33 sec: 1.01x faster                                   |
| sqlglot_optimize           | 53.7 ms                                                                | 53.4 ms: 1.01x faster                                    |
| regex_effbot               | 2.78 ms                                                                | 2.76 ms: 1.01x faster                                    |
| xml_etree_generate         | 85.7 ms                                                                | 85.2 ms: 1.01x faster                                    |
| unpickle_pure_python       | 217 us                                                                 | 216 us: 1.01x faster                                     |
| json_dumps                 | 11.5 ms                                                                | 11.5 ms: 1.00x faster                                    |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.00x faster                                     |
| chaos                      | 58.7 ms                                                                | 58.5 ms: 1.00x faster                                    |
| raytrace                   | 267 ms                                                                 | 266 ms: 1.00x faster                                     |
| sqlglot_parse              | 1.29 ms                                                                | 1.30 ms: 1.00x slower                                    |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                    |
| many_optionals             | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                    |
| pyflate                    | 449 ms                                                                 | 451 ms: 1.00x slower                                     |
| pprint_safe_repr           | 721 ms                                                                 | 725 ms: 1.00x slower                                     |
| xml_etree_parse            | 127 ms                                                                 | 128 ms: 1.01x slower                                     |
| 2to3                       | 258 ms                                                                 | 259 ms: 1.01x slower                                     |
| shortest_path              | 444 ms                                                                 | 446 ms: 1.01x slower                                     |
| regex_compile              | 129 ms                                                                 | 130 ms: 1.01x slower                                     |
| scimark_monte_carlo        | 65.7 ms                                                                | 66.2 ms: 1.01x slower                                    |
| deepcopy                   | 262 us                                                                 | 264 us: 1.01x slower                                     |
| deepcopy_memo              | 30.0 us                                                                | 30.2 us: 1.01x slower                                    |
| async_generators           | 362 ms                                                                 | 364 ms: 1.01x slower                                     |
| thrift                     | 737 us                                                                 | 743 us: 1.01x slower                                     |
| sympy_expand               | 460 ms                                                                 | 465 ms: 1.01x slower                                     |
| dulwich_log                | 75.2 ms                                                                | 76.0 ms: 1.01x slower                                    |
| pprint_pformat             | 1.47 sec                                                               | 1.49 sec: 1.01x slower                                   |
| pathlib                    | 18.2 ms                                                                | 18.4 ms: 1.01x slower                                    |
| typing_runtime_protocols   | 157 us                                                                 | 159 us: 1.01x slower                                     |
| scimark_fft                | 334 ms                                                                 | 338 ms: 1.01x slower                                     |
| pycparser                  | 1.11 sec                                                               | 1.13 sec: 1.01x slower                                   |
| generators                 | 29.0 ms                                                                | 29.4 ms: 1.01x slower                                    |
| python_startup_no_site     | 7.47 ms                                                                | 7.58 ms: 1.01x slower                                    |
| scimark_lu                 | 113 ms                                                                 | 115 ms: 1.02x slower                                     |
| crypto_pyaes               | 66.4 ms                                                                | 67.5 ms: 1.02x slower                                    |
| python_startup             | 14.6 ms                                                                | 14.8 ms: 1.02x slower                                    |
| go                         | 120 ms                                                                 | 122 ms: 1.02x slower                                     |
| scimark_sparse_mat_mult    | 4.52 ms                                                                | 4.60 ms: 1.02x slower                                    |
| richards                   | 45.7 ms                                                                | 46.6 ms: 1.02x slower                                    |
| gc_traversal               | 4.24 ms                                                                | 4.33 ms: 1.02x slower                                    |
| richards_super             | 52.1 ms                                                                | 53.3 ms: 1.02x slower                                    |
| logging_simple             | 6.02 us                                                                | 6.16 us: 1.02x slower                                    |
| spectral_norm              | 107 ms                                                                 | 110 ms: 1.03x slower                                     |
| logging_format             | 6.78 us                                                                | 6.97 us: 1.03x slower                                    |
| coroutines                 | 21.8 ms                                                                | 22.6 ms: 1.03x slower                                    |
| create_gc_cycles           | 1.70 ms                                                                | 1.77 ms: 1.05x slower                                    |
| mdp                        | 2.33 sec                                                               | 2.52 sec: 1.08x slower                                   |
| pidigits                   | 186 ms                                                                 | 223 ms: 1.19x slower                                     |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 604 ms: 1.20x slower                                     |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 600 ms: 1.20x slower                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                             |

Benchmark hidden because not significant (28): k_core, telco, sphinx, sqlite_synth, tomli_loads, pylint, async_tree_io_tg, async_tree_none_tg, xml_etree_iterparse, deepcopy_reduce, sqlglot_transpile, xml_etree_process, scimark_sor, sympy_str, pickle_pure_python, asyncio_websockets, bench_mp_pool, mako, async_tree_none, float, async_tree_memoization_tg, connected_components, subparsers, regex_v8, deltablue, async_tree_io, django_template, async_tree_memoization
Ignored benchmarks (3) of results/bm-20241206-3.14.0a2+-5b6635f/bm-20241206-vultr-x86_64-python-5b6635f772d187d6049a-3.14.0a2+-5b6635f.json: coverage, sqlalchemy_declarative, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 95.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x