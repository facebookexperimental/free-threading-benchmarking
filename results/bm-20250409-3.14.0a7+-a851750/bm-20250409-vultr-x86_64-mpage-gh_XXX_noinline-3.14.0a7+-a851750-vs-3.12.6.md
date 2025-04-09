# Results vs. 3.12.6

- fork: mpage
- ref: gh_XXX_noinline
- machine: linux-x86_64
- commit hash: a851750
- commit date: 2025-04-09
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                             |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                           |
| Geometric mean | (ref)                                                  | 1.06x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                             |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                             |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                             |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                             |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                             |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.2 ms: 1.17x faster                                            |
| nbody          | 89.3 ms                                                | 84.9 ms: 1.05x faster                                            |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                             |
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                            |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.07x slower                                            |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.12x faster                                           |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                             |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                            |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                             |
| pickle_pure_python   | 308 us                                                 | 303 us: 1.02x faster                                             |
| xml_etree_generate   | 85.2 ms                                                | 83.9 ms: 1.02x faster                                            |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                            |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                     |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.62 ms: 1.20x slower                                            |
| python_startup         | 9.93 ms                                                | 15.0 ms: 1.51x slower                                            |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.3 ms: 1.12x faster                                            |
| genshi_xml      | 50.2 ms                                                | 47.6 ms: 1.05x faster                                            |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                            |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.13x faster                                           |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                             |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.80x faster                                             |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                             |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                             |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                             |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 29.5 us: 1.37x faster                                            |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                             |
| raytrace                   | 299 ms                                                 | 246 ms: 1.21x faster                                             |
| spectral_norm              | 110 ms                                                 | 91.3 ms: 1.21x faster                                            |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                            |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                             |
| chaos                      | 62.8 ms                                                | 52.6 ms: 1.19x faster                                            |
| comprehensions             | 19.8 us                                                | 16.6 us: 1.19x faster                                            |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                             |
| dulwich_log                | 78.9 ms                                                | 67.0 ms: 1.18x faster                                            |
| float                      | 80.8 ms                                                | 69.2 ms: 1.17x faster                                            |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                            |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                             |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                             |
| crypto_pyaes               | 76.6 ms                                                | 67.1 ms: 1.14x faster                                            |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 60.0 ms: 1.14x faster                                            |
| richards                   | 45.9 ms                                                | 40.7 ms: 1.13x faster                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                           |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                             |
| genshi_text                | 22.8 ms                                                | 20.3 ms: 1.12x faster                                            |
| logging_silent             | 109 ns                                                 | 97.4 ns: 1.12x faster                                            |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.12x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                            |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                            |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                             |
| richards_super             | 51.9 ms                                                | 46.8 ms: 1.11x faster                                            |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                            |
| logging_simple             | 6.63 us                                                | 5.99 us: 1.11x faster                                            |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.11x faster                                             |
| hexiom                     | 6.17 ms                                                | 5.64 ms: 1.09x faster                                            |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                            |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                             |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.07x faster                                             |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                            |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                             |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                           |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                            |
| genshi_xml                 | 50.2 ms                                                | 47.6 ms: 1.05x faster                                            |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.05x faster                                           |
| nqueens                    | 80.1 ms                                                | 76.1 ms: 1.05x faster                                            |
| nbody                      | 89.3 ms                                                | 84.9 ms: 1.05x faster                                            |
| pprint_safe_repr           | 743 ms                                                 | 707 ms: 1.05x faster                                             |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                           |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                            |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                             |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                             |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.02x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                            |
| pickle_pure_python         | 308 us                                                 | 303 us: 1.02x faster                                             |
| xml_etree_generate         | 85.2 ms                                                | 83.9 ms: 1.02x faster                                            |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.37 ms: 1.00x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                             |
| django_template            | 34.7 ms                                                | 34.9 ms: 1.01x slower                                            |
| fannkuch                   | 372 ms                                                 | 375 ms: 1.01x slower                                             |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                            |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                            |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.07x slower                                            |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                             |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                            |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                             |
| telco                      | 6.53 ms                                                | 7.15 ms: 1.09x slower                                            |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                            |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                            |
| coverage                   | 71.4 ms                                                | 79.7 ms: 1.12x slower                                            |
| python_startup_no_site     | 7.16 ms                                                | 8.62 ms: 1.20x slower                                            |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                            |
| python_startup             | 9.93 ms                                                | 15.0 ms: 1.51x slower                                            |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                            |
| bench_mp_pool              | 10.8 ms                                                | 88.2 ms: 8.17x slower                                            |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                     |

Benchmark hidden because not significant (2): xml_etree_process, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250409-3.14.0a7+-a851750/bm-20250409-vultr-x86_64-mpage-gh_XXX_noinline-3.14.0a7+-a851750.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x