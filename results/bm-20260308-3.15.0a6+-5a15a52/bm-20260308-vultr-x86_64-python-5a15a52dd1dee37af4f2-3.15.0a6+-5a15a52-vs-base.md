# Results vs. base

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: linux-x86_64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.002x faster
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 249 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 502 ms: 1.01x faster                                                   |
| async_tree_io              | 590 ms                                                                 | 586 ms: 1.01x faster                                                   |
| async_tree_none            | 247 ms                                                                 | 249 ms: 1.01x slower                                                   |
| coroutines                 | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_generators, async_tree_io_tg, asyncio_websockets, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                                | 90.3 ms: 1.03x faster                                                  |
| float          | 70.4 ms                                                                | 68.9 ms: 1.02x faster                                                  |
| pidigits       | 198 ms                                                                 | 221 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 124 ms                                                                 | 123 ms: 1.01x faster                                                   |
| regex_dna      | 173 ms                                                                 | 187 ms: 1.08x slower                                                   |
| regex_effbot   | 2.73 ms                                                                | 3.02 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps          | 9.94 ms                                                                | 9.66 ms: 1.03x faster                                                  |
| xml_etree_process   | 59.0 ms                                                                | 57.9 ms: 1.02x faster                                                  |
| xml_etree_generate  | 84.0 ms                                                                | 82.6 ms: 1.02x faster                                                  |
| xml_etree_parse     | 132 ms                                                                 | 131 ms: 1.01x faster                                                   |
| json_loads          | 28.5 us                                                                | 28.1 us: 1.01x faster                                                  |
| tomli_loads         | 1.83 sec                                                               | 1.81 sec: 1.01x faster                                                 |
| pickle_pure_python  | 309 us                                                                 | 307 us: 1.01x faster                                                   |
| xml_etree_iterparse | 84.6 ms                                                                | 85.3 ms: 1.01x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.44 ms                                                                | 7.41 ms: 1.00x faster                                                  |
| python_startup         | 12.6 ms                                                                | 12.6 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.7 ms                                                                | 48.7 ms: 1.02x faster                                                  |
| mako            | 12.0 ms                                                                | 12.0 ms: 1.00x slower                                                  |
| django_template | 34.7 ms                                                                | 35.2 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pycparser                  | 1.13 sec                                                               | 1.08 sec: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 4.63 ms                                                                | 4.46 ms: 1.04x faster                                                  |
| nbody                      | 92.9 ms                                                                | 90.3 ms: 1.03x faster                                                  |
| json_dumps                 | 9.94 ms                                                                | 9.66 ms: 1.03x faster                                                  |
| hexiom                     | 5.67 ms                                                                | 5.53 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 2.55 us                                                                | 2.49 us: 1.02x faster                                                  |
| float                      | 70.4 ms                                                                | 68.9 ms: 1.02x faster                                                  |
| scimark_fft                | 314 ms                                                                 | 308 ms: 1.02x faster                                                   |
| genshi_xml                 | 49.7 ms                                                                | 48.7 ms: 1.02x faster                                                  |
| pathlib                    | 17.4 ms                                                                | 17.1 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                                | 57.9 ms: 1.02x faster                                                  |
| logging_silent             | 102 ns                                                                 | 99.7 ns: 1.02x faster                                                  |
| create_gc_cycles           | 1.89 ms                                                                | 1.86 ms: 1.02x faster                                                  |
| generators                 | 27.9 ms                                                                | 27.4 ms: 1.02x faster                                                  |
| xml_etree_generate         | 84.0 ms                                                                | 82.6 ms: 1.02x faster                                                  |
| nqueens                    | 75.1 ms                                                                | 74.0 ms: 1.02x faster                                                  |
| sympy_sum                  | 160 ms                                                                 | 157 ms: 1.02x faster                                                   |
| crypto_pyaes               | 68.2 ms                                                                | 67.2 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 502 ms: 1.01x faster                                                   |
| json                       | 5.15 ms                                                                | 5.08 ms: 1.01x faster                                                  |
| chaos                      | 54.1 ms                                                                | 53.4 ms: 1.01x faster                                                  |
| xml_etree_parse            | 132 ms                                                                 | 131 ms: 1.01x faster                                                   |
| json_loads                 | 28.5 us                                                                | 28.1 us: 1.01x faster                                                  |
| tomli_loads                | 1.83 sec                                                               | 1.81 sec: 1.01x faster                                                 |
| connected_components       | 392 ms                                                                 | 388 ms: 1.01x faster                                                   |
| spectral_norm              | 92.9 ms                                                                | 92.0 ms: 1.01x faster                                                  |
| mdp                        | 1.15 sec                                                               | 1.14 sec: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 101 ms: 1.01x faster                                                   |
| regex_compile              | 124 ms                                                                 | 123 ms: 1.01x faster                                                   |
| go                         | 105 ms                                                                 | 104 ms: 1.01x faster                                                   |
| dulwich_log                | 67.5 ms                                                                | 66.9 ms: 1.01x faster                                                  |
| k_core                     | 1.88 sec                                                               | 1.87 sec: 1.01x faster                                                 |
| deepcopy                   | 232 us                                                                 | 230 us: 1.01x faster                                                   |
| scimark_monte_carlo        | 62.6 ms                                                                | 62.0 ms: 1.01x faster                                                  |
| comprehensions             | 16.2 us                                                                | 16.1 us: 1.01x faster                                                  |
| logging_simple             | 5.88 us                                                                | 5.84 us: 1.01x faster                                                  |
| bpe_tokeniser              | 4.12 sec                                                               | 4.09 sec: 1.01x faster                                                 |
| async_tree_io              | 590 ms                                                                 | 586 ms: 1.01x faster                                                   |
| subparsers                 | 9.19 ms                                                                | 9.14 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.4 ms                                                                | 19.3 ms: 1.01x faster                                                  |
| 2to3                       | 250 ms                                                                 | 249 ms: 1.01x faster                                                   |
| pickle_pure_python         | 309 us                                                                 | 307 us: 1.01x faster                                                   |
| python_startup_no_site     | 7.44 ms                                                                | 7.41 ms: 1.00x faster                                                  |
| deltablue                  | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                                  |
| python_startup             | 12.6 ms                                                                | 12.6 ms: 1.00x faster                                                  |
| pyflate                    | 406 ms                                                                 | 405 ms: 1.00x faster                                                   |
| sqlglot_v2_optimize        | 51.0 ms                                                                | 50.9 ms: 1.00x faster                                                  |
| raytrace                   | 251 ms                                                                 | 250 ms: 1.00x faster                                                   |
| shortest_path              | 431 ms                                                                 | 432 ms: 1.00x slower                                                   |
| gc_traversal               | 4.02 ms                                                                | 4.03 ms: 1.00x slower                                                  |
| mako                       | 12.0 ms                                                                | 12.0 ms: 1.00x slower                                                  |
| fannkuch                   | 378 ms                                                                 | 380 ms: 1.00x slower                                                   |
| richards_super             | 47.7 ms                                                                | 48.1 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 714 ms                                                                 | 719 ms: 1.01x slower                                                   |
| xml_etree_iterparse        | 84.6 ms                                                                | 85.3 ms: 1.01x slower                                                  |
| async_tree_none            | 247 ms                                                                 | 249 ms: 1.01x slower                                                   |
| sqlglot_v2_transpile       | 1.50 ms                                                                | 1.52 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.47 sec: 1.01x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 110 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 160 us                                                                 | 162 us: 1.01x slower                                                   |
| coroutines                 | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                  |
| django_template            | 34.7 ms                                                                | 35.2 ms: 1.02x slower                                                  |
| logging_format             | 6.58 us                                                                | 6.73 us: 1.02x slower                                                  |
| regex_dna                  | 173 ms                                                                 | 187 ms: 1.08x slower                                                   |
| regex_effbot               | 2.73 ms                                                                | 3.02 ms: 1.11x slower                                                  |
| pidigits                   | 198 ms                                                                 | 221 ms: 1.12x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (28): bench_mp_pool, pylint, async_tree_cpu_io_mixed, coverage, async_tree_memoization_tg, sympy_str, async_generators, genshi_text, async_tree_io_tg, sqlite_synth, sqlglot_v2_parse, sqlglot_v2_normalize, unpickle_pure_python, docutils, asyncio_websockets, sympy_expand, scimark_sor, deepcopy_memo, thrift, richards, many_optionals, telco, sphinx, bench_thread_pool, regex_v8, async_tree_memoization, html5lib, async_tree_none_tg
Ignored benchmarks (8) of results/bm-20260307-3.15.0a6+-149c465/bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x