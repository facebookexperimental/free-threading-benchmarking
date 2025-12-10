# Results vs. 3.12.6

- fork: python
- ref: 726e8e8defc487c55ade
- machine: linux-x86_64
- commit hash: 726e8e8
- commit date: 2025-12-08
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                   |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| nbody          | 89.3 ms                                                | 85.3 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.62 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 57.4 ms: 1.03x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.18 sec: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                  |
| mako           | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 244 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 27.1 us: 1.49x faster                                                  |
| deepcopy                   | 352 us                                                 | 245 us: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                   |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.25x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.23x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.9 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.2 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 97.0 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.5 ms: 1.12x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.95 us: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 61.5 ms: 1.11x faster                                                  |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                                   |
| genshi_text                | 22.8 ms                                                | 20.5 ms: 1.11x faster                                                  |
| pyflate                    | 448 ms                                                 | 403 ms: 1.11x faster                                                   |
| logging_format             | 7.35 us                                                | 6.66 us: 1.10x faster                                                  |
| logging_silent             | 109 ns                                                 | 99.4 ns: 1.10x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.72 ms: 1.08x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.62 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.5 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 247 ms: 1.07x faster                                                   |
| richards                   | 45.9 ms                                                | 43.1 ms: 1.07x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                   |
| html5lib                   | 63.6 ms                                                | 60.0 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.05x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                  |
| nbody                      | 89.3 ms                                                | 85.3 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 759 us: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.6 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.34 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.4 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.03x faster                                                   |
| nqueens                    | 80.1 ms                                                | 78.5 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.32 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 481 ms: 1.03x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.18 sec: 1.04x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.29 us: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| pidigits                   | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.12 ms: 1.19x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| telco                      | 6.53 ms                                                | 159 ms: 24.36x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 320 ms: 29.66x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): django_template, pickle_pure_python
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251208-3.15.0a2+-726e8e8/bm-20251208-vultr-x86_64-python-726e8e8defc487c55ade-3.15.0a2+-726e8e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x