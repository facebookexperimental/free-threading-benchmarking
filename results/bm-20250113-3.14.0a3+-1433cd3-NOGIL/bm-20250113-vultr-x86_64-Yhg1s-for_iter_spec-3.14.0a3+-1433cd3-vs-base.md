# Results vs. base

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 1433cd3
- commit date: 2025-01-13
- overall geometric mean: 1.004x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 348 ms                                                                 | 343 ms: 1.02x faster                                           |
| html5lib       | 91.2 ms                                                                | 88.7 ms: 1.03x faster                                          |
| sphinx         | 1.17 sec                                                               | 1.15 sec: 1.01x faster                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                   |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg        | 319 ms                                                                 | 314 ms: 1.01x faster                                           |
| async_tree_memoization_tg | 401 ms                                                                 | 395 ms: 1.01x faster                                           |
| async_tree_io_tg          | 740 ms                                                                 | 733 ms: 1.01x faster                                           |
| coroutines                | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                          |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io, async_generators, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 182 ms: 1.01x faster                                           |
| float          | 107 ms                                                                 | 107 ms: 1.01x slower                                           |
| nbody          | 128 ms                                                                 | 130 ms: 1.01x slower                                           |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 2.95 ms                                                                | 2.69 ms: 1.09x faster                                          |
| regex_v8       | 25.4 ms                                                                | 23.8 ms: 1.07x faster                                          |
| regex_compile  | 167 ms                                                                 | 166 ms: 1.00x faster                                           |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                   |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| unpickle_pure_python | 328 us                                                                 | 322 us: 1.02x faster                                           |
| pickle_pure_python   | 498 us                                                                 | 492 us: 1.01x faster                                           |
| json_dumps           | 14.0 ms                                                                | 13.9 ms: 1.01x faster                                          |
| xml_etree_process    | 74.2 ms                                                                | 73.9 ms: 1.00x faster                                          |
| xml_etree_generate   | 98.6 ms                                                                | 98.2 ms: 1.00x faster                                          |
| xml_etree_iterparse  | 89.4 ms                                                                | 89.8 ms: 1.00x slower                                          |
| tomli_loads          | 2.33 sec                                                               | 2.34 sec: 1.01x slower                                         |
| json_loads           | 28.6 us                                                                | 28.8 us: 1.01x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                   |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.7 ms: 1.00x faster                                          |
| python_startup_no_site | 9.83 ms                                                                | 9.80 ms: 1.00x faster                                          |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 63.3 ms                                                                | 60.2 ms: 1.05x faster                                          |
| genshi_text     | 30.7 ms                                                                | 29.4 ms: 1.04x faster                                          |
| mako            | 17.0 ms                                                                | 17.2 ms: 1.01x slower                                          |
| django_template | 49.2 ms                                                                | 50.1 ms: 1.02x slower                                          |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                   |

All benchmarks:
===============

