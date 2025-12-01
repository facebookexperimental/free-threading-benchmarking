# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                   |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                 |
| html5lib       | 63.6 ms                                                | 67.6 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                   |
| async_tree_io_tg           | 1.11 sec                                               | 595 ms: 1.86x faster                                   |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                   |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                   |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                   |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                   |
| Geometric mean             | (ref)                                                  | 1.50x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 80.8 ms                                                | 59.9 ms: 1.35x faster                                  |
| nbody          | 89.3 ms                                                | 88.0 ms: 1.01x faster                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.18x faster                                  |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                   |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                   |
| regex_v8       | 20.6 ms                                                | 22.5 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.20x faster                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 82.0 ms: 1.18x faster                                  |
| tomli_loads          | 2.11 sec                                               | 1.82 sec: 1.16x faster                                 |
| json_dumps           | 10.4 ms                                                | 9.06 ms: 1.14x faster                                  |
| xml_etree_generate   | 85.2 ms                                                | 77.4 ms: 1.10x faster                                  |
| xml_etree_process    | 59.0 ms                                                | 53.6 ms: 1.10x faster                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                   |
| pickle_pure_python   | 308 us                                                 | 293 us: 1.05x faster                                   |
| json_loads           | 26.5 us                                                | 28.8 us: 1.09x slower                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.23 ms: 1.01x slower                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                  |
| mako            | 11.0 ms                                                | 10.4 ms: 1.05x faster                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                  |
| genshi_xml      | 50.2 ms                                                | 56.1 ms: 1.12x slower                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.9 ms: 2.20x faster                                  |
| richards_super             | 51.9 ms                                                | 25.6 ms: 2.03x faster                                  |
| async_tree_io              | 1.08 sec                                               | 563 ms: 1.92x faster                                   |
| async_tree_none            | 464 ms                                                 | 248 ms: 1.87x faster                                   |
| async_tree_io_tg           | 1.11 sec                                               | 595 ms: 1.86x faster                                   |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                 |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                   |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                   |
| deepcopy_memo              | 40.3 us                                                | 25.0 us: 1.61x faster                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 489 ms: 1.48x faster                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                   |
| deepcopy                   | 352 us                                                 | 247 us: 1.42x faster                                   |
| float                      | 80.8 ms                                                | 59.9 ms: 1.35x faster                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                   |
| scimark_fft                | 342 ms                                                 | 257 ms: 1.33x faster                                   |
| scimark_sor                | 130 ms                                                 | 98.6 ms: 1.32x faster                                  |
| spectral_norm              | 110 ms                                                 | 84.5 ms: 1.30x faster                                  |
| logging_silent             | 109 ns                                                 | 85.3 ns: 1.28x faster                                  |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 55.8 ms: 1.23x faster                                  |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                  |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.20x faster                                   |
| deltablue                  | 3.45 ms                                                | 2.87 ms: 1.20x faster                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.96 sec: 1.19x faster                                 |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.18x faster                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 82.0 ms: 1.18x faster                                  |
| pyflate                    | 448 ms                                                 | 380 ms: 1.18x faster                                   |
| tomli_loads                | 2.11 sec                                               | 1.82 sec: 1.16x faster                                 |
| chaos                      | 62.8 ms                                                | 54.5 ms: 1.15x faster                                  |
| logging_simple             | 6.63 us                                                | 5.77 us: 1.15x faster                                  |
| json_dumps                 | 10.4 ms                                                | 9.06 ms: 1.14x faster                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.1 ms: 1.14x faster                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                   |
| raytrace                   | 299 ms                                                 | 264 ms: 1.13x faster                                   |
| logging_format             | 7.35 us                                                | 6.48 us: 1.13x faster                                  |
| scimark_lu                 | 114 ms                                                 | 101 ms: 1.13x faster                                   |
| generators                 | 32.2 ms                                                | 29.1 ms: 1.11x faster                                  |
| xml_etree_generate         | 85.2 ms                                                | 77.4 ms: 1.10x faster                                  |
| xml_etree_process          | 59.0 ms                                                | 53.6 ms: 1.10x faster                                  |
| pprint_safe_repr           | 743 ms                                                 | 682 ms: 1.09x faster                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                   |
| thrift                     | 791 us                                                 | 739 us: 1.07x faster                                   |
| async_generators           | 384 ms                                                 | 360 ms: 1.07x faster                                   |
| meteor_contest             | 104 ms                                                 | 97.0 ms: 1.07x faster                                  |
| dulwich_log                | 78.9 ms                                                | 73.9 ms: 1.07x faster                                  |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                   |
| mako                       | 11.0 ms                                                | 10.4 ms: 1.05x faster                                  |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                 |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                 |
| pickle_pure_python         | 308 us                                                 | 293 us: 1.05x faster                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.23 ms: 1.04x faster                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                   |
| nbody                      | 89.3 ms                                                | 88.0 ms: 1.01x faster                                  |
| hexiom                     | 6.17 ms                                                | 6.09 ms: 1.01x faster                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.23 ms: 1.01x slower                                  |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                  |
| sympy_integrate            | 20.5 ms                                                | 21.2 ms: 1.03x slower                                  |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                   |
| sympy_sum                  | 166 ms                                                 | 175 ms: 1.05x slower                                   |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                   |
| html5lib                   | 63.6 ms                                                | 67.6 ms: 1.06x slower                                  |
| nqueens                    | 80.1 ms                                                | 85.7 ms: 1.07x slower                                  |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                   |
| sympy_expand               | 468 ms                                                 | 506 ms: 1.08x slower                                   |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.09x slower                                  |
| regex_v8                   | 20.6 ms                                                | 22.5 ms: 1.09x slower                                  |
| genshi_xml                 | 50.2 ms                                                | 56.1 ms: 1.12x slower                                  |
| coverage                   | 71.4 ms                                                | 81.4 ms: 1.14x slower                                  |
| bench_thread_pool          | 941 us                                                 | 1.10 ms: 1.16x slower                                  |
| bench_mp_pool              | 10.8 ms                                                | 13.0 ms: 1.21x slower                                  |
| gc_traversal               | 3.46 ms                                                | 4.27 ms: 1.24x slower                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.90 ms: 1.74x slower                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.50x slower                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                           |

Benchmark hidden because not significant (4): pylint, fannkuch, json, sqlite_synth
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251124-3.15.0a2+-dc62b62-JIT/bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x