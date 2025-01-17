# Results vs. base

- fork: mpage
- ref: aa_test_1
- machine: linux-x86_64
- commit hash: de82556
- commit date: 2025-01-16
- overall geometric mean: 1.000x faster
- HPT reliability: 61.06%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg | 300 ms                                                                 | 303 ms: 1.01x slower                                       |
| async_generators          | 320 ms                                                                 | 326 ms: 1.02x slower                                       |
| Geometric mean            | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (9): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, asyncio_websockets, async_tree_io_tg, async_tree_none_tg, coroutines, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 203 ms                                                                 | 192 ms: 1.06x faster                                       |
| nbody          | 88.6 ms                                                                | 86.3 ms: 1.03x faster                                      |
| float          | 71.4 ms                                                                | 72.5 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                                  | 1.02x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 2.76 ms                                                                | 2.73 ms: 1.01x faster                                      |
| regex_dna      | 170 ms                                                                 | 171 ms: 1.01x slower                                       |
| regex_v8       | 24.4 ms                                                                | 25.0 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| json_dumps          | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                      |
| xml_etree_generate  | 85.2 ms                                                                | 83.9 ms: 1.02x faster                                      |
| pickle_pure_python  | 313 us                                                                 | 309 us: 1.01x faster                                       |
| tomli_loads         | 1.89 sec                                                               | 1.87 sec: 1.01x faster                                     |
| xml_etree_iterparse | 91.1 ms                                                                | 90.6 ms: 1.01x faster                                      |
| xml_etree_process   | 59.9 ms                                                                | 59.6 ms: 1.00x faster                                      |
| json_loads          | 27.7 us                                                                | 27.8 us: 1.00x slower                                      |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                               |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.49 ms                                                                | 7.45 ms: 1.01x faster                                      |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 21.2 ms                                                                | 21.0 ms: 1.01x faster                                      |
| mako            | 11.6 ms                                                                | 11.6 ms: 1.00x faster                                      |
| django_template | 35.4 ms                                                                | 36.1 ms: 1.02x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4+-f48702d | bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4+-de82556 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mdp                       | 2.47 sec                                                               | 2.32 sec: 1.06x faster                                     |
| pidigits                  | 203 ms                                                                 | 192 ms: 1.06x faster                                       |
| nbody                     | 88.6 ms                                                                | 86.3 ms: 1.03x faster                                      |
| spectral_norm             | 92.6 ms                                                                | 90.8 ms: 1.02x faster                                      |
| json_dumps                | 11.6 ms                                                                | 11.4 ms: 1.02x faster                                      |
| xml_etree_generate        | 85.2 ms                                                                | 83.9 ms: 1.02x faster                                      |
| typing_runtime_protocols  | 158 us                                                                 | 155 us: 1.02x faster                                       |
| gc_traversal              | 4.43 ms                                                                | 4.37 ms: 1.02x faster                                      |
| pickle_pure_python        | 313 us                                                                 | 309 us: 1.01x faster                                       |
| deepcopy_reduce           | 2.62 us                                                                | 2.59 us: 1.01x faster                                      |
| genshi_text               | 21.2 ms                                                                | 21.0 ms: 1.01x faster                                      |
| deepcopy                  | 260 us                                                                 | 257 us: 1.01x faster                                       |
| tomli_loads               | 1.89 sec                                                               | 1.87 sec: 1.01x faster                                     |
| regex_effbot              | 2.76 ms                                                                | 2.73 ms: 1.01x faster                                      |
| sympy_str                 | 274 ms                                                                 | 271 ms: 1.01x faster                                       |
| create_gc_cycles          | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                      |
| nqueens                   | 78.7 ms                                                                | 78.0 ms: 1.01x faster                                      |
| pathlib                   | 18.1 ms                                                                | 18.0 ms: 1.01x faster                                      |
| fannkuch                  | 369 ms                                                                 | 366 ms: 1.01x faster                                       |
| thrift                    | 741 us                                                                 | 736 us: 1.01x faster                                       |
| xml_etree_iterparse       | 91.1 ms                                                                | 90.6 ms: 1.01x faster                                      |
| python_startup_no_site    | 7.49 ms                                                                | 7.45 ms: 1.01x faster                                      |
| generators                | 28.4 ms                                                                | 28.2 ms: 1.00x faster                                      |
| xml_etree_process         | 59.9 ms                                                                | 59.6 ms: 1.00x faster                                      |
| pprint_pformat            | 1.42 sec                                                               | 1.41 sec: 1.00x faster                                     |
| scimark_fft               | 311 ms                                                                 | 310 ms: 1.00x faster                                       |
| deepcopy_memo             | 30.1 us                                                                | 30.0 us: 1.00x faster                                      |
| bpe_tokeniser             | 4.23 sec                                                               | 4.21 sec: 1.00x faster                                     |
| sqlglot_optimize          | 52.8 ms                                                                | 52.6 ms: 1.00x faster                                      |
| mako                      | 11.6 ms                                                                | 11.6 ms: 1.00x faster                                      |
| sqlalchemy_declarative    | 128 ms                                                                 | 128 ms: 1.00x slower                                       |
| crypto_pyaes              | 66.7 ms                                                                | 66.9 ms: 1.00x slower                                      |
| json_loads                | 27.7 us                                                                | 27.8 us: 1.00x slower                                      |
| regex_dna                 | 170 ms                                                                 | 171 ms: 1.01x slower                                       |
| sqlglot_transpile         | 1.55 ms                                                                | 1.56 ms: 1.01x slower                                      |
| pycparser                 | 1.12 sec                                                               | 1.12 sec: 1.01x slower                                     |
| async_tree_memoization_tg | 300 ms                                                                 | 303 ms: 1.01x slower                                       |
| sqlglot_parse             | 1.26 ms                                                                | 1.26 ms: 1.01x slower                                      |
| comprehensions            | 16.7 us                                                                | 16.9 us: 1.01x slower                                      |
| logging_simple            | 6.11 us                                                                | 6.18 us: 1.01x slower                                      |
| hexiom                    | 5.74 ms                                                                | 5.81 ms: 1.01x slower                                      |
| raytrace                  | 262 ms                                                                 | 265 ms: 1.01x slower                                       |
| logging_silent            | 105 ns                                                                 | 106 ns: 1.01x slower                                       |
| float                     | 71.4 ms                                                                | 72.5 ms: 1.01x slower                                      |
| telco                     | 7.13 ms                                                                | 7.25 ms: 1.02x slower                                      |
| sqlite_synth              | 2.19 us                                                                | 2.23 us: 1.02x slower                                      |
| async_generators          | 320 ms                                                                 | 326 ms: 1.02x slower                                       |
| richards_super            | 47.5 ms                                                                | 48.4 ms: 1.02x slower                                      |
| scimark_sor               | 114 ms                                                                 | 116 ms: 1.02x slower                                       |
| django_template           | 35.4 ms                                                                | 36.1 ms: 1.02x slower                                      |
| scimark_monte_carlo       | 62.4 ms                                                                | 63.9 ms: 1.02x slower                                      |
| deltablue                 | 3.12 ms                                                                | 3.20 ms: 1.02x slower                                      |
| regex_v8                  | 24.4 ms                                                                | 25.0 ms: 1.03x slower                                      |
| richards                  | 41.3 ms                                                                | 42.4 ms: 1.03x slower                                      |
| coverage                  | 78.8 ms                                                                | 81.0 ms: 1.03x slower                                      |
| go                        | 114 ms                                                                 | 117 ms: 1.03x slower                                       |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                               |

Benchmark hidden because not significant (39): async_tree_none, async_tree_cpu_io_mixed_tg, json, xml_etree_parse, genshi_xml, unpickle_pure_python, subparsers, pprint_safe_repr, k_core, async_tree_cpu_io_mixed, sqlglot_normalize, pylint, bench_mp_pool, scimark_lu, async_tree_memoization, many_optionals, dulwich_log, sympy_expand, python_startup, sqlalchemy_imperative, asyncio_websockets, async_tree_io_tg, sympy_integrate, async_tree_none_tg, sympy_sum, coroutines, bench_thread_pool, shortest_path, pyflate, chaos, docutils, 2to3, regex_compile, meteor_contest, async_tree_io, connected_components, sphinx, logging_format, scimark_sparse_mat_mult

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 61.06% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x