| Benchmark                 | bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3+-7dc41ad | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot              | 2.95 ms                                                                | 2.69 ms: 1.09x faster                                          |
| regex_v8                  | 25.4 ms                                                                | 23.8 ms: 1.07x faster                                          |
| gc_traversal              | 3.53 ms                                                                | 3.30 ms: 1.07x faster                                          |
| genshi_xml                | 63.3 ms                                                                | 60.2 ms: 1.05x faster                                          |
| genshi_text               | 30.7 ms                                                                | 29.4 ms: 1.04x faster                                          |
| generators                | 38.8 ms                                                                | 37.4 ms: 1.04x faster                                          |
| richards                  | 67.9 ms                                                                | 65.5 ms: 1.04x faster                                          |
| pprint_safe_repr          | 965 ms                                                                 | 936 ms: 1.03x faster                                           |
| logging_silent            | 187 ns                                                                 | 182 ns: 1.03x faster                                           |
| html5lib                  | 91.2 ms                                                                | 88.7 ms: 1.03x faster                                          |
| pprint_pformat            | 2.00 sec                                                               | 1.95 sec: 1.03x faster                                         |
| pycparser                 | 1.37 sec                                                               | 1.33 sec: 1.02x faster                                         |
| deepcopy_reduce           | 3.45 us                                                                | 3.38 us: 1.02x faster                                          |
| unpickle_pure_python      | 328 us                                                                 | 322 us: 1.02x faster                                           |
| telco                     | 8.78 ms                                                                | 8.61 ms: 1.02x faster                                          |
| go                        | 235 ms                                                                 | 231 ms: 1.02x faster                                           |
| crypto_pyaes              | 90.8 ms                                                                | 89.2 ms: 1.02x faster                                          |
| create_gc_cycles          | 1.85 ms                                                                | 1.82 ms: 1.02x faster                                          |
| 2to3                      | 348 ms                                                                 | 343 ms: 1.02x faster                                           |
| scimark_monte_carlo       | 104 ms                                                                 | 102 ms: 1.01x faster                                           |
| async_tree_none_tg        | 319 ms                                                                 | 314 ms: 1.01x faster                                           |
| async_tree_memoization_tg | 401 ms                                                                 | 395 ms: 1.01x faster                                           |
| sphinx                    | 1.17 sec                                                               | 1.15 sec: 1.01x faster                                         |
| pidigits                  | 184 ms                                                                 | 182 ms: 1.01x faster                                           |
| pickle_pure_python        | 498 us                                                                 | 492 us: 1.01x faster                                           |
| async_tree_io_tg          | 740 ms                                                                 | 733 ms: 1.01x faster                                           |
| sqlglot_normalize         | 133 ms                                                                 | 132 ms: 1.01x faster                                           |
| deepcopy_memo             | 41.3 us                                                                | 40.9 us: 1.01x faster                                          |
| k_core                    | 2.35 sec                                                               | 2.34 sec: 1.01x faster                                         |
| pathlib                   | 19.5 ms                                                                | 19.4 ms: 1.01x faster                                          |
| json_dumps                | 14.0 ms                                                                | 13.9 ms: 1.01x faster                                          |
| hexiom                    | 9.34 ms                                                                | 9.28 ms: 1.01x faster                                          |
| bench_thread_pool         | 3.37 ms                                                                | 3.36 ms: 1.01x faster                                          |
| raytrace                  | 492 ms                                                                 | 490 ms: 1.01x faster                                           |
| xml_etree_process         | 74.2 ms                                                                | 73.9 ms: 1.00x faster                                          |
| pyflate                   | 640 ms                                                                 | 637 ms: 1.00x faster                                           |
| xml_etree_generate        | 98.6 ms                                                                | 98.2 ms: 1.00x faster                                          |
| scimark_sor               | 202 ms                                                                 | 202 ms: 1.00x faster                                           |
| bpe_tokeniser             | 4.99 sec                                                               | 4.97 sec: 1.00x faster                                         |
| python_startup            | 15.7 ms                                                                | 15.7 ms: 1.00x faster                                          |
| python_startup_no_site    | 9.83 ms                                                                | 9.80 ms: 1.00x faster                                          |
| regex_compile             | 167 ms                                                                 | 166 ms: 1.00x faster                                           |
| xml_etree_iterparse       | 89.4 ms                                                                | 89.8 ms: 1.00x slower                                          |
| sqlglot_parse             | 2.31 ms                                                                | 2.32 ms: 1.00x slower                                          |
| deepcopy                  | 324 us                                                                 | 325 us: 1.00x slower                                           |
| tomli_loads               | 2.33 sec                                                               | 2.34 sec: 1.01x slower                                         |
| json_loads                | 28.6 us                                                                | 28.8 us: 1.01x slower                                          |
| fannkuch                  | 482 ms                                                                 | 486 ms: 1.01x slower                                           |
| float                     | 107 ms                                                                 | 107 ms: 1.01x slower                                           |
| mako                      | 17.0 ms                                                                | 17.2 ms: 1.01x slower                                          |
| shortest_path             | 548 ms                                                                 | 554 ms: 1.01x slower                                           |
| logging_format            | 10.0 us                                                                | 10.1 us: 1.01x slower                                          |
| typing_runtime_protocols  | 203 us                                                                 | 205 us: 1.01x slower                                           |
| connected_components      | 496 ms                                                                 | 502 ms: 1.01x slower                                           |
| json                      | 5.05 ms                                                                | 5.11 ms: 1.01x slower                                          |
| nqueens                   | 95.5 ms                                                                | 96.6 ms: 1.01x slower                                          |
| nbody                     | 128 ms                                                                 | 130 ms: 1.01x slower                                           |
| scimark_fft               | 374 ms                                                                 | 380 ms: 1.02x slower                                           |
| richards_super            | 75.3 ms                                                                | 76.5 ms: 1.02x slower                                          |
| subparsers                | 28.4 ms                                                                | 28.9 ms: 1.02x slower                                          |
| django_template           | 49.2 ms                                                                | 50.1 ms: 1.02x slower                                          |
| comprehensions            | 27.3 us                                                                | 27.9 us: 1.02x slower                                          |
| coroutines                | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                          |
| spectral_norm             | 109 ms                                                                 | 112 ms: 1.03x slower                                           |
| scimark_sparse_mat_mult   | 5.22 ms                                                                | 5.41 ms: 1.04x slower                                          |
| mdp                       | 2.67 sec                                                               | 2.86 sec: 1.07x slower                                         |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                   |

Benchmark hidden because not significant (30): pylint, async_tree_none, docutils, bench_mp_pool, sqlite_synth, async_tree_io, sqlglot_optimize, deltablue, chaos, sympy_expand, scimark_lu, dulwich_log, sqlalchemy_imperative, sympy_integrate, async_generators, async_tree_cpu_io_mixed, sqlalchemy_declarative, sympy_sum, regex_dna, async_tree_memoization, async_tree_cpu_io_mixed_tg, asyncio_websockets, thrift, coverage, sympy_str, xml_etree_parse, many_optionals, sqlglot_transpile, logging_simple, meteor_contest

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.69% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x