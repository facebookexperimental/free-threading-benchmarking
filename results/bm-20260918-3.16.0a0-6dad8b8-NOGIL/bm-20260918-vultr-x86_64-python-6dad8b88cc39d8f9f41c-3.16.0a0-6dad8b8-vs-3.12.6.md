# Results vs. 3.12.6

- fork: python
- ref: 6dad8b88cc39d8f9f41c
- machine: linux-x86_64
- commit hash: 6dad8b8
- commit date: 2026-09-18
- overall geometric mean: 1.044x slower
- HPT reliability: 87.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| docutils       | 2.64 sec                                               | 2.94 sec: 1.12x slower                                                |
| html5lib       | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 728 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 406 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                  |
| async_tree_none            | 464 ms                                                 | 375 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 451 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 588 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 614 ms: 1.16x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                 |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 180 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 85.1 ms: 1.05x slower                                                 |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.00 ms: 1.06x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                 |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 339 us: 1.10x slower                                                  |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 99.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.73 ms: 1.36x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.4 ms: 1.65x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.0 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 16.1 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 129 ms: 2.47x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.77 ms: 1.95x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| bench_mp_pool              | 10.8 ms                                                | 6.73 ms: 1.61x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 728 ms: 1.49x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 406 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                  |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                                  |
| async_tree_none            | 464 ms                                                 | 375 ms: 1.24x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 451 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 588 ms: 1.23x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 33.0 us: 1.22x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 614 ms: 1.16x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.93 us: 1.14x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.00 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.92 us: 1.05x faster                                                 |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| chaos                      | 62.8 ms                                                | 60.6 ms: 1.04x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.99 ms: 1.04x faster                                                 |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                  |
| pidigits                   | 184 ms                                                 | 180 ms: 1.02x faster                                                  |
| raytrace                   | 299 ms                                                 | 292 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.2 ms: 1.02x faster                                                 |
| pyflate                    | 448 ms                                                 | 456 ms: 1.02x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                                 |
| float                      | 80.8 ms                                                | 85.1 ms: 1.05x slower                                                 |
| generators                 | 32.2 ms                                                | 34.1 ms: 1.06x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.54 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.70 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 801 ms: 1.08x slower                                                  |
| async_generators           | 384 ms                                                 | 415 ms: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.09x slower                                                  |
| logging_format             | 7.35 us                                                | 8.00 us: 1.09x slower                                                 |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| sympy_str                  | 292 ms                                                 | 319 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                |
| pickle_pure_python         | 308 us                                                 | 339 us: 1.10x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.94 sec: 1.12x slower                                                |
| nqueens                    | 80.1 ms                                                | 89.5 ms: 1.12x slower                                                 |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.1 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 534 ms: 1.14x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                                 |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 99.0 ms: 1.16x slower                                                 |
| richards_super             | 51.9 ms                                                | 60.6 ms: 1.17x slower                                                 |
| thrift                     | 791 us                                                 | 930 us: 1.18x slower                                                  |
| django_template            | 34.7 ms                                                | 41.0 ms: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.21 ms: 1.19x slower                                                 |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.20x slower                                                  |
| fannkuch                   | 372 ms                                                 | 467 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.73 ms: 1.36x slower                                                 |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.47x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.58x slower                                                 |
| python_startup             | 9.93 ms                                                | 16.4 ms: 1.65x slower                                                 |
| coverage                   | 71.4 ms                                                | 118 ms: 1.65x slower                                                  |
| telco                      | 6.53 ms                                                | 175 ms: 26.77x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (2): scimark_fft, pycparser
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260918-3.16.0a0-6dad8b8-NOGIL/bm-20260918-vultr-x86_64-python-6dad8b88cc39d8f9f41c-3.16.0a0-6dad8b8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 87.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x