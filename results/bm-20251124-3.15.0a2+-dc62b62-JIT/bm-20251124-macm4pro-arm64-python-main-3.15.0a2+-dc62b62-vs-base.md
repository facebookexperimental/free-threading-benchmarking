# Results vs. base

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.002x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 117 ms                                                                   | 118 ms: 1.01x slower                                     |
| html5lib       | 23.0 ms                                                                  | 23.4 ms: 1.02x slower                                    |
| sphinx         | 8.70 ms                                                                  | 8.74 ms: 1.00x slower                                    |
| Geometric mean | (ref)                                                                    | 1.01x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|-------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 225 ms                                                                   | 226 ms: 1.01x slower                                     |
| async_tree_eager_tg           | 82.3 ms                                                                  | 83.0 ms: 1.01x slower                                    |
| async_generators              | 185 ms                                                                   | 188 ms: 1.01x slower                                     |
| async_tree_eager              | 42.3 ms                                                                  | 42.9 ms: 1.02x slower                                    |
| Geometric mean                | (ref)                                                                    | 1.01x slower                                             |

Benchmark hidden because not significant (15): async_tree_io_tg, coroutines, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_memoization, async_tree_io, async_tree_eager_io, async_tree_eager_memoization, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 54.4 ms                                                                  | 54.1 ms: 1.00x faster                                    |
| pidigits       | 167 ms                                                                   | 167 ms: 1.00x slower                                     |
| Geometric mean | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_v8       | 9.84 ms                                                                  | 9.72 ms: 1.01x faster                                    |
| regex_dna      | 97.3 ms                                                                  | 96.6 ms: 1.01x faster                                    |
| regex_compile  | 45.3 ms                                                                  | 45.5 ms: 1.00x slower                                    |
| Geometric mean | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|---------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse     | 62.7 ms                                                                  | 61.5 ms: 1.02x faster                                    |
| xml_etree_iterparse | 39.0 ms                                                                  | 38.3 ms: 1.02x faster                                    |
| xml_etree_generate  | 34.5 ms                                                                  | 34.2 ms: 1.01x faster                                    |
| json_loads          | 11.1 us                                                                  | 10.9 us: 1.01x faster                                    |
| pickle_pure_python  | 133 us                                                                   | 132 us: 1.01x faster                                     |
| xml_etree_process   | 23.7 ms                                                                  | 23.6 ms: 1.00x faster                                    |
| json_dumps          | 3.79 ms                                                                  | 3.82 ms: 1.01x slower                                    |
| Geometric mean      | (ref)                                                                    | 1.01x faster                                             |

Benchmark hidden because not significant (2): tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 6.52 ms                                                                  | 6.53 ms: 1.00x slower                                    |
| python_startup         | 9.07 ms                                                                  | 9.10 ms: 1.00x slower                                    |
| Geometric mean         | (ref)                                                                    | 1.00x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                                  | 10.3 ms: 1.02x faster                                    |
| mako            | 4.36 ms                                                                  | 4.37 ms: 1.00x slower                                    |
| django_template | 14.7 ms                                                                  | 14.8 ms: 1.01x slower                                    |
| Geometric mean  | (ref)                                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                     | bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b | bm-20251124-macm4pro-arm64-python-main-3.15.0a2+-dc62b62 |
|-------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------:|
| deepcopy_reduce               | 1.07 us                                                                  | 1.04 us: 1.03x faster                                    |
| fannkuch                      | 181 ms                                                                   | 176 ms: 1.03x faster                                     |
| genshi_text                   | 10.5 ms                                                                  | 10.3 ms: 1.02x faster                                    |
| xml_etree_parse               | 62.7 ms                                                                  | 61.5 ms: 1.02x faster                                    |
| xml_etree_iterparse           | 39.0 ms                                                                  | 38.3 ms: 1.02x faster                                    |
| json                          | 1.96 ms                                                                  | 1.92 ms: 1.02x faster                                    |
| scimark_lu                    | 51.4 ms                                                                  | 50.5 ms: 1.02x faster                                    |
| richards_super                | 16.8 ms                                                                  | 16.6 ms: 1.01x faster                                    |
| coverage                      | 34.1 ms                                                                  | 33.7 ms: 1.01x faster                                    |
| regex_v8                      | 9.84 ms                                                                  | 9.72 ms: 1.01x faster                                    |
| xml_etree_generate            | 34.5 ms                                                                  | 34.2 ms: 1.01x faster                                    |
| json_loads                    | 11.1 us                                                                  | 10.9 us: 1.01x faster                                    |
| scimark_fft                   | 121 ms                                                                   | 120 ms: 1.01x faster                                     |
| pickle_pure_python            | 133 us                                                                   | 132 us: 1.01x faster                                     |
| deepcopy                      | 103 us                                                                   | 102 us: 1.01x faster                                     |
| regex_dna                     | 97.3 ms                                                                  | 96.6 ms: 1.01x faster                                    |
| nbody                         | 54.4 ms                                                                  | 54.1 ms: 1.00x faster                                    |
| xml_etree_process             | 23.7 ms                                                                  | 23.6 ms: 1.00x faster                                    |
| python_startup_no_site        | 6.52 ms                                                                  | 6.53 ms: 1.00x slower                                    |
| mako                          | 4.36 ms                                                                  | 4.37 ms: 1.00x slower                                    |
| python_startup                | 9.07 ms                                                                  | 9.10 ms: 1.00x slower                                    |
| pidigits                      | 167 ms                                                                   | 167 ms: 1.00x slower                                     |
| regex_compile                 | 45.3 ms                                                                  | 45.5 ms: 1.00x slower                                    |
| sqlglot_v2_parse              | 536 us                                                                   | 538 us: 1.00x slower                                     |
| sphinx                        | 8.70 ms                                                                  | 8.74 ms: 1.00x slower                                    |
| sqlglot_v2_transpile          | 663 us                                                                   | 666 us: 1.01x slower                                     |
| async_tree_eager_cpu_io_mixed | 225 ms                                                                   | 226 ms: 1.01x slower                                     |
| pprint_pformat                | 587 ms                                                                   | 591 ms: 1.01x slower                                     |
| crypto_pyaes                  | 37.8 ms                                                                  | 38.0 ms: 1.01x slower                                    |
| bpe_tokeniser                 | 2.04 sec                                                                 | 2.05 sec: 1.01x slower                                   |
| django_template               | 14.7 ms                                                                  | 14.8 ms: 1.01x slower                                    |
| comprehensions                | 7.37 us                                                                  | 7.41 us: 1.01x slower                                    |
| bench_mp_pool                 | 45.6 ms                                                                  | 45.9 ms: 1.01x slower                                    |
| pathlib                       | 10.9 ms                                                                  | 11.0 ms: 1.01x slower                                    |
| bench_thread_pool             | 430 us                                                                   | 433 us: 1.01x slower                                     |
| sqlite_synth                  | 958 ns                                                                   | 965 ns: 1.01x slower                                     |
| json_dumps                    | 3.79 ms                                                                  | 3.82 ms: 1.01x slower                                    |
| 2to3                          | 117 ms                                                                   | 118 ms: 1.01x slower                                     |
| hexiom                        | 3.20 ms                                                                  | 3.23 ms: 1.01x slower                                    |
| async_tree_eager_tg           | 82.3 ms                                                                  | 83.0 ms: 1.01x slower                                    |
| gc_traversal                  | 2.10 ms                                                                  | 2.12 ms: 1.01x slower                                    |
| sqlglot_v2_normalize          | 49.3 ms                                                                  | 49.8 ms: 1.01x slower                                    |
| chaos                         | 27.1 ms                                                                  | 27.4 ms: 1.01x slower                                    |
| sympy_expand                  | 183 ms                                                                   | 185 ms: 1.01x slower                                     |
| create_gc_cycles              | 939 us                                                                   | 949 us: 1.01x slower                                     |
| async_generators              | 185 ms                                                                   | 188 ms: 1.01x slower                                     |
| subparsers                    | 18.3 ms                                                                  | 18.5 ms: 1.01x slower                                    |
| dulwich_log                   | 19.7 ms                                                                  | 20.0 ms: 1.01x slower                                    |
| meteor_contest                | 50.0 ms                                                                  | 50.7 ms: 1.01x slower                                    |
| sympy_integrate               | 8.52 ms                                                                  | 8.65 ms: 1.02x slower                                    |
| logging_silent                | 47.9 ns                                                                  | 48.6 ns: 1.02x slower                                    |
| async_tree_eager              | 42.3 ms                                                                  | 42.9 ms: 1.02x slower                                    |
| html5lib                      | 23.0 ms                                                                  | 23.4 ms: 1.02x slower                                    |
| sympy_str                     | 113 ms                                                                   | 115 ms: 1.02x slower                                     |
| logging_format                | 2.44 us                                                                  | 2.48 us: 1.02x slower                                    |
| sympy_sum                     | 61.2 ms                                                                  | 62.3 ms: 1.02x slower                                    |
| many_optionals                | 375 us                                                                   | 384 us: 1.02x slower                                     |
| logging_simple                | 2.20 us                                                                  | 2.26 us: 1.02x slower                                    |
| generators                    | 18.8 ms                                                                  | 19.4 ms: 1.03x slower                                    |
| Geometric mean                | (ref)                                                                    | 1.00x slower                                             |

Benchmark hidden because not significant (39): mdp, tomli_loads, telco, typing_runtime_protocols, go, scimark_sparse_mat_mult, float, genshi_xml, deltablue, deepcopy_memo, async_tree_io_tg, sqlglot_v2_optimize, pprint_safe_repr, nqueens, coroutines, asyncio_websockets, raytrace, spectral_norm, pyflate, unpickle_pure_python, scimark_monte_carlo, thrift, async_tree_cpu_io_mixed_tg, pylint, async_tree_eager_io_tg, async_tree_memoization_tg, regex_effbot, async_tree_eager_memoization_tg, pycparser, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_memoization, async_tree_io, async_tree_eager_io, async_tree_eager_memoization, async_tree_none_tg, async_tree_none, richards, scimark_sor
Ignored benchmarks (1) of results/bm-20251124-3.15.0a2+-369ce2b-JIT/bm-20251124-macm4pro-arm64-python-369ce2b139a5b76c9c09-3.15.0a2+-369ce2b.json: dask

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x