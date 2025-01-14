# Results vs. base

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 0c173c9
- commit date: 2025-01-13
- overall geometric mean: 1.000x faster
- HPT reliability: 84.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 345 ms                                                                 | 341 ms: 1.01x faster                                                    |
| html5lib       | 88.3 ms                                                                | 88.8 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|--------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg | 316 ms                                                                 | 312 ms: 1.01x faster                                                    |
| async_tree_none    | 353 ms                                                                 | 351 ms: 1.01x faster                                                    |
| coroutines         | 23.1 ms                                                                | 23.7 ms: 1.03x slower                                                   |
| async_generators   | 430 ms                                                                 | 448 ms: 1.04x slower                                                    |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (7): async_tree_memoization, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| nbody          | 129 ms                                                                 | 131 ms: 1.02x slower                                                    |
| pidigits       | 197 ms                                                                 | 201 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 166 ms                                                                 | 165 ms: 1.00x faster                                                    |
| regex_effbot   | 2.69 ms                                                                | 2.75 ms: 1.02x slower                                                   |
| regex_dna      | 181 ms                                                                 | 188 ms: 1.03x slower                                                    |
| regex_v8       | 23.4 ms                                                                | 24.4 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 14.1 ms                                                                | 13.7 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 90.0 ms                                                                | 88.9 ms: 1.01x faster                                                   |
| pickle_pure_python   | 493 us                                                                 | 487 us: 1.01x faster                                                    |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                                    |
| unpickle_pure_python | 320 us                                                                 | 321 us: 1.00x slower                                                    |
| tomli_loads          | 2.32 sec                                                               | 2.37 sec: 1.02x slower                                                  |
| json_loads           | 28.6 us                                                                | 29.2 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 9.82 ms                                                                | 9.59 ms: 1.02x faster                                                   |
| python_startup         | 15.7 ms                                                                | 15.4 ms: 1.02x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.02x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 17.1 ms                                                                | 17.0 ms: 1.00x faster                                                   |
| django_template | 49.4 ms                                                                | 49.9 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3+-a1284e9 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| create_gc_cycles         | 1.84 ms                                                                | 1.36 ms: 1.35x faster                                                   |
| logging_silent           | 187 ns                                                                 | 177 ns: 1.06x faster                                                    |
| comprehensions           | 27.6 us                                                                | 26.7 us: 1.03x faster                                                   |
| richards                 | 67.2 ms                                                                | 65.0 ms: 1.03x faster                                                   |
| bench_mp_pool            | 100 ms                                                                 | 97.3 ms: 1.03x faster                                                   |
| json_dumps               | 14.1 ms                                                                | 13.7 ms: 1.03x faster                                                   |
| python_startup_no_site   | 9.82 ms                                                                | 9.59 ms: 1.02x faster                                                   |
| python_startup           | 15.7 ms                                                                | 15.4 ms: 1.02x faster                                                   |
| deltablue                | 7.29 ms                                                                | 7.17 ms: 1.02x faster                                                   |
| subparsers               | 28.6 ms                                                                | 28.1 ms: 1.02x faster                                                   |
| pprint_pformat           | 1.99 sec                                                               | 1.96 sec: 1.02x faster                                                  |
| pprint_safe_repr         | 961 ms                                                                 | 946 ms: 1.02x faster                                                    |
| raytrace                 | 495 ms                                                                 | 489 ms: 1.01x faster                                                    |
| xml_etree_iterparse      | 90.0 ms                                                                | 88.9 ms: 1.01x faster                                                   |
| pickle_pure_python       | 493 us                                                                 | 487 us: 1.01x faster                                                    |
| async_tree_none_tg       | 316 ms                                                                 | 312 ms: 1.01x faster                                                    |
| xml_etree_parse          | 130 ms                                                                 | 128 ms: 1.01x faster                                                    |
| many_optionals           | 1.24 ms                                                                | 1.22 ms: 1.01x faster                                                   |
| 2to3                     | 345 ms                                                                 | 341 ms: 1.01x faster                                                    |
| deepcopy_reduce          | 3.46 us                                                                | 3.43 us: 1.01x faster                                                   |
| deepcopy_memo            | 40.6 us                                                                | 40.2 us: 1.01x faster                                                   |
| scimark_monte_carlo      | 103 ms                                                                 | 102 ms: 1.01x faster                                                    |
| dulwich_log              | 90.4 ms                                                                | 89.6 ms: 1.01x faster                                                   |
| bpe_tokeniser            | 4.98 sec                                                               | 4.94 sec: 1.01x faster                                                  |
| connected_components     | 493 ms                                                                 | 489 ms: 1.01x faster                                                    |
| shortest_path            | 547 ms                                                                 | 543 ms: 1.01x faster                                                    |
| go                       | 231 ms                                                                 | 229 ms: 1.01x faster                                                    |
| async_tree_none          | 353 ms                                                                 | 351 ms: 1.01x faster                                                    |
| sqlalchemy_declarative   | 183 ms                                                                 | 182 ms: 1.01x faster                                                    |
| mako                     | 17.1 ms                                                                | 17.0 ms: 1.00x faster                                                   |
| regex_compile            | 166 ms                                                                 | 165 ms: 1.00x faster                                                    |
| hexiom                   | 9.22 ms                                                                | 9.24 ms: 1.00x slower                                                   |
| sqlglot_normalize        | 132 ms                                                                 | 133 ms: 1.00x slower                                                    |
| unpickle_pure_python     | 320 us                                                                 | 321 us: 1.00x slower                                                    |
| float                    | 106 ms                                                                 | 106 ms: 1.00x slower                                                    |
| sympy_integrate          | 25.0 ms                                                                | 25.2 ms: 1.01x slower                                                   |
| html5lib                 | 88.3 ms                                                                | 88.8 ms: 1.01x slower                                                   |
| scimark_lu               | 155 ms                                                                 | 156 ms: 1.01x slower                                                    |
| deepcopy                 | 323 us                                                                 | 325 us: 1.01x slower                                                    |
| pycparser                | 1.34 sec                                                               | 1.35 sec: 1.01x slower                                                  |
| django_template          | 49.4 ms                                                                | 49.9 ms: 1.01x slower                                                   |
| fannkuch                 | 480 ms                                                                 | 485 ms: 1.01x slower                                                    |
| scimark_sor              | 201 ms                                                                 | 203 ms: 1.01x slower                                                    |
| typing_runtime_protocols | 201 us                                                                 | 203 us: 1.01x slower                                                    |
| coverage                 | 97.6 ms                                                                | 99.0 ms: 1.01x slower                                                   |
| nbody                    | 129 ms                                                                 | 131 ms: 1.02x slower                                                    |
| logging_simple           | 8.83 us                                                                | 8.98 us: 1.02x slower                                                   |
| spectral_norm            | 108 ms                                                                 | 110 ms: 1.02x slower                                                    |
| json                     | 5.10 ms                                                                | 5.20 ms: 1.02x slower                                                   |
| richards_super           | 74.6 ms                                                                | 76.0 ms: 1.02x slower                                                   |
| mdp                      | 2.73 sec                                                               | 2.78 sec: 1.02x slower                                                  |
| tomli_loads              | 2.32 sec                                                               | 2.37 sec: 1.02x slower                                                  |
| scimark_sparse_mat_mult  | 5.45 ms                                                                | 5.57 ms: 1.02x slower                                                   |
| pidigits                 | 197 ms                                                                 | 201 ms: 1.02x slower                                                    |
| json_loads               | 28.6 us                                                                | 29.2 us: 1.02x slower                                                   |
| nqueens                  | 95.3 ms                                                                | 97.4 ms: 1.02x slower                                                   |
| regex_effbot             | 2.69 ms                                                                | 2.75 ms: 1.02x slower                                                   |
| logging_format           | 9.81 us                                                                | 10.1 us: 1.02x slower                                                   |
| coroutines               | 23.1 ms                                                                | 23.7 ms: 1.03x slower                                                   |
| scimark_fft              | 373 ms                                                                 | 384 ms: 1.03x slower                                                    |
| pathlib                  | 19.2 ms                                                                | 19.8 ms: 1.03x slower                                                   |
| regex_dna                | 181 ms                                                                 | 188 ms: 1.03x slower                                                    |
| gc_traversal             | 3.52 ms                                                                | 3.65 ms: 1.04x slower                                                   |
| regex_v8                 | 23.4 ms                                                                | 24.4 ms: 1.04x slower                                                   |
| async_generators         | 430 ms                                                                 | 448 ms: 1.04x slower                                                    |
| pyflate                  | 620 ms                                                                 | 646 ms: 1.04x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (30): pylint, thrift, sphinx, sqlglot_optimize, sqlglot_transpile, xml_etree_generate, sqlglot_parse, generators, docutils, sympy_sum, xml_etree_process, k_core, async_tree_memoization, bench_thread_pool, crypto_pyaes, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_io_tg, telco, genshi_text, async_tree_cpu_io_mixed_tg, sympy_str, chaos, async_tree_io, genshi_xml, sqlite_synth, meteor_contest, sympy_expand, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 84.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x