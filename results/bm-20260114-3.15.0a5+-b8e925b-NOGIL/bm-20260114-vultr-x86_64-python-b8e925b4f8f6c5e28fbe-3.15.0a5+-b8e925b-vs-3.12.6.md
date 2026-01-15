# Results vs. 3.12.6

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: linux-x86_64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.029x slower
- HPT reliability: 74.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| docutils       | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| html5lib       | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 517 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                   |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.8 ms: 1.11x faster                                                  |
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                   |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.08x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 339 us: 1.10x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.9 ms: 1.13x slower                                                  |
| django_template | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.2 ms: 1.19x slower                                                  |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.81x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.95 ms: 1.78x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.05 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 517 ms: 1.40x faster                                                   |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.7 us: 1.31x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.21x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 70.4 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.8 ms: 1.11x faster                                                  |
| comprehensions             | 19.8 us                                                | 18.0 us: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                 |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| pylint                     | 319 ms                                                 | 302 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.92 us: 1.05x faster                                                  |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 511 ms: 1.01x faster                                                   |
| generators                 | 32.2 ms                                                | 31.9 ms: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 340 ms: 1.01x faster                                                   |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                   |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.72 sec: 1.03x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                  |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 772 ms: 1.04x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.93 us: 1.05x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.46 ms: 1.05x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 174 ms: 1.05x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.62 ms: 1.05x slower                                                  |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.05x slower                                                   |
| logging_format             | 7.35 us                                                | 7.77 us: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.7 ms: 1.06x slower                                                  |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.0 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.08x slower                                                   |
| json                       | 5.02 ms                                                | 5.52 ms: 1.10x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 339 us: 1.10x slower                                                   |
| sympy_expand               | 468 ms                                                 | 518 ms: 1.11x slower                                                   |
| nqueens                    | 80.1 ms                                                | 88.7 ms: 1.11x slower                                                  |
| thrift                     | 791 us                                                 | 888 us: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.3 ms: 1.13x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 56.9 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.6 ms: 1.13x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                   |
| richards                   | 45.9 ms                                                | 52.6 ms: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.1 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                  |
| meteor_contest             | 104 ms                                                 | 122 ms: 1.17x slower                                                   |
| django_template            | 34.7 ms                                                | 41.1 ms: 1.19x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.2 ms: 1.19x slower                                                  |
| json_loads                 | 26.5 us                                                | 32.4 us: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.38 ms: 1.22x slower                                                  |
| fannkuch                   | 372 ms                                                 | 459 ms: 1.23x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.72 ms: 1.36x slower                                                  |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                                  |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| telco                      | 6.53 ms                                                | 176 ms: 26.96x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): spectral_norm
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260114-3.15.0a5+-b8e925b-NOGIL/bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 74.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x