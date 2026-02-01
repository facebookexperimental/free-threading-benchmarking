# Results vs. base

- fork: python
- ref: ccbe41e27cdb44103318
- machine: darwin-arm64
- commit hash: ccbe41e
- commit date: 2026-01-30
- overall geometric mean: 1.003x faster
- HPT reliability: 98.01%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| html5lib       | 22.6 ms                                                                  | 22.4 ms: 1.01x faster                                                    |
| sphinx         | 406 ms                                                                   | 405 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|--------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines         | 10.8 ms                                                                  | 10.2 ms: 1.05x faster                                                    |
| async_tree_eager   | 46.2 ms                                                                  | 45.9 ms: 1.01x faster                                                    |
| async_generators   | 182 ms                                                                   | 181 ms: 1.00x faster                                                     |
| asyncio_websockets | 185 ms                                                                   | 186 ms: 1.01x slower                                                     |
| Geometric mean     | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (15): async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_memoization_tg, async_tree_eager_io, async_tree_eager_tg, async_tree_eager_io_tg, async_tree_io_tg, async_tree_none, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed, async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_eager_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 28.5 ms                                                                  | 28.4 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 9.10 ms                                                                  | 8.97 ms: 1.01x faster                                                    |
| regex_compile  | 49.6 ms                                                                  | 49.5 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 58.5 ms                                                                  | 57.3 ms: 1.02x faster                                                    |
| xml_etree_generate   | 36.9 ms                                                                  | 36.5 ms: 1.01x faster                                                    |
| unpickle_pure_python | 107 us                                                                   | 106 us: 1.01x faster                                                     |
| tomli_loads          | 875 ms                                                                   | 866 ms: 1.01x faster                                                     |
| pickle_pure_python   | 143 us                                                                   | 142 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 38.0 ms                                                                  | 38.8 ms: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (3): json_loads, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 11.7 ms                                                                  | 10.6 ms: 1.10x faster                                                    |
| genshi_xml     | 21.9 ms                                                                  | 21.7 ms: 1.01x faster                                                    |
| mako           | 5.47 ms                                                                  | 5.42 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20260130-macm4pro-arm64-python-96e4cd698a3000382f17-3.15.0a5+-96e4cd6 | bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e |
|--------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text              | 11.7 ms                                                                  | 10.6 ms: 1.10x faster                                                    |
| coroutines               | 10.8 ms                                                                  | 10.2 ms: 1.05x faster                                                    |
| crypto_pyaes             | 42.8 ms                                                                  | 41.8 ms: 1.02x faster                                                    |
| xml_etree_parse          | 58.5 ms                                                                  | 57.3 ms: 1.02x faster                                                    |
| comprehensions           | 8.26 us                                                                  | 8.11 us: 1.02x faster                                                    |
| spectral_norm            | 50.9 ms                                                                  | 50.0 ms: 1.02x faster                                                    |
| regex_v8                 | 9.10 ms                                                                  | 8.97 ms: 1.01x faster                                                    |
| thrift                   | 331 us                                                                   | 326 us: 1.01x faster                                                     |
| go                       | 59.6 ms                                                                  | 58.8 ms: 1.01x faster                                                    |
| logging_format           | 2.65 us                                                                  | 2.62 us: 1.01x faster                                                    |
| deltablue                | 1.59 ms                                                                  | 1.58 ms: 1.01x faster                                                    |
| xml_etree_generate       | 36.9 ms                                                                  | 36.5 ms: 1.01x faster                                                    |
| genshi_xml               | 21.9 ms                                                                  | 21.7 ms: 1.01x faster                                                    |
| unpickle_pure_python     | 107 us                                                                   | 106 us: 1.01x faster                                                     |
| tomli_loads              | 875 ms                                                                   | 866 ms: 1.01x faster                                                     |
| mako                     | 5.47 ms                                                                  | 5.42 ms: 1.01x faster                                                    |
| json                     | 1.92 ms                                                                  | 1.90 ms: 1.01x faster                                                    |
| html5lib                 | 22.6 ms                                                                  | 22.4 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult  | 2.12 ms                                                                  | 2.11 ms: 1.01x faster                                                    |
| async_tree_eager         | 46.2 ms                                                                  | 45.9 ms: 1.01x faster                                                    |
| pickle_pure_python       | 143 us                                                                   | 142 us: 1.01x faster                                                     |
| dulwich_log              | 18.1 ms                                                                  | 18.0 ms: 1.01x faster                                                    |
| pycparser                | 454 ms                                                                   | 451 ms: 1.00x faster                                                     |
| float                    | 28.5 ms                                                                  | 28.4 ms: 1.00x faster                                                    |
| sphinx                   | 406 ms                                                                   | 405 ms: 1.00x faster                                                     |
| async_generators         | 182 ms                                                                   | 181 ms: 1.00x faster                                                     |
| coverage                 | 38.5 ms                                                                  | 38.4 ms: 1.00x faster                                                    |
| telco                    | 3.02 ms                                                                  | 3.01 ms: 1.00x faster                                                    |
| pprint_pformat           | 675 ms                                                                   | 673 ms: 1.00x faster                                                     |
| richards                 | 22.4 ms                                                                  | 22.4 ms: 1.00x faster                                                    |
| pprint_safe_repr         | 330 ms                                                                   | 329 ms: 1.00x faster                                                     |
| regex_compile            | 49.6 ms                                                                  | 49.5 ms: 1.00x faster                                                    |
| bench_mp_pool            | 45.1 ms                                                                  | 45.2 ms: 1.00x slower                                                    |
| nqueens                  | 41.8 ms                                                                  | 41.9 ms: 1.00x slower                                                    |
| chaos                    | 27.3 ms                                                                  | 27.4 ms: 1.00x slower                                                    |
| mdp                      | 595 ms                                                                   | 598 ms: 1.00x slower                                                     |
| sympy_sum                | 59.2 ms                                                                  | 59.5 ms: 1.00x slower                                                    |
| hexiom                   | 3.09 ms                                                                  | 3.10 ms: 1.00x slower                                                    |
| connected_components     | 245 ms                                                                   | 246 ms: 1.00x slower                                                     |
| deepcopy                 | 104 us                                                                   | 105 us: 1.01x slower                                                     |
| asyncio_websockets       | 185 ms                                                                   | 186 ms: 1.01x slower                                                     |
| bpe_tokeniser            | 1.95 sec                                                                 | 1.96 sec: 1.01x slower                                                   |
| pyflate                  | 191 ms                                                                   | 193 ms: 1.01x slower                                                     |
| logging_silent           | 43.4 ns                                                                  | 43.8 ns: 1.01x slower                                                    |
| generators               | 20.3 ms                                                                  | 20.6 ms: 1.02x slower                                                    |
| typing_runtime_protocols | 69.3 us                                                                  | 70.5 us: 1.02x slower                                                    |
| xml_etree_iterparse      | 38.0 ms                                                                  | 38.8 ms: 1.02x slower                                                    |
| scimark_lu               | 55.1 ms                                                                  | 57.3 ms: 1.04x slower                                                    |
| Geometric mean           | (ref)                                                                    | 1.00x faster                                                             |

Benchmark hidden because not significant (55): pylint, sqlite_synth, deepcopy_reduce, richards_super, logging_simple, sqlglot_v2_transpile, scimark_monte_carlo, sqlglot_v2_parse, bench_thread_pool, pathlib, create_gc_cycles, async_tree_cpu_io_mixed, many_optionals, sympy_integrate, async_tree_eager_memoization, json_loads, xml_etree_process, docutils, async_tree_memoization_tg, fannkuch, shortest_path, async_tree_eager_io, 2to3, pidigits, sympy_expand, dask, scimark_sor, async_tree_eager_tg, async_tree_eager_io_tg, async_tree_io_tg, python_startup, async_tree_none, raytrace, django_template, k_core, gc_traversal, async_tree_eager_memoization_tg, python_startup_no_site, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed, sqlglot_v2_optimize, subparsers, regex_dna, sympy_str, json_dumps, meteor_contest, async_tree_memoization, async_tree_io, deepcopy_memo, sqlglot_v2_normalize, async_tree_none_tg, async_tree_eager_cpu_io_mixed_tg, regex_effbot, scimark_fft, nbody
Ignored benchmarks (8) of results/bm-20260130-3.15.0a5+-ccbe41e-NOGIL/bm-20260130-macm4pro-arm64-python-ccbe41e27cdb44103318-3.15.0a5+-ccbe41e.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 98.01% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x