# Results vs. default_base_vs_NOGIL

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.106x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                | 297 ms: 1.15x slower                                              |
| docutils       | 2.40 sec                                                              | 2.93 sec: 1.22x slower                                            |
| html5lib       | 60.8 ms                                                               | 68.6 ms: 1.13x slower                                             |
| sphinx         | 978 ms                                                                | 1.11 sec: 1.13x slower                                            |
| Geometric mean | (ref)                                                                 | 1.16x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 761 ms                                                                | 681 ms: 1.12x faster                                              |
| asyncio_websockets         | 544 ms                                                                | 513 ms: 1.06x faster                                              |
| async_tree_io              | 721 ms                                                                | 709 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                | 578 ms: 1.03x slower                                              |
| coroutines                 | 24.1 ms                                                               | 25.0 ms: 1.04x slower                                             |
| async_tree_memoization_tg  | 365 ms                                                                | 394 ms: 1.08x slower                                              |
| async_tree_none_tg         | 299 ms                                                                | 324 ms: 1.08x slower                                              |
| async_tree_cpu_io_mixed    | 544 ms                                                                | 605 ms: 1.11x slower                                              |
| async_tree_memoization     | 378 ms                                                                | 420 ms: 1.11x slower                                              |
| async_generators           | 342 ms                                                                | 390 ms: 1.14x slower                                              |
| async_tree_none            | 295 ms                                                                | 345 ms: 1.17x slower                                              |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 75.0 ms                                                               | 86.9 ms: 1.16x slower                                             |
| nbody          | 90.5 ms                                                               | 125 ms: 1.38x slower                                              |
| Geometric mean | (ref)                                                                 | 1.17x slower                                                      |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 21.4 ms                                                               | 21.6 ms: 1.01x slower                                             |
| regex_dna      | 173 ms                                                                | 188 ms: 1.09x slower                                              |
| regex_compile  | 124 ms                                                                | 142 ms: 1.15x slower                                              |
| regex_effbot   | 2.61 ms                                                               | 3.14 ms: 1.20x slower                                             |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                | 142 ms: 1.01x faster                                              |
| tomli_loads          | 1.86 sec                                                              | 1.98 sec: 1.06x slower                                            |
| pickle_pure_python   | 314 us                                                                | 335 us: 1.07x slower                                              |
| xml_etree_iterparse  | 89.7 ms                                                               | 95.7 ms: 1.07x slower                                             |
| json_loads           | 27.2 us                                                               | 29.8 us: 1.10x slower                                             |
| json_dumps           | 9.70 ms                                                               | 10.7 ms: 1.10x slower                                             |
| unpickle_pure_python | 216 us                                                                | 239 us: 1.11x slower                                              |
| xml_etree_generate   | 86.3 ms                                                               | 102 ms: 1.18x slower                                              |
| xml_etree_process    | 61.3 ms                                                               | 75.8 ms: 1.24x slower                                             |
| Geometric mean       | (ref)                                                                 | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                               | 15.6 ms: 1.27x slower                                             |
| python_startup_no_site | 6.92 ms                                                               | 9.18 ms: 1.33x slower                                             |
| Geometric mean         | (ref)                                                                 | 1.30x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 35.1 ms                                                               | 41.8 ms: 1.19x slower                                             |
| mako            | 11.8 ms                                                               | 15.9 ms: 1.34x slower                                             |
| Geometric mean  | (ref)                                                                 | 1.26x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| bench_mp_pool              | 241 ms                                                                | 6.76 ms: 35.64x faster                                            |
| gc_traversal               | 3.57 ms                                                               | 1.78 ms: 2.01x faster                                             |
| create_gc_cycles           | 1.68 ms                                                               | 1.37 ms: 1.23x faster                                             |
| sqlite_synth               | 2.24 us                                                               | 1.96 us: 1.15x faster                                             |
| async_tree_io_tg           | 761 ms                                                                | 681 ms: 1.12x faster                                              |
| asyncio_websockets         | 544 ms                                                                | 513 ms: 1.06x faster                                              |
| async_tree_io              | 721 ms                                                                | 709 ms: 1.02x faster                                              |
| xml_etree_parse            | 144 ms                                                                | 142 ms: 1.01x faster                                              |
| regex_v8                   | 21.4 ms                                                               | 21.6 ms: 1.01x slower                                             |
| pathlib                    | 17.8 ms                                                               | 17.9 ms: 1.01x slower                                             |
| pycparser                  | 1.19 sec                                                              | 1.20 sec: 1.01x slower                                            |
| dulwich_log                | 68.9 ms                                                               | 70.4 ms: 1.02x slower                                             |
| async_tree_cpu_io_mixed_tg | 559 ms                                                                | 578 ms: 1.03x slower                                              |
| coroutines                 | 24.1 ms                                                               | 25.0 ms: 1.04x slower                                             |
| bpe_tokeniser              | 4.21 sec                                                              | 4.42 sec: 1.05x slower                                            |
| json                       | 5.00 ms                                                               | 5.26 ms: 1.05x slower                                             |
| tomli_loads                | 1.86 sec                                                              | 1.98 sec: 1.06x slower                                            |
| pickle_pure_python         | 314 us                                                                | 335 us: 1.07x slower                                              |
| xml_etree_iterparse        | 89.7 ms                                                               | 95.7 ms: 1.07x slower                                             |
| deltablue                  | 3.47 ms                                                               | 3.73 ms: 1.07x slower                                             |
| logging_silent             | 101 ns                                                                | 108 ns: 1.07x slower                                              |
| telco                      | 163 ms                                                                | 175 ms: 1.08x slower                                              |
| async_tree_memoization_tg  | 365 ms                                                                | 394 ms: 1.08x slower                                              |
| async_tree_none_tg         | 299 ms                                                                | 324 ms: 1.08x slower                                              |
| scimark_fft                | 320 ms                                                                | 348 ms: 1.09x slower                                              |
| regex_dna                  | 173 ms                                                                | 188 ms: 1.09x slower                                              |
| bench_thread_pool          | 1.36 ms                                                               | 1.48 ms: 1.09x slower                                             |
| json_loads                 | 27.2 us                                                               | 29.8 us: 1.10x slower                                             |
| pprint_safe_repr           | 734 ms                                                                | 807 ms: 1.10x slower                                              |
| comprehensions             | 16.0 us                                                               | 17.6 us: 1.10x slower                                             |
| json_dumps                 | 9.70 ms                                                               | 10.7 ms: 1.10x slower                                             |
| unpickle_pure_python       | 216 us                                                                | 239 us: 1.11x slower                                              |
| many_optionals             | 917 us                                                                | 1.01 ms: 1.11x slower                                             |
| scimark_sor                | 111 ms                                                                | 123 ms: 1.11x slower                                              |
| async_tree_cpu_io_mixed    | 544 ms                                                                | 605 ms: 1.11x slower                                              |
| async_tree_memoization     | 378 ms                                                                | 420 ms: 1.11x slower                                              |
| subparsers                 | 9.37 ms                                                               | 10.4 ms: 1.11x slower                                             |
| pyflate                    | 414 ms                                                                | 463 ms: 1.12x slower                                              |
| spectral_norm              | 97.9 ms                                                               | 110 ms: 1.12x slower                                              |
| k_core                     | 2.03 sec                                                              | 2.28 sec: 1.12x slower                                            |
| html5lib                   | 60.8 ms                                                               | 68.6 ms: 1.13x slower                                             |
| pprint_pformat             | 1.49 sec                                                              | 1.68 sec: 1.13x slower                                            |
| chaos                      | 55.7 ms                                                               | 62.9 ms: 1.13x slower                                             |
| hexiom                     | 5.89 ms                                                               | 6.66 ms: 1.13x slower                                             |
| sphinx                     | 978 ms                                                                | 1.11 sec: 1.13x slower                                            |
| go                         | 108 ms                                                                | 122 ms: 1.13x slower                                              |
| sqlglot_v2_optimize        | 51.2 ms                                                               | 58.0 ms: 1.13x slower                                             |
| deepcopy_reduce            | 2.58 us                                                               | 2.94 us: 1.14x slower                                             |
| sqlglot_v2_normalize       | 101 ms                                                                | 115 ms: 1.14x slower                                              |
| async_generators           | 342 ms                                                                | 390 ms: 1.14x slower                                              |
| 2to3                       | 259 ms                                                                | 297 ms: 1.15x slower                                              |
| deepcopy                   | 232 us                                                                | 267 us: 1.15x slower                                              |
| generators                 | 28.7 ms                                                               | 33.1 ms: 1.15x slower                                             |
| regex_compile              | 124 ms                                                                | 142 ms: 1.15x slower                                              |
| sympy_integrate            | 19.0 ms                                                               | 21.9 ms: 1.15x slower                                             |
| float                      | 75.0 ms                                                               | 86.9 ms: 1.16x slower                                             |
| scimark_lu                 | 112 ms                                                                | 130 ms: 1.16x slower                                              |
| sympy_expand               | 458 ms                                                                | 531 ms: 1.16x slower                                              |
| thrift                     | 791 us                                                                | 919 us: 1.16x slower                                              |
| mdp                        | 1.13 sec                                                              | 1.32 sec: 1.16x slower                                            |
| sympy_sum                  | 156 ms                                                                | 181 ms: 1.16x slower                                              |
| pylint                     | 115 ms                                                                | 134 ms: 1.17x slower                                              |
| async_tree_none            | 295 ms                                                                | 345 ms: 1.17x slower                                              |
| sympy_str                  | 273 ms                                                                | 318 ms: 1.17x slower                                              |
| scimark_sparse_mat_mult    | 4.53 ms                                                               | 5.30 ms: 1.17x slower                                             |
| logging_simple             | 6.10 us                                                               | 7.16 us: 1.18x slower                                             |
| deepcopy_memo              | 26.6 us                                                               | 31.4 us: 1.18x slower                                             |
| xml_etree_generate         | 86.3 ms                                                               | 102 ms: 1.18x slower                                              |
| sqlglot_v2_transpile       | 1.46 ms                                                               | 1.73 ms: 1.19x slower                                             |
| raytrace                   | 259 ms                                                                | 307 ms: 1.19x slower                                              |
| nqueens                    | 74.2 ms                                                               | 88.0 ms: 1.19x slower                                             |
| logging_format             | 6.77 us                                                               | 8.05 us: 1.19x slower                                             |
| django_template            | 35.1 ms                                                               | 41.8 ms: 1.19x slower                                             |
| fannkuch                   | 384 ms                                                                | 458 ms: 1.19x slower                                              |
| regex_effbot               | 2.61 ms                                                               | 3.14 ms: 1.20x slower                                             |
| sqlglot_v2_parse           | 1.17 ms                                                               | 1.41 ms: 1.21x slower                                             |
| richards                   | 43.7 ms                                                               | 53.1 ms: 1.21x slower                                             |
| connected_components       | 401 ms                                                                | 489 ms: 1.22x slower                                              |
| docutils                   | 2.40 sec                                                              | 2.93 sec: 1.22x slower                                            |
| shortest_path              | 443 ms                                                                | 541 ms: 1.22x slower                                              |
| richards_super             | 49.5 ms                                                               | 60.7 ms: 1.23x slower                                             |
| xml_etree_process          | 61.3 ms                                                               | 75.8 ms: 1.24x slower                                             |
| scimark_monte_carlo        | 64.6 ms                                                               | 80.0 ms: 1.24x slower                                             |
| typing_runtime_protocols   | 117 us                                                                | 147 us: 1.26x slower                                              |
| python_startup             | 12.3 ms                                                               | 15.6 ms: 1.27x slower                                             |
| meteor_contest             | 101 ms                                                                | 129 ms: 1.28x slower                                              |
| crypto_pyaes               | 70.2 ms                                                               | 90.4 ms: 1.29x slower                                             |
| python_startup_no_site     | 6.92 ms                                                               | 9.18 ms: 1.33x slower                                             |
| mako                       | 11.8 ms                                                               | 15.9 ms: 1.34x slower                                             |
| coverage                   | 84.2 ms                                                               | 115 ms: 1.37x slower                                              |
| nbody                      | 90.5 ms                                                               | 125 ms: 1.38x slower                                              |
| Geometric mean             | (ref)                                                                 | 1.07x slower                                                      |

Benchmark hidden because not significant (1): pidigits

- Geometric mean (including insignificant results): 1.106x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x