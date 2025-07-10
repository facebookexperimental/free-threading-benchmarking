# Results vs. 3.12.6

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: linux-x86_64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.027x slower
- HPT reliability: 94.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.0 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.96x faster                                                  |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 204 ms: 1.11x slower                                                  |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 339 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.5 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.96x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                                 |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 490 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 517 ms: 1.38x faster                                                  |
| deepcopy                   | 352 us                                                 | 294 us: 1.20x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| float                      | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                  |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.7 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.12 us: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| raytrace                   | 299 ms                                                 | 307 ms: 1.03x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.34 ms: 1.03x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.56 ms: 1.03x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.18 sec: 1.03x slower                                                |
| html5lib                   | 63.6 ms                                                | 66.0 ms: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 467 ms: 1.04x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 777 ms: 1.05x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                |
| logging_format             | 7.35 us                                                | 7.88 us: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| scimark_fft                | 342 ms                                                 | 374 ms: 1.10x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.0 ms: 1.10x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 339 us: 1.10x slower                                                  |
| pidigits                   | 184 ms                                                 | 204 ms: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 878 us: 1.11x slower                                                  |
| richards                   | 45.9 ms                                                | 51.3 ms: 1.12x slower                                                 |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.7 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| richards_super             | 51.9 ms                                                | 58.8 ms: 1.13x slower                                                 |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.13x slower                                                  |
| django_template            | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 78.5 ms: 1.15x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.5 ms: 1.15x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 188 us: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.9 ms: 1.18x slower                                                 |
| fannkuch                   | 372 ms                                                 | 463 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.34x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.03x slower                                                 |
| telco                      | 6.53 ms                                                | 178 ms: 27.29x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (2): pylint, regex_compile
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 94.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x