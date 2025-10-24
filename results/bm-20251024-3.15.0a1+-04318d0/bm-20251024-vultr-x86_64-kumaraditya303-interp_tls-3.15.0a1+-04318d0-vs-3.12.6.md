# Results vs. 3.12.6

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.083x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                 |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                               |
| html5lib       | 63.6 ms                                                | 62.5 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 558 ms: 1.94x faster                                                 |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.88x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                 |
| async_generators           | 384 ms                                                 | 346 ms: 1.11x faster                                                 |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                |
| nbody          | 89.3 ms                                                | 87.7 ms: 1.02x faster                                                |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                 |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                 |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                  | 1.07x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.2 ms: 1.15x faster                                                |
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.11x faster                                               |
| json_dumps           | 10.4 ms                                                | 9.49 ms: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.5 ms: 1.03x faster                                                |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.20 ms: 1.01x slower                                                |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                |
| genshi_xml      | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                |
| django_template | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.11x faster                                               |
| async_tree_io              | 1.08 sec                                               | 558 ms: 1.94x faster                                                 |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.88x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 594 ms: 1.87x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 247 ms: 1.81x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 25.9 us: 1.56x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 482 ms: 1.48x faster                                                 |
| deepcopy                   | 352 us                                                 | 241 us: 1.46x faster                                                 |
| go                         | 139 ms                                                 | 103 ms: 1.36x faster                                                 |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                |
| scimark_sor                | 130 ms                                                 | 105 ms: 1.23x faster                                                 |
| raytrace                   | 299 ms                                                 | 247 ms: 1.21x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.58 us: 1.19x faster                                                |
| spectral_norm              | 110 ms                                                 | 92.6 ms: 1.19x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                |
| float                      | 80.8 ms                                                | 69.4 ms: 1.16x faster                                                |
| dulwich_log                | 78.9 ms                                                | 68.2 ms: 1.16x faster                                                |
| logging_simple             | 6.63 us                                                | 5.75 us: 1.15x faster                                                |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 84.2 ms: 1.15x faster                                                |
| logging_format             | 7.35 us                                                | 6.46 us: 1.14x faster                                                |
| logging_silent             | 109 ns                                                 | 95.9 ns: 1.14x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                               |
| chaos                      | 62.8 ms                                                | 55.3 ms: 1.14x faster                                                |
| richards                   | 45.9 ms                                                | 40.7 ms: 1.13x faster                                                |
| richards_super             | 51.9 ms                                                | 46.4 ms: 1.12x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 68.5 ms: 1.12x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 61.3 ms: 1.12x faster                                                |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.54 ms: 1.11x faster                                                |
| async_generators           | 384 ms                                                 | 346 ms: 1.11x faster                                                 |
| scimark_fft                | 342 ms                                                 | 308 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.11x faster                                               |
| pyflate                    | 448 ms                                                 | 407 ms: 1.10x faster                                                 |
| pylint                     | 319 ms                                                 | 289 ms: 1.10x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.10x faster                                               |
| json_dumps                 | 10.4 ms                                                | 9.49 ms: 1.09x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                               |
| pprint_safe_repr           | 743 ms                                                 | 683 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                |
| deltablue                  | 3.45 ms                                                | 3.20 ms: 1.08x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                 |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                 |
| thrift                     | 791 us                                                 | 754 us: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.3 ms: 1.04x faster                                                |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.5 ms: 1.03x faster                                                |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                               |
| nqueens                    | 80.1 ms                                                | 78.6 ms: 1.02x faster                                                |
| nbody                      | 89.3 ms                                                | 87.7 ms: 1.02x faster                                                |
| html5lib                   | 63.6 ms                                                | 62.5 ms: 1.02x faster                                                |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                |
| django_template            | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.4 ms: 1.01x faster                                                |
| python_startup_no_site     | 7.16 ms                                                | 7.20 ms: 1.01x slower                                                |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                |
| sympy_expand               | 468 ms                                                 | 477 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.51 ms: 1.03x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 995 us: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                |
| coverage                   | 71.4 ms                                                | 82.5 ms: 1.16x slower                                                |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                |
| gc_traversal               | 3.46 ms                                                | 4.79 ms: 1.39x slower                                                |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                |
| telco                      | 6.53 ms                                                | 155 ms: 23.80x slower                                                |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                         |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-04318d0/bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.16x