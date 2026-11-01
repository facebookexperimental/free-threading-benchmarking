# Results vs. base

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: linux-x86_64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.005x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| docutils       | 2.85 sec                                                                  | 2.89 sec: 1.01x slower                                                    |
| html5lib       | 64.4 ms                                                                   | 64.9 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                              |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 692 ms                                                                    | 697 ms: 1.01x slower                                                      |
| async_tree_io              | 705 ms                                                                    | 712 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed_tg | 577 ms                                                                    | 589 ms: 1.02x slower                                                      |
| async_tree_cpu_io_mixed    | 594 ms                                                                    | 606 ms: 1.02x slower                                                      |
| coroutines                 | 25.6 ms                                                                   | 26.2 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.01x slower                                                              |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_none_tg, async_generators, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                    | 188 ms: 1.00x slower                                                      |
| float          | 84.3 ms                                                                   | 84.7 ms: 1.00x slower                                                     |
| nbody          | 115 ms                                                                    | 116 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 2.89 ms                                                                   | 2.99 ms: 1.04x slower                                                     |
| regex_dna      | 173 ms                                                                    | 180 ms: 1.04x slower                                                      |
| regex_v8       | 20.1 ms                                                                   | 21.1 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.03x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|---------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_loads          | 30.8 us                                                                   | 30.5 us: 1.01x faster                                                     |
| xml_etree_iterparse | 97.3 ms                                                                   | 96.8 ms: 1.01x faster                                                     |
| xml_etree_process   | 75.5 ms                                                                   | 75.8 ms: 1.00x slower                                                     |
| xml_etree_parse     | 142 ms                                                                    | 143 ms: 1.01x slower                                                      |
| json_dumps          | 10.1 ms                                                                   | 10.2 ms: 1.01x slower                                                     |
| pickle_pure_python  | 342 us                                                                    | 347 us: 1.01x slower                                                      |
| xml_etree_generate  | 98.9 ms                                                                   | 101 ms: 1.02x slower                                                      |
| Geometric mean      | (ref)                                                                     | 1.00x slower                                                              |

Benchmark hidden because not significant (2): tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 13.8 ms                                                                   | 13.8 ms: 1.00x faster                                                     |
| python_startup_no_site | 9.08 ms                                                                   | 9.09 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                     | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 15.7 ms                                                                   | 15.6 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a | bm-20261031-vultr-x86_64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------|:-------------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| scimark_lu                 | 132 ms                                                                    | 127 ms: 1.04x faster                                                      |
| scimark_sparse_mat_mult    | 4.97 ms                                                                   | 4.85 ms: 1.02x faster                                                     |
| pycparser                  | 1.15 sec                                                                  | 1.12 sec: 1.02x faster                                                    |
| fannkuch                   | 470 ms                                                                    | 465 ms: 1.01x faster                                                      |
| json_loads                 | 30.8 us                                                                   | 30.5 us: 1.01x faster                                                     |
| comprehensions             | 17.9 us                                                                   | 17.7 us: 1.01x faster                                                     |
| shortest_path              | 536 ms                                                                    | 531 ms: 1.01x faster                                                      |
| bpe_tokeniser              | 4.41 sec                                                                  | 4.38 sec: 1.01x faster                                                    |
| mako                       | 15.7 ms                                                                   | 15.6 ms: 1.01x faster                                                     |
| sqlglot_v2_normalize       | 117 ms                                                                    | 116 ms: 1.01x faster                                                      |
| xml_etree_iterparse        | 97.3 ms                                                                   | 96.8 ms: 1.01x faster                                                     |
| scimark_monte_carlo        | 78.0 ms                                                                   | 77.5 ms: 1.01x faster                                                     |
| crypto_pyaes               | 88.1 ms                                                                   | 87.7 ms: 1.00x faster                                                     |
| mdp                        | 1.31 sec                                                                  | 1.30 sec: 1.00x faster                                                    |
| pyflate                    | 447 ms                                                                    | 445 ms: 1.00x faster                                                      |
| python_startup             | 13.8 ms                                                                   | 13.8 ms: 1.00x faster                                                     |
| python_startup_no_site     | 9.08 ms                                                                   | 9.09 ms: 1.00x slower                                                     |
| pidigits                   | 187 ms                                                                    | 188 ms: 1.00x slower                                                      |
| float                      | 84.3 ms                                                                   | 84.7 ms: 1.00x slower                                                     |
| xml_etree_process          | 75.5 ms                                                                   | 75.8 ms: 1.00x slower                                                     |
| xml_etree_parse            | 142 ms                                                                    | 143 ms: 1.01x slower                                                      |
| connected_components       | 486 ms                                                                    | 489 ms: 1.01x slower                                                      |
| json_dumps                 | 10.1 ms                                                                   | 10.2 ms: 1.01x slower                                                     |
| bench_thread_pool          | 1.40 ms                                                                   | 1.41 ms: 1.01x slower                                                     |
| html5lib                   | 64.4 ms                                                                   | 64.9 ms: 1.01x slower                                                     |
| sympy_integrate            | 22.0 ms                                                                   | 22.2 ms: 1.01x slower                                                     |
| async_tree_io_tg           | 692 ms                                                                    | 697 ms: 1.01x slower                                                      |
| meteor_contest             | 124 ms                                                                    | 125 ms: 1.01x slower                                                      |
| sqlglot_v2_parse           | 1.39 ms                                                                   | 1.40 ms: 1.01x slower                                                     |
| k_core                     | 2.22 sec                                                                  | 2.23 sec: 1.01x slower                                                    |
| coverage                   | 116 ms                                                                    | 117 ms: 1.01x slower                                                      |
| nbody                      | 115 ms                                                                    | 116 ms: 1.01x slower                                                      |
| spectral_norm              | 103 ms                                                                    | 104 ms: 1.01x slower                                                      |
| sqlglot_v2_transpile       | 1.71 ms                                                                   | 1.73 ms: 1.01x slower                                                     |
| richards_super             | 60.3 ms                                                                   | 60.9 ms: 1.01x slower                                                     |
| async_tree_io              | 705 ms                                                                    | 712 ms: 1.01x slower                                                      |
| raytrace                   | 291 ms                                                                    | 294 ms: 1.01x slower                                                      |
| deepcopy                   | 267 us                                                                    | 270 us: 1.01x slower                                                      |
| docutils                   | 2.85 sec                                                                  | 2.89 sec: 1.01x slower                                                    |
| deepcopy_reduce            | 2.90 us                                                                   | 2.94 us: 1.01x slower                                                     |
| pickle_pure_python         | 342 us                                                                    | 347 us: 1.01x slower                                                      |
| hexiom                     | 6.40 ms                                                                   | 6.49 ms: 1.01x slower                                                     |
| deltablue                  | 3.68 ms                                                                   | 3.74 ms: 1.02x slower                                                     |
| go                         | 120 ms                                                                    | 122 ms: 1.02x slower                                                      |
| pprint_safe_repr           | 796 ms                                                                    | 812 ms: 1.02x slower                                                      |
| async_tree_cpu_io_mixed_tg | 577 ms                                                                    | 589 ms: 1.02x slower                                                      |
| deepcopy_memo              | 32.7 us                                                                   | 33.3 us: 1.02x slower                                                     |
| async_tree_cpu_io_mixed    | 594 ms                                                                    | 606 ms: 1.02x slower                                                      |
| coroutines                 | 25.6 ms                                                                   | 26.2 ms: 1.02x slower                                                     |
| logging_format             | 7.76 us                                                                   | 7.93 us: 1.02x slower                                                     |
| xml_etree_generate         | 98.9 ms                                                                   | 101 ms: 1.02x slower                                                      |
| pprint_pformat             | 1.65 sec                                                                  | 1.69 sec: 1.03x slower                                                    |
| logging_silent             | 106 ns                                                                    | 110 ns: 1.03x slower                                                      |
| regex_effbot               | 2.89 ms                                                                   | 2.99 ms: 1.04x slower                                                     |
| typing_runtime_protocols   | 137 us                                                                    | 142 us: 1.04x slower                                                      |
| regex_dna                  | 173 ms                                                                    | 180 ms: 1.04x slower                                                      |
| regex_v8                   | 20.1 ms                                                                   | 21.1 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.01x slower                                                              |

Benchmark hidden because not significant (35): json, bench_mp_pool, subparsers, many_optionals, logging_simple, pylint, dulwich_log, create_gc_cycles, scimark_sor, 2to3, django_template, chaos, scimark_fft, regex_compile, asyncio_websockets, sympy_expand, tomli_loads, telco, unpickle_pure_python, nqueens, sqlite_synth, gc_traversal, thrift, richards, async_tree_none_tg, sympy_sum, sympy_str, generators, pathlib, sqlglot_v2_optimize, async_generators, sphinx, async_tree_memoization_tg, async_tree_none, async_tree_memoization
Ignored benchmarks (8) of results/bm-20261031-3.16.0a1+dev-47c249a-NOGIL/bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1+dev-47c249a.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x