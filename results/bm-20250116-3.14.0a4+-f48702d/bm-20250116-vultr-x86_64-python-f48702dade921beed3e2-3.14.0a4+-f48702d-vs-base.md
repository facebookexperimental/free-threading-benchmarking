# Results vs. base

- fork: python
- ref: f48702dade921beed3e2
- machine: linux-x86_64
- commit hash: f48702d
- commit date: 2025-01-16
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 316 ms                                                                 | 320 ms: 1.01x slower                                                   |
| coroutines       | 21.1 ms                                                                | 22.1 ms: 1.05x slower                                                  |
| Geometric mean   | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (9): async_tree_io, async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 87.9 ms                                                                | 88.6 ms: 1.01x slower                                                  |
| float          | 70.5 ms                                                                | 71.4 ms: 1.01x slower                                                  |
| pidigits       | 200 ms                                                                 | 203 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                  |
| regex_dna      | 170 ms                                                                 | 170 ms: 1.00x faster                                                   |
| regex_v8       | 24.1 ms                                                                | 24.4 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 311 us                                                                 | 313 us: 1.01x slower                                                   |
| unpickle_pure_python | 212 us                                                                 | 214 us: 1.01x slower                                                   |
| xml_etree_iterparse  | 90.4 ms                                                                | 91.1 ms: 1.01x slower                                                  |
| json_loads           | 27.4 us                                                                | 27.7 us: 1.01x slower                                                  |
| json_dumps           | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                  |
| xml_etree_generate   | 82.9 ms                                                                | 85.2 ms: 1.03x slower                                                  |
| xml_etree_process    | 58.1 ms                                                                | 59.9 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 14.7 ms: 1.00x slower                                                  |
| python_startup_no_site | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                  |
| django_template | 35.2 ms                                                                | 35.4 ms: 1.01x slower                                                  |
| genshi_text     | 20.6 ms                                                                | 21.2 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                 | 42.2 ms                                                                | 41.3 ms: 1.02x faster                                                  |
| telco                    | 7.27 ms                                                                | 7.13 ms: 1.02x faster                                                  |
| regex_effbot             | 2.81 ms                                                                | 2.76 ms: 1.02x faster                                                  |
| logging_simple           | 6.21 us                                                                | 6.11 us: 1.02x faster                                                  |
| richards_super           | 48.2 ms                                                                | 47.5 ms: 1.02x faster                                                  |
| pyflate                  | 416 ms                                                                 | 411 ms: 1.01x faster                                                   |
| meteor_contest           | 99.0 ms                                                                | 98.2 ms: 1.01x faster                                                  |
| comprehensions           | 16.9 us                                                                | 16.7 us: 1.01x faster                                                  |
| many_optionals           | 1.03 ms                                                                | 1.02 ms: 1.00x faster                                                  |
| regex_dna                | 170 ms                                                                 | 170 ms: 1.00x faster                                                   |
| python_startup           | 14.7 ms                                                                | 14.7 ms: 1.00x slower                                                  |
| sympy_integrate          | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                  |
| mako                     | 11.6 ms                                                                | 11.6 ms: 1.00x slower                                                  |
| go                       | 113 ms                                                                 | 114 ms: 1.00x slower                                                   |
| scimark_sor              | 114 ms                                                                 | 114 ms: 1.00x slower                                                   |
| python_startup_no_site   | 7.46 ms                                                                | 7.49 ms: 1.00x slower                                                  |
| django_template          | 35.2 ms                                                                | 35.4 ms: 1.01x slower                                                  |
| coverage                 | 78.4 ms                                                                | 78.8 ms: 1.01x slower                                                  |
| hexiom                   | 5.71 ms                                                                | 5.74 ms: 1.01x slower                                                  |
| pickle_pure_python       | 311 us                                                                 | 313 us: 1.01x slower                                                   |
| crypto_pyaes             | 66.3 ms                                                                | 66.7 ms: 1.01x slower                                                  |
| unpickle_pure_python     | 212 us                                                                 | 214 us: 1.01x slower                                                   |
| docutils                 | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                 |
| sympy_str                | 272 ms                                                                 | 274 ms: 1.01x slower                                                   |
| pprint_safe_repr         | 691 ms                                                                 | 696 ms: 1.01x slower                                                   |
| mdp                      | 2.45 sec                                                               | 2.47 sec: 1.01x slower                                                 |
| chaos                    | 54.2 ms                                                                | 54.6 ms: 1.01x slower                                                  |
| scimark_monte_carlo      | 61.9 ms                                                                | 62.4 ms: 1.01x slower                                                  |
| xml_etree_iterparse      | 90.4 ms                                                                | 91.1 ms: 1.01x slower                                                  |
| pprint_pformat           | 1.41 sec                                                               | 1.42 sec: 1.01x slower                                                 |
| sqlglot_transpile        | 1.54 ms                                                                | 1.55 ms: 1.01x slower                                                  |
| json_loads               | 27.4 us                                                                | 27.7 us: 1.01x slower                                                  |
| nbody                    | 87.9 ms                                                                | 88.6 ms: 1.01x slower                                                  |
| create_gc_cycles         | 1.84 ms                                                                | 1.86 ms: 1.01x slower                                                  |
| shortest_path            | 428 ms                                                                 | 432 ms: 1.01x slower                                                   |
| sqlglot_parse            | 1.24 ms                                                                | 1.26 ms: 1.01x slower                                                  |
| scimark_lu               | 110 ms                                                                 | 111 ms: 1.01x slower                                                   |
| connected_components     | 387 ms                                                                 | 391 ms: 1.01x slower                                                   |
| regex_v8                 | 24.1 ms                                                                | 24.4 ms: 1.01x slower                                                  |
| deepcopy_reduce          | 2.59 us                                                                | 2.62 us: 1.01x slower                                                  |
| async_generators         | 316 ms                                                                 | 320 ms: 1.01x slower                                                   |
| float                    | 70.5 ms                                                                | 71.4 ms: 1.01x slower                                                  |
| json                     | 4.92 ms                                                                | 4.99 ms: 1.01x slower                                                  |
| bpe_tokeniser            | 4.16 sec                                                               | 4.23 sec: 1.02x slower                                                 |
| sqlglot_optimize         | 52.0 ms                                                                | 52.8 ms: 1.02x slower                                                  |
| nqueens                  | 77.5 ms                                                                | 78.7 ms: 1.02x slower                                                  |
| pidigits                 | 200 ms                                                                 | 203 ms: 1.02x slower                                                   |
| typing_runtime_protocols | 155 us                                                                 | 158 us: 1.02x slower                                                   |
| json_dumps               | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                  |
| deepcopy                 | 255 us                                                                 | 260 us: 1.02x slower                                                   |
| deepcopy_memo            | 29.5 us                                                                | 30.1 us: 1.02x slower                                                  |
| logging_silent           | 102 ns                                                                 | 105 ns: 1.02x slower                                                   |
| genshi_text              | 20.6 ms                                                                | 21.2 ms: 1.03x slower                                                  |
| xml_etree_generate       | 82.9 ms                                                                | 85.2 ms: 1.03x slower                                                  |
| xml_etree_process        | 58.1 ms                                                                | 59.9 ms: 1.03x slower                                                  |
| fannkuch                 | 358 ms                                                                 | 369 ms: 1.03x slower                                                   |
| sqlglot_normalize        | 102 ms                                                                 | 106 ms: 1.03x slower                                                   |
| gc_traversal             | 4.28 ms                                                                | 4.43 ms: 1.04x slower                                                  |
| spectral_norm            | 89.3 ms                                                                | 92.6 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult  | 4.16 ms                                                                | 4.32 ms: 1.04x slower                                                  |
| coroutines               | 21.1 ms                                                                | 22.1 ms: 1.05x slower                                                  |
| generators               | 27.0 ms                                                                | 28.4 ms: 1.05x slower                                                  |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (33): async_tree_io, logging_format, sqlalchemy_imperative, sympy_sum, deltablue, pycparser, sympy_expand, async_tree_none_tg, bench_mp_pool, scimark_fft, asyncio_websockets, bench_thread_pool, raytrace, sqlite_synth, xml_etree_parse, async_tree_memoization_tg, 2to3, tomli_loads, sqlalchemy_declarative, async_tree_none, dulwich_log, subparsers, pylint, genshi_xml, async_tree_memoization, pathlib, async_tree_cpu_io_mixed, sphinx, regex_compile, thrift, async_tree_cpu_io_mixed_tg, k_core, async_tree_io_tg

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x