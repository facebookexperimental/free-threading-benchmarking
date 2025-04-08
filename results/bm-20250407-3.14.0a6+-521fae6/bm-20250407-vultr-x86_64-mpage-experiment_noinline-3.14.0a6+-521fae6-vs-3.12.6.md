# Results vs. 3.12.6

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.121x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.07x faster                                                 |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                               |
| Geometric mean | (ref)                                                  | 1.06x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 609 ms: 1.82x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                 |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                 |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.4 ms: 1.18x faster                                                |
| nbody          | 89.3 ms                                                | 84.2 ms: 1.06x faster                                                |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                 |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.08x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.87 sec: 1.13x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.06x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                |
| pickle_pure_python   | 308 us                                                 | 300 us: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.63 ms: 1.21x slower                                                |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                |
| genshi_xml     | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                |
| mako           | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.13x faster                                               |
| async_tree_io_tg           | 1.11 sec                                               | 609 ms: 1.82x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                 |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 28.3 us: 1.43x faster                                                |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                 |
| go                         | 139 ms                                                 | 107 ms: 1.30x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.22x faster                                                |
| raytrace                   | 299 ms                                                 | 246 ms: 1.21x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                |
| spectral_norm              | 110 ms                                                 | 91.8 ms: 1.20x faster                                                |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                |
| chaos                      | 62.8 ms                                                | 52.7 ms: 1.19x faster                                                |
| float                      | 80.8 ms                                                | 68.4 ms: 1.18x faster                                                |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                |
| logging_silent             | 109 ns                                                 | 92.5 ns: 1.18x faster                                                |
| dulwich_log                | 78.9 ms                                                | 67.1 ms: 1.18x faster                                                |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                 |
| pylint                     | 319 ms                                                 | 278 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 60.0 ms: 1.14x faster                                                |
| richards                   | 45.9 ms                                                | 40.3 ms: 1.14x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.87 sec: 1.13x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                               |
| richards_super             | 51.9 ms                                                | 46.2 ms: 1.12x faster                                                |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                                 |
| pyflate                    | 448 ms                                                 | 405 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                |
| scimark_fft                | 342 ms                                                 | 309 ms: 1.10x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.8 ms: 1.10x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                 |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.19 ms: 1.08x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                               |
| pprint_safe_repr           | 743 ms                                                 | 695 ms: 1.07x faster                                                 |
| 2to3                       | 264 ms                                                 | 247 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                               |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.06x faster                                                 |
| nqueens                    | 80.1 ms                                                | 75.5 ms: 1.06x faster                                                |
| nbody                      | 89.3 ms                                                | 84.2 ms: 1.06x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                |
| meteor_contest             | 104 ms                                                 | 98.0 ms: 1.06x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                               |
| genshi_xml                 | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                |
| pickle_pure_python         | 308 us                                                 | 300 us: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                 |
| json                       | 5.02 ms                                                | 4.92 ms: 1.02x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.02x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| fannkuch                   | 372 ms                                                 | 374 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                |
| telco                      | 6.53 ms                                                | 7.04 ms: 1.08x slower                                                |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                |
| coverage                   | 71.4 ms                                                | 81.4 ms: 1.14x slower                                                |
| gc_traversal               | 3.46 ms                                                | 4.03 ms: 1.16x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 8.63 ms: 1.21x slower                                                |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 88.3 ms: 8.18x slower                                                |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_process, django_template
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-521fae6/bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.121x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.12x