# Results vs. 3.12.6

- fork: python
- ref: c461aa99e2fabbaf5859
- machine: linux-x86_64
- commit hash: c461aa9
- commit date: 2026-01-15
- overall geometric mean: 1.074x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.2 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.96x faster                                                   |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 306 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 477 ms: 1.50x faster                                                   |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.1 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 91.4 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.58 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                  |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 554 ms: 1.96x faster                                                   |
| async_tree_none            | 464 ms                                                 | 243 ms: 1.91x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 306 ms: 1.82x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 477 ms: 1.50x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.9 us: 1.50x faster                                                  |
| deepcopy                   | 352 us                                                 | 238 us: 1.48x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.23x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.6 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.0 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.9 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 71.1 ms: 1.14x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.9 ms: 1.12x faster                                                  |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                  |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                   |
| logging_format             | 7.35 us                                                | 6.59 us: 1.11x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 69.7 ms: 1.10x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.2 ms: 1.10x faster                                                  |
| pyflate                    | 448 ms                                                 | 409 ms: 1.10x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.65 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.58 ms: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.2 ms: 1.07x faster                                                  |
| richards                   | 45.9 ms                                                | 42.8 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.8 ms: 1.06x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.6 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 702 ms: 1.06x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.32 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                   |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.2 ms: 1.01x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 49.7 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.37 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.28 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                  |
| nbody                      | 89.3 ms                                                | 91.4 ms: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                   |
| sympy_expand               | 468 ms                                                 | 491 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                  |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.5 ms: 1.14x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.00 ms: 1.16x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.45x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 283 ms: 26.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260115-3.15.0a5+-c461aa9/bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x