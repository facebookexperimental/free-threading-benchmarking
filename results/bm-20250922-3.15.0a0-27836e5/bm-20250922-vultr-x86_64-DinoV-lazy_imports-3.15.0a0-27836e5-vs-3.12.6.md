# Results vs. 3.12.6

- fork: DinoV
- ref: lazy_imports
- machine: linux-x86_64
- commit hash: 27836e5
- commit date: 2025-09-22
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                       |
| html5lib       | 63.6 ms                                                | 61.4 ms: 1.04x faster                                        |
| Geometric mean | (ref)                                                  | 1.04x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                         |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                         |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                         |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                         |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                        |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                 |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                        |
| nbody          | 89.3 ms                                                | 90.7 ms: 1.02x slower                                        |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                         |
| Geometric mean | (ref)                                                  | 1.01x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.19x faster                                        |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                         |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                        |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                  | 1.07x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                       |
| json_dumps           | 10.4 ms                                                | 9.58 ms: 1.08x faster                                        |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                         |
| xml_etree_iterparse  | 96.7 ms                                                | 93.2 ms: 1.04x faster                                        |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                         |
| xml_etree_generate   | 85.2 ms                                                | 83.5 ms: 1.02x faster                                        |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                        |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                        |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.27 ms: 1.02x slower                                        |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                        |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                        |
| genshi_xml      | 50.2 ms                                                | 48.4 ms: 1.04x faster                                        |
| django_template | 34.7 ms                                                | 34.0 ms: 1.02x faster                                        |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                       |
| async_tree_io              | 1.08 sec                                               | 605 ms: 1.79x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                         |
| async_tree_io_tg           | 1.11 sec                                               | 627 ms: 1.77x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                         |
| async_tree_none            | 464 ms                                                 | 265 ms: 1.75x faster                                         |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                        |
| deepcopy                   | 352 us                                                 | 242 us: 1.45x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                         |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                         |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.26x faster                                        |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                        |
| dulwich_log                | 78.9 ms                                                | 66.2 ms: 1.19x faster                                        |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.19x faster                                        |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                         |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                         |
| spectral_norm              | 110 ms                                                 | 94.7 ms: 1.16x faster                                        |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.15x faster                                        |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                         |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                         |
| logging_simple             | 6.63 us                                                | 5.84 us: 1.14x faster                                        |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                       |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                         |
| crypto_pyaes               | 76.6 ms                                                | 68.4 ms: 1.12x faster                                        |
| logging_format             | 7.35 us                                                | 6.56 us: 1.12x faster                                        |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                        |
| chaos                      | 62.8 ms                                                | 56.7 ms: 1.11x faster                                        |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                        |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                        |
| scimark_monte_carlo        | 68.4 ms                                                | 61.9 ms: 1.10x faster                                        |
| pyflate                    | 448 ms                                                 | 410 ms: 1.09x faster                                         |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                       |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                        |
| richards_super             | 51.9 ms                                                | 47.5 ms: 1.09x faster                                        |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                        |
| typing_runtime_protocols   | 163 us                                                 | 151 us: 1.09x faster                                         |
| json_dumps                 | 10.4 ms                                                | 9.58 ms: 1.08x faster                                        |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                         |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                         |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                         |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                       |
| pprint_safe_repr           | 743 ms                                                 | 694 ms: 1.07x faster                                         |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                       |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                         |
| meteor_contest             | 104 ms                                                 | 98.9 ms: 1.05x faster                                        |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                         |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 93.2 ms: 1.04x faster                                        |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                         |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                        |
| html5lib                   | 63.6 ms                                                | 61.4 ms: 1.04x faster                                        |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                         |
| nqueens                    | 80.1 ms                                                | 77.8 ms: 1.03x faster                                        |
| deltablue                  | 3.45 ms                                                | 3.36 ms: 1.03x faster                                        |
| django_template            | 34.7 ms                                                | 34.0 ms: 1.02x faster                                        |
| xml_etree_generate         | 85.2 ms                                                | 83.5 ms: 1.02x faster                                        |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                        |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                         |
| nbody                      | 89.3 ms                                                | 90.7 ms: 1.02x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 7.27 ms: 1.02x slower                                        |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                         |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                        |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                        |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                         |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                        |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                        |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                         |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                        |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.89 ms: 1.11x slower                                        |
| coverage                   | 71.4 ms                                                | 81.8 ms: 1.15x slower                                        |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                        |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                        |
| gc_traversal               | 3.46 ms                                                | 4.75 ms: 1.37x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.95 ms: 1.79x slower                                        |
| telco                      | 6.53 ms                                                | 158 ms: 24.19x slower                                        |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                 |

Benchmark hidden because not significant (4): sympy_expand, pickle_pure_python, json, asyncio_websockets
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mako, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (9) of results/bm-20250922-3.15.0a0-27836e5/bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5.json: connected_components, k_core, many_optionals, shortest_path, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x