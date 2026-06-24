# Results vs. base

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.008x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                | 262 ms: 1.01x slower                                              |
| docutils       | 2.40 sec                                                              | 2.39 sec: 1.01x faster                                            |
| sphinx         | 978 ms                                                                | 998 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines     | 24.1 ms                                                               | 23.5 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                      |

Benchmark hidden because not significant (10): async_generators, async_tree_memoization, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 75.0 ms                                                               | 74.3 ms: 1.01x faster                                             |
| pidigits       | 188 ms                                                                | 191 ms: 1.01x slower                                              |
| nbody          | 90.5 ms                                                               | 95.0 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 124 ms                                                                | 125 ms: 1.02x slower                                              |
| regex_v8       | 21.4 ms                                                               | 22.2 ms: 1.04x slower                                             |
| regex_dna      | 173 ms                                                                | 181 ms: 1.04x slower                                              |
| regex_effbot   | 2.61 ms                                                               | 2.75 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                 | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_parse     | 144 ms                                                                | 143 ms: 1.01x faster                                              |
| pickle_pure_python  | 314 us                                                                | 313 us: 1.00x faster                                              |
| tomli_loads         | 1.86 sec                                                              | 1.88 sec: 1.01x slower                                            |
| json_dumps          | 9.70 ms                                                               | 9.84 ms: 1.01x slower                                             |
| xml_etree_iterparse | 89.7 ms                                                               | 91.6 ms: 1.02x slower                                             |
| xml_etree_generate  | 86.3 ms                                                               | 88.6 ms: 1.03x slower                                             |
| xml_etree_process   | 61.3 ms                                                               | 63.1 ms: 1.03x slower                                             |
| Geometric mean      | (ref)                                                                 | 1.01x slower                                                      |

Benchmark hidden because not significant (2): json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 6.92 ms                                                               | 6.97 ms: 1.01x slower                                             |
| python_startup         | 12.3 ms                                                               | 12.4 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.8 ms                                                               | 11.9 ms: 1.00x slower                                             |
| django_template | 35.1 ms                                                               | 37.2 ms: 1.06x slower                                             |
| Geometric mean  | (ref)                                                                 | 1.03x slower                                                      |

All benchmarks:
===============

| Benchmark                | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| spectral_norm            | 97.9 ms                                                               | 94.3 ms: 1.04x faster                                             |
| pycparser                | 1.19 sec                                                              | 1.15 sec: 1.04x faster                                            |
| coroutines               | 24.1 ms                                                               | 23.5 ms: 1.03x faster                                             |
| deltablue                | 3.47 ms                                                               | 3.41 ms: 1.02x faster                                             |
| go                       | 108 ms                                                                | 106 ms: 1.02x faster                                              |
| create_gc_cycles         | 1.68 ms                                                               | 1.65 ms: 1.02x faster                                             |
| chaos                    | 55.7 ms                                                               | 54.8 ms: 1.02x faster                                             |
| subparsers               | 9.37 ms                                                               | 9.22 ms: 1.02x faster                                             |
| comprehensions           | 16.0 us                                                               | 15.7 us: 1.02x faster                                             |
| json                     | 5.00 ms                                                               | 4.93 ms: 1.02x faster                                             |
| meteor_contest           | 101 ms                                                                | 99.3 ms: 1.01x faster                                             |
| pyflate                  | 414 ms                                                                | 408 ms: 1.01x faster                                              |
| sqlite_synth             | 2.24 us                                                               | 2.21 us: 1.01x faster                                             |
| generators               | 28.7 ms                                                               | 28.3 ms: 1.01x faster                                             |
| bench_thread_pool        | 1.36 ms                                                               | 1.34 ms: 1.01x faster                                             |
| scimark_monte_carlo      | 64.6 ms                                                               | 63.8 ms: 1.01x faster                                             |
| raytrace                 | 259 ms                                                                | 256 ms: 1.01x faster                                              |
| deepcopy_memo            | 26.6 us                                                               | 26.4 us: 1.01x faster                                             |
| float                    | 75.0 ms                                                               | 74.3 ms: 1.01x faster                                             |
| crypto_pyaes             | 70.2 ms                                                               | 69.5 ms: 1.01x faster                                             |
| gc_traversal             | 3.57 ms                                                               | 3.54 ms: 1.01x faster                                             |
| fannkuch                 | 384 ms                                                                | 381 ms: 1.01x faster                                              |
| dulwich_log              | 68.9 ms                                                               | 68.4 ms: 1.01x faster                                             |
| hexiom                   | 5.89 ms                                                               | 5.85 ms: 1.01x faster                                             |
| docutils                 | 2.40 sec                                                              | 2.39 sec: 1.01x faster                                            |
| xml_etree_parse          | 144 ms                                                                | 143 ms: 1.01x faster                                              |
| many_optionals           | 917 us                                                                | 912 us: 1.00x faster                                              |
| scimark_sor              | 111 ms                                                                | 111 ms: 1.00x faster                                              |
| pickle_pure_python       | 314 us                                                                | 313 us: 1.00x faster                                              |
| shortest_path            | 443 ms                                                                | 445 ms: 1.00x slower                                              |
| mako                     | 11.8 ms                                                               | 11.9 ms: 1.00x slower                                             |
| sqlglot_v2_transpile     | 1.46 ms                                                               | 1.47 ms: 1.00x slower                                             |
| pprint_safe_repr         | 734 ms                                                                | 738 ms: 1.01x slower                                              |
| connected_components     | 401 ms                                                                | 403 ms: 1.01x slower                                              |
| python_startup_no_site   | 6.92 ms                                                               | 6.97 ms: 1.01x slower                                             |
| tomli_loads              | 1.86 sec                                                              | 1.88 sec: 1.01x slower                                            |
| mdp                      | 1.13 sec                                                              | 1.14 sec: 1.01x slower                                            |
| pylint                   | 115 ms                                                                | 116 ms: 1.01x slower                                              |
| 2to3                     | 259 ms                                                                | 262 ms: 1.01x slower                                              |
| bpe_tokeniser            | 4.21 sec                                                              | 4.25 sec: 1.01x slower                                            |
| telco                    | 163 ms                                                                | 165 ms: 1.01x slower                                              |
| python_startup           | 12.3 ms                                                               | 12.4 ms: 1.01x slower                                             |
| scimark_fft              | 320 ms                                                                | 325 ms: 1.01x slower                                              |
| pidigits                 | 188 ms                                                                | 191 ms: 1.01x slower                                              |
| json_dumps               | 9.70 ms                                                               | 9.84 ms: 1.01x slower                                             |
| regex_compile            | 124 ms                                                                | 125 ms: 1.02x slower                                              |
| sympy_integrate          | 19.0 ms                                                               | 19.3 ms: 1.02x slower                                             |
| nqueens                  | 74.2 ms                                                               | 75.4 ms: 1.02x slower                                             |
| sympy_sum                | 156 ms                                                                | 158 ms: 1.02x slower                                              |
| pprint_pformat           | 1.49 sec                                                              | 1.51 sec: 1.02x slower                                            |
| coverage                 | 84.2 ms                                                               | 85.7 ms: 1.02x slower                                             |
| logging_simple           | 6.10 us                                                               | 6.22 us: 1.02x slower                                             |
| sphinx                   | 978 ms                                                                | 998 ms: 1.02x slower                                              |
| xml_etree_iterparse      | 89.7 ms                                                               | 91.6 ms: 1.02x slower                                             |
| pathlib                  | 17.8 ms                                                               | 18.2 ms: 1.02x slower                                             |
| richards                 | 43.7 ms                                                               | 44.7 ms: 1.02x slower                                             |
| deepcopy                 | 232 us                                                                | 238 us: 1.03x slower                                              |
| xml_etree_generate       | 86.3 ms                                                               | 88.6 ms: 1.03x slower                                             |
| sympy_str                | 273 ms                                                                | 280 ms: 1.03x slower                                              |
| xml_etree_process        | 61.3 ms                                                               | 63.1 ms: 1.03x slower                                             |
| sqlglot_v2_normalize     | 101 ms                                                                | 104 ms: 1.03x slower                                              |
| richards_super           | 49.5 ms                                                               | 51.1 ms: 1.03x slower                                             |
| sqlglot_v2_optimize      | 51.2 ms                                                               | 52.8 ms: 1.03x slower                                             |
| deepcopy_reduce          | 2.58 us                                                               | 2.67 us: 1.03x slower                                             |
| thrift                   | 791 us                                                                | 818 us: 1.03x slower                                              |
| regex_v8                 | 21.4 ms                                                               | 22.2 ms: 1.04x slower                                             |
| sympy_expand             | 458 ms                                                                | 475 ms: 1.04x slower                                              |
| regex_dna                | 173 ms                                                                | 181 ms: 1.04x slower                                              |
| typing_runtime_protocols | 117 us                                                                | 122 us: 1.04x slower                                              |
| logging_format           | 6.77 us                                                               | 7.08 us: 1.05x slower                                             |
| nbody                    | 90.5 ms                                                               | 95.0 ms: 1.05x slower                                             |
| regex_effbot             | 2.61 ms                                                               | 2.75 ms: 1.05x slower                                             |
| django_template          | 35.1 ms                                                               | 37.2 ms: 1.06x slower                                             |
| scimark_lu               | 112 ms                                                                | 119 ms: 1.06x slower                                              |
| scimark_sparse_mat_mult  | 4.53 ms                                                               | 4.83 ms: 1.06x slower                                             |
| Geometric mean           | (ref)                                                                 | 1.01x slower                                                      |

Benchmark hidden because not significant (17): bench_mp_pool, logging_silent, k_core, async_generators, sqlglot_v2_parse, async_tree_memoization, asyncio_websockets, json_loads, async_tree_cpu_io_mixed_tg, unpickle_pure_python, html5lib, async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_io, async_tree_io_tg

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x