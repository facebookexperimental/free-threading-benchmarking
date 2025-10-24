# Results vs. base

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.008x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 247 ms: 1.00x faster                                                 |
| html5lib       | 61.6 ms                                                                | 62.5 ms: 1.01x slower                                                |
| sphinx         | 977 ms                                                                 | 970 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                         |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators          | 344 ms                                                                 | 346 ms: 1.01x slower                                                 |
| async_tree_memoization_tg | 308 ms                                                                 | 310 ms: 1.01x slower                                                 |
| async_tree_io_tg          | 588 ms                                                                 | 594 ms: 1.01x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                                         |

Benchmark hidden because not significant (8): asyncio_websockets, async_tree_none, async_tree_cpu_io_mixed, coroutines, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 209 ms                                                                 | 201 ms: 1.04x faster                                                 |
| nbody          | 90.6 ms                                                                | 87.7 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 184 ms                                                                 | 169 ms: 1.09x faster                                                 |
| regex_v8       | 22.9 ms                                                                | 21.2 ms: 1.08x faster                                                |
| regex_effbot   | 2.87 ms                                                                | 2.69 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                         |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_dumps           | 9.63 ms                                                                | 9.49 ms: 1.01x faster                                                |
| unpickle_pure_python | 211 us                                                                 | 208 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 85.3 ms                                                                | 84.2 ms: 1.01x faster                                                |
| json_loads           | 28.1 us                                                                | 27.8 us: 1.01x faster                                                |
| tomli_loads          | 1.92 sec                                                               | 1.91 sec: 1.01x faster                                               |
| xml_etree_generate   | 82.3 ms                                                                | 82.5 ms: 1.00x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.26 ms                                                                | 7.20 ms: 1.01x faster                                                |
| python_startup         | 12.4 ms                                                                | 12.3 ms: 1.01x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                |
| django_template | 34.6 ms                                                                | 34.1 ms: 1.01x faster                                                |
| genshi_text     | 20.7 ms                                                                | 20.4 ms: 1.01x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20251024-vultr-x86_64-python-95e5d596308620acbd86-3.15.0a1+-95e5d59 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna                 | 184 ms                                                                 | 169 ms: 1.09x faster                                                 |
| regex_v8                  | 22.9 ms                                                                | 21.2 ms: 1.08x faster                                                |
| regex_effbot              | 2.87 ms                                                                | 2.69 ms: 1.07x faster                                                |
| spectral_norm             | 97.5 ms                                                                | 92.6 ms: 1.05x faster                                                |
| logging_format            | 6.71 us                                                                | 6.46 us: 1.04x faster                                                |
| pidigits                  | 209 ms                                                                 | 201 ms: 1.04x faster                                                 |
| json                      | 5.12 ms                                                                | 4.94 ms: 1.04x faster                                                |
| logging_silent            | 99.3 ns                                                                | 95.9 ns: 1.04x faster                                                |
| nbody                     | 90.6 ms                                                                | 87.7 ms: 1.03x faster                                                |
| hexiom                    | 5.72 ms                                                                | 5.54 ms: 1.03x faster                                                |
| pyflate                   | 418 ms                                                                 | 407 ms: 1.03x faster                                                 |
| pprint_safe_repr          | 703 ms                                                                 | 683 ms: 1.03x faster                                                 |
| go                        | 106 ms                                                                 | 103 ms: 1.03x faster                                                 |
| logging_simple            | 5.91 us                                                                | 5.75 us: 1.03x faster                                                |
| richards_super            | 47.4 ms                                                                | 46.4 ms: 1.02x faster                                                |
| deepcopy_memo             | 26.5 us                                                                | 25.9 us: 1.02x faster                                                |
| pprint_pformat            | 1.42 sec                                                               | 1.39 sec: 1.02x faster                                               |
| scimark_sor               | 107 ms                                                                 | 105 ms: 1.02x faster                                                 |
| chaos                     | 56.4 ms                                                                | 55.3 ms: 1.02x faster                                                |
| fannkuch                  | 395 ms                                                                 | 388 ms: 1.02x faster                                                 |
| richards                  | 41.4 ms                                                                | 40.7 ms: 1.02x faster                                                |
| scimark_fft               | 314 ms                                                                 | 308 ms: 1.02x faster                                                 |
| bpe_tokeniser             | 4.24 sec                                                               | 4.17 sec: 1.02x faster                                               |
| telco                     | 158 ms                                                                 | 155 ms: 1.02x faster                                                 |
| deepcopy                  | 245 us                                                                 | 241 us: 1.02x faster                                                 |
| sympy_str                 | 278 ms                                                                 | 274 ms: 1.02x faster                                                 |
| json_dumps                | 9.63 ms                                                                | 9.49 ms: 1.01x faster                                                |
| unpickle_pure_python      | 211 us                                                                 | 208 us: 1.01x faster                                                 |
| pycparser                 | 1.08 sec                                                               | 1.07 sec: 1.01x faster                                               |
| mako                      | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                |
| django_template           | 34.6 ms                                                                | 34.1 ms: 1.01x faster                                                |
| xml_etree_iterparse       | 85.3 ms                                                                | 84.2 ms: 1.01x faster                                                |
| comprehensions            | 15.8 us                                                                | 15.6 us: 1.01x faster                                                |
| genshi_text               | 20.7 ms                                                                | 20.4 ms: 1.01x faster                                                |
| raytrace                  | 250 ms                                                                 | 247 ms: 1.01x faster                                                 |
| sqlglot_v2_parse          | 1.20 ms                                                                | 1.18 ms: 1.01x faster                                                |
| scimark_lu                | 111 ms                                                                 | 110 ms: 1.01x faster                                                 |
| json_loads                | 28.1 us                                                                | 27.8 us: 1.01x faster                                                |
| python_startup_no_site    | 7.26 ms                                                                | 7.20 ms: 1.01x faster                                                |
| sphinx                    | 977 ms                                                                 | 970 ms: 1.01x faster                                                 |
| meteor_contest            | 99.9 ms                                                                | 99.2 ms: 1.01x faster                                                |
| python_startup            | 12.4 ms                                                                | 12.3 ms: 1.01x faster                                                |
| mdp                       | 1.15 sec                                                               | 1.14 sec: 1.01x faster                                               |
| tomli_loads               | 1.92 sec                                                               | 1.91 sec: 1.01x faster                                               |
| deepcopy_reduce           | 2.60 us                                                                | 2.58 us: 1.01x faster                                                |
| sympy_integrate           | 19.1 ms                                                                | 19.0 ms: 1.01x faster                                                |
| crypto_pyaes              | 68.9 ms                                                                | 68.5 ms: 1.01x faster                                                |
| sqlglot_v2_optimize       | 50.8 ms                                                                | 50.6 ms: 1.00x faster                                                |
| 2to3                      | 249 ms                                                                 | 247 ms: 1.00x faster                                                 |
| bench_thread_pool         | 999 us                                                                 | 995 us: 1.00x faster                                                 |
| xml_etree_generate        | 82.3 ms                                                                | 82.5 ms: 1.00x slower                                                |
| nqueens                   | 78.3 ms                                                                | 78.6 ms: 1.00x slower                                                |
| async_generators          | 344 ms                                                                 | 346 ms: 1.01x slower                                                 |
| async_tree_memoization_tg | 308 ms                                                                 | 310 ms: 1.01x slower                                                 |
| thrift                    | 747 us                                                                 | 754 us: 1.01x slower                                                 |
| async_tree_io_tg          | 588 ms                                                                 | 594 ms: 1.01x slower                                                 |
| html5lib                  | 61.6 ms                                                                | 62.5 ms: 1.01x slower                                                |
| pathlib                   | 17.6 ms                                                                | 17.8 ms: 1.01x slower                                                |
| coverage                  | 80.6 ms                                                                | 82.5 ms: 1.02x slower                                                |
| deltablue                 | 3.08 ms                                                                | 3.20 ms: 1.04x slower                                                |
| gc_traversal              | 4.19 ms                                                                | 4.79 ms: 1.14x slower                                                |
| Geometric mean            | (ref)                                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (33): sympy_expand, sqlite_synth, float, connected_components, typing_runtime_protocols, sqlglot_v2_normalize, sympy_sum, docutils, shortest_path, k_core, subparsers, generators, asyncio_websockets, scimark_sparse_mat_mult, pylint, many_optionals, scimark_monte_carlo, xml_etree_process, regex_compile, dulwich_log, pickle_pure_python, async_tree_none, genshi_xml, bench_mp_pool, xml_etree_parse, async_tree_cpu_io_mixed, coroutines, async_tree_cpu_io_mixed_tg, async_tree_none_tg, create_gc_cycles, async_tree_memoization, sqlglot_v2_transpile, async_tree_io

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x