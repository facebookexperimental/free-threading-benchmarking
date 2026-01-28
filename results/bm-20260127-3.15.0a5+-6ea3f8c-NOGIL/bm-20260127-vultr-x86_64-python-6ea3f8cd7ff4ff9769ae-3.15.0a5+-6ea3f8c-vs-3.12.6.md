# Results vs. 3.12.6

- fork: python
- ref: 6ea3f8cd7ff4ff9769ae
- machine: linux-x86_64
- commit hash: 6ea3f8c
- commit date: 2026-01-27
- overall geometric mean: 1.032x slower
- HPT reliability: 85.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                   |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 66.3 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 627 ms: 1.73x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 331 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 267 ms: 1.67x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.28x faster                                                   |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.5 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| nbody          | 89.3 ms                                                | 127 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| regex_compile  | 142 ms                                                 | 140 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.1 ms: 1.08x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                  |
| django_template | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                  |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 627 ms: 1.73x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 331 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 267 ms: 1.67x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 359 ms: 1.55x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.08 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 537 ms: 1.35x faster                                                   |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 561 ms: 1.28x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                                  |
| float                      | 80.8 ms                                                | 73.5 ms: 1.10x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.2 us: 1.09x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.88 us: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.07x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.45 sec: 1.06x faster                                                 |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pylint                     | 319 ms                                                 | 303 ms: 1.05x faster                                                   |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| regex_compile              | 142 ms                                                 | 140 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| generators                 | 32.2 ms                                                | 32.4 ms: 1.00x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.2 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                   |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 770 ms: 1.04x slower                                                   |
| scimark_fft                | 342 ms                                                 | 355 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.3 ms: 1.04x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.46 ms: 1.05x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.95 us: 1.05x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 175 ms: 1.05x slower                                                   |
| sympy_str                  | 292 ms                                                 | 307 ms: 1.05x slower                                                   |
| pyflate                    | 448 ms                                                 | 472 ms: 1.05x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 21.7 ms: 1.05x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.64 ms: 1.06x slower                                                  |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 54.1 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                   |
| logging_format             | 7.35 us                                                | 7.99 us: 1.09x slower                                                  |
| json                       | 5.02 ms                                                | 5.47 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                   |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                   |
| nqueens                    | 80.1 ms                                                | 89.4 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 885 us: 1.12x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 52.2 ms: 1.14x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.0 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.4 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.4 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.17x slower                                                  |
| django_template            | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                                   |
| meteor_contest             | 104 ms                                                 | 124 ms: 1.19x slower                                                   |
| json_loads                 | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 462 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.52 ms: 1.26x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.37x slower                                                  |
| nbody                      | 89.3 ms                                                | 127 ms: 1.43x slower                                                   |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.56x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 174 ms: 26.70x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260127-3.15.0a5+-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5+-6ea3f8c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x slower

# HPT report

- Reliability score: 85.32% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x