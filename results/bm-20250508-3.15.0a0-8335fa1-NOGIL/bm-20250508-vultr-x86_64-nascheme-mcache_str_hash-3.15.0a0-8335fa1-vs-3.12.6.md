# Results vs. 3.12.6

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: 8335fa1
- commit date: 2025-05-08
- overall geometric mean: 1.008x faster
- HPT reliability: 90.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 286 ms: 1.09x slower                                               |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                             |
| html5lib       | 63.6 ms                                                | 66.3 ms: 1.04x slower                                              |
| Geometric mean | (ref)                                                  | 1.05x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                               |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                               |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.53x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                               |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                              |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                       |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.7 ms: 1.14x faster                                              |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| nbody          | 89.3 ms                                                | 119 ms: 1.33x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                              |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                               |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                              |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.2 ms: 1.11x faster                                              |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                               |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                             |
| unpickle_pure_python | 221 us                                                 | 232 us: 1.05x slower                                               |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.08x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                              |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 69.8 ms: 1.18x slower                                              |
| json_dumps           | 10.4 ms                                                | 13.4 ms: 1.29x slower                                              |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                              |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                              |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                              |
| django_template | 34.7 ms                                                | 40.9 ms: 1.18x slower                                              |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                              |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.98x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                               |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                               |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.81x faster                                              |
| mdp                        | 2.42 sec                                               | 1.34 sec: 1.81x faster                                             |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.53x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 502 ms: 1.42x faster                                               |
| deepcopy                   | 352 us                                                 | 292 us: 1.20x faster                                               |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                              |
| float                      | 80.8 ms                                                | 70.7 ms: 1.14x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 35.4 us: 1.14x faster                                              |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 87.2 ms: 1.11x faster                                              |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                              |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                              |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                               |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                               |
| generators                 | 32.2 ms                                                | 30.7 ms: 1.05x faster                                              |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.04 us: 1.01x faster                                              |
| comprehensions             | 19.8 us                                                | 19.6 us: 1.01x faster                                              |
| raytrace                   | 299 ms                                                 | 297 ms: 1.01x faster                                               |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                             |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                               |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                               |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                              |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                             |
| deltablue                  | 3.45 ms                                                | 3.54 ms: 1.03x slower                                              |
| json                       | 5.02 ms                                                | 5.19 ms: 1.03x slower                                              |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                               |
| html5lib                   | 63.6 ms                                                | 66.3 ms: 1.04x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 780 ms: 1.05x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 232 us: 1.05x slower                                               |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                               |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.07x slower                                             |
| pyflate                    | 448 ms                                                 | 481 ms: 1.07x slower                                               |
| scimark_fft                | 342 ms                                                 | 369 ms: 1.08x slower                                               |
| hexiom                     | 6.17 ms                                                | 6.68 ms: 1.08x slower                                              |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.08x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 22.3 ms: 1.08x slower                                              |
| 2to3                       | 264 ms                                                 | 286 ms: 1.09x slower                                               |
| sympy_str                  | 292 ms                                                 | 318 ms: 1.09x slower                                               |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                               |
| nqueens                    | 80.1 ms                                                | 88.1 ms: 1.10x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                              |
| richards                   | 45.9 ms                                                | 50.7 ms: 1.10x slower                                              |
| thrift                     | 791 us                                                 | 889 us: 1.12x slower                                               |
| scimark_monte_carlo        | 68.4 ms                                                | 76.9 ms: 1.12x slower                                              |
| richards_super             | 51.9 ms                                                | 58.3 ms: 1.12x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 86.5 ms: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                              |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                               |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                              |
| sympy_expand               | 468 ms                                                 | 538 ms: 1.15x slower                                               |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                              |
| logging_simple             | 6.63 us                                                | 7.76 us: 1.17x slower                                              |
| logging_format             | 7.35 us                                                | 8.62 us: 1.17x slower                                              |
| django_template            | 34.7 ms                                                | 40.9 ms: 1.18x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 69.8 ms: 1.18x slower                                              |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                               |
| fannkuch                   | 372 ms                                                 | 473 ms: 1.27x slower                                               |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.62 ms: 1.28x slower                                              |
| json_dumps                 | 10.4 ms                                                | 13.4 ms: 1.29x slower                                              |
| nbody                      | 89.3 ms                                                | 119 ms: 1.33x slower                                               |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                              |
| telco                      | 6.53 ms                                                | 8.79 ms: 1.35x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.36x slower                                              |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                              |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                               |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                              |
| logging_silent             | 109 ns                                                 | 536 ns: 4.92x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.53x slower                                               |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                       |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, chaos
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250508-3.15.0a0-8335fa1-NOGIL/bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-8335fa1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 90.88% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x