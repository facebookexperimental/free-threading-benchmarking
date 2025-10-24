# Results vs. 3.12.6

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.016x slower
- HPT reliability: 84.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                               |
| html5lib       | 63.6 ms                                                | 67.6 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.05x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 540 ms: 2.01x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.99x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.98x faster                                                 |
| async_tree_none            | 464 ms                                                 | 254 ms: 1.83x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.81x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 25.7 ms: 1.07x slower                                                |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                |
| pidigits       | 184 ms                                                 | 196 ms: 1.07x slower                                                 |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                 |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.04 sec: 1.04x faster                                               |
| unpickle_pure_python | 221 us                                                 | 235 us: 1.06x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                |
| pickle_pure_python   | 308 us                                                 | 339 us: 1.10x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                |
| json_loads           | 26.5 us                                                | 30.9 us: 1.17x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                |
| django_template | 34.7 ms                                                | 40.3 ms: 1.16x slower                                                |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 540 ms: 2.01x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.99x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.98x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                               |
| async_tree_none            | 464 ms                                                 | 254 ms: 1.83x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.81x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 31.0 us: 1.30x faster                                                |
| deepcopy                   | 352 us                                                 | 281 us: 1.25x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                |
| float                      | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                                |
| dulwich_log                | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                 |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                 |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 2.04 sec: 1.04x faster                                               |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                               |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.10 us: 1.01x slower                                                |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                 |
| chaos                      | 62.8 ms                                                | 63.9 ms: 1.02x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                               |
| pyflate                    | 448 ms                                                 | 460 ms: 1.03x slower                                                 |
| scimark_fft                | 342 ms                                                 | 353 ms: 1.03x slower                                                 |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.42 ms: 1.04x slower                                                |
| logging_simple             | 6.63 us                                                | 6.91 us: 1.04x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.61 ms: 1.05x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 785 ms: 1.06x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.6 ms: 1.06x slower                                                |
| sympy_str                  | 292 ms                                                 | 310 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 235 us: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 196 ms: 1.07x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.62 sec: 1.07x slower                                               |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                |
| logging_format             | 7.35 us                                                | 7.86 us: 1.07x slower                                                |
| coroutines                 | 23.9 ms                                                | 25.7 ms: 1.07x slower                                                |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                |
| pickle_pure_python         | 308 us                                                 | 339 us: 1.10x slower                                                 |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                 |
| nqueens                    | 80.1 ms                                                | 88.4 ms: 1.10x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                |
| richards                   | 45.9 ms                                                | 51.8 ms: 1.13x slower                                                |
| thrift                     | 791 us                                                 | 894 us: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 187 us: 1.15x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 79.2 ms: 1.16x slower                                                |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                |
| django_template            | 34.7 ms                                                | 40.3 ms: 1.16x slower                                                |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.17x slower                                                |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.9 ms: 1.17x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.19 ms: 1.18x slower                                                |
| fannkuch                   | 372 ms                                                 | 452 ms: 1.21x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 15.0 ms: 1.39x slower                                                |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.06 ms: 3.25x slower                                                |
| telco                      | 6.53 ms                                                | 178 ms: 27.21x slower                                                |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                         |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-04318d0-NOGIL/bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 84.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x