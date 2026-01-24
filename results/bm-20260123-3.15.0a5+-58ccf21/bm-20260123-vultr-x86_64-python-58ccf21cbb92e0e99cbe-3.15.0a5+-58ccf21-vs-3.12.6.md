# Results vs. 3.12.6

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: linux-x86_64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 559 ms: 1.99x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 546 ms: 1.98x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 495 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                   |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.6 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 90.9 ms: 1.02x slower                                                  |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 85.1 ms: 1.14x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.54 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.27 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| genshi_xml     | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                  |
| mako           | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 559 ms: 1.99x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 546 ms: 1.98x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 304 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                   |
| deepcopy                   | 352 us                                                 | 230 us: 1.53x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.4 us: 1.52x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 495 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 491 ms: 1.46x faster                                                   |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                   |
| scimark_sor                | 130 ms                                                 | 104 ms: 1.25x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.3 ms: 1.24x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                   |
| spectral_norm              | 110 ms                                                 | 92.8 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.7 ms: 1.18x faster                                                  |
| regex_compile              | 142 ms                                                 | 122 ms: 1.17x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.6 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 85.1 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 283 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 56.1 ms: 1.12x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.96 us: 1.11x faster                                                  |
| scimark_fft                | 342 ms                                                 | 308 ms: 1.11x faster                                                   |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.62 ms: 1.10x faster                                                  |
| richards                   | 45.9 ms                                                | 42.1 ms: 1.09x faster                                                  |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                                   |
| logging_format             | 7.35 us                                                | 6.75 us: 1.09x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.9 ms: 1.09x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.54 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.1 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                   |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 709 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 757 us: 1.05x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 82.0 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.33 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.7 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.27 ms: 1.01x slower                                                  |
| nbody                      | 89.3 ms                                                | 90.9 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                  |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                   |
| sympy_expand               | 468 ms                                                 | 491 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.29 ms: 1.24x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.30 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 255 ms: 23.59x slower                                                  |
| telco                      | 6.53 ms                                                | 156 ms: 23.91x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): django_template
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260123-3.15.0a5+-58ccf21/bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x