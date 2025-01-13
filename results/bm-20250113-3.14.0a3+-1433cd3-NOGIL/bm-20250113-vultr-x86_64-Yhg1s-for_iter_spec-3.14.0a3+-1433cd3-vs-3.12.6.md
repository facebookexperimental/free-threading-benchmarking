# Results vs. 3.12.6

- fork: Yhg1s
- ref: for_iter_spec
- machine: linux-x86_64
- commit hash: 1433cd3
- commit date: 2025-01-13
- overall geometric mean: 1.161x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 343 ms: 1.30x slower                                           |
| docutils       | 2.64 sec                                               | 3.00 sec: 1.14x slower                                         |
| html5lib       | 63.6 ms                                                | 88.7 ms: 1.39x slower                                          |
| Geometric mean | (ref)                                                  | 1.27x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 733 ms: 1.51x faster                                           |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.42x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 314 ms: 1.42x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                           |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 575 ms: 1.26x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                           |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                          |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                           |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                   |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                           |
| float          | 80.8 ms                                                | 107 ms: 1.33x slower                                           |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                           |
| Geometric mean | (ref)                                                  | 1.24x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                          |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                           |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                          |
| regex_compile  | 142 ms                                                 | 166 ms: 1.17x slower                                           |
| Geometric mean | (ref)                                                  | 1.06x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.8 ms: 1.08x faster                                          |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                           |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                          |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                         |
| xml_etree_generate   | 85.2 ms                                                | 98.2 ms: 1.15x slower                                          |
| xml_etree_process    | 59.0 ms                                                | 73.9 ms: 1.25x slower                                          |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.35x slower                                          |
| unpickle_pure_python | 221 us                                                 | 322 us: 1.46x slower                                           |
| pickle_pure_python   | 308 us                                                 | 492 us: 1.60x slower                                           |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.80 ms: 1.37x slower                                          |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                          |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.2 ms: 1.20x slower                                          |
| genshi_text     | 22.8 ms                                                | 29.4 ms: 1.29x slower                                          |
| django_template | 34.7 ms                                                | 50.1 ms: 1.45x slower                                          |
| mako            | 11.0 ms                                                | 17.2 ms: 1.56x slower                                          |
| Geometric mean  | (ref)                                                  | 1.37x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 733 ms: 1.51x faster                                           |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.42x faster                                           |
| async_tree_none_tg         | 446 ms                                                 | 314 ms: 1.42x faster                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                           |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 575 ms: 1.26x faster                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                          |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                          |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                           |
| xml_etree_iterparse        | 96.7 ms                                                | 89.8 ms: 1.08x faster                                          |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                           |
| sqlite_synth               | 2.20 us                                                | 2.10 us: 1.05x faster                                          |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                          |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                           |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                          |
| deepcopy_memo              | 40.3 us                                                | 40.9 us: 1.02x slower                                          |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                          |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.97 sec: 1.05x slower                                         |
| pylint                     | 319 ms                                                 | 342 ms: 1.07x slower                                           |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                           |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.08x slower                                          |
| deepcopy_reduce            | 3.08 us                                                | 3.38 us: 1.10x slower                                          |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                         |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                           |
| dulwich_log                | 78.9 ms                                                | 89.7 ms: 1.14x slower                                          |
| docutils                   | 2.64 sec                                               | 3.00 sec: 1.14x slower                                         |
| pycparser                  | 1.17 sec                                               | 1.33 sec: 1.14x slower                                         |
| xml_etree_generate         | 85.2 ms                                                | 98.2 ms: 1.15x slower                                          |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                          |
| generators                 | 32.2 ms                                                | 37.4 ms: 1.16x slower                                          |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                           |
| crypto_pyaes               | 76.6 ms                                                | 89.2 ms: 1.16x slower                                          |
| regex_compile              | 142 ms                                                 | 166 ms: 1.17x slower                                           |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                           |
| mdp                        | 2.42 sec                                               | 2.86 sec: 1.18x slower                                         |
| genshi_xml                 | 50.2 ms                                                | 60.2 ms: 1.20x slower                                          |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                          |
| sympy_str                  | 292 ms                                                 | 354 ms: 1.21x slower                                           |
| sympy_integrate            | 20.5 ms                                                | 25.1 ms: 1.22x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.41 ms: 1.23x slower                                          |
| sqlglot_normalize          | 107 ms                                                 | 132 ms: 1.24x slower                                           |
| sympy_expand               | 468 ms                                                 | 582 ms: 1.24x slower                                           |
| sqlglot_optimize           | 53.3 ms                                                | 66.5 ms: 1.25x slower                                          |
| xml_etree_process          | 59.0 ms                                                | 73.9 ms: 1.25x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 205 us: 1.26x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 936 ms: 1.26x slower                                           |
| thrift                     | 791 us                                                 | 1.01 ms: 1.27x slower                                          |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.28x slower                                           |
| sqlalchemy_declarative     | 143 ms                                                 | 183 ms: 1.28x slower                                           |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.9 ms: 1.28x slower                                          |
| pprint_pformat             | 1.52 sec                                               | 1.95 sec: 1.28x slower                                         |
| genshi_text                | 22.8 ms                                                | 29.4 ms: 1.29x slower                                          |
| 2to3                       | 264 ms                                                 | 343 ms: 1.30x slower                                           |
| fannkuch                   | 372 ms                                                 | 486 ms: 1.30x slower                                           |
| telco                      | 6.53 ms                                                | 8.61 ms: 1.32x slower                                          |
| float                      | 80.8 ms                                                | 107 ms: 1.33x slower                                           |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.35x slower                                          |
| scimark_lu                 | 114 ms                                                 | 154 ms: 1.35x slower                                           |
| logging_simple             | 6.63 us                                                | 9.04 us: 1.36x slower                                          |
| python_startup_no_site     | 7.16 ms                                                | 9.80 ms: 1.37x slower                                          |
| coverage                   | 71.4 ms                                                | 98.5 ms: 1.38x slower                                          |
| logging_format             | 7.35 us                                                | 10.1 us: 1.38x slower                                          |
| html5lib                   | 63.6 ms                                                | 88.7 ms: 1.39x slower                                          |
| comprehensions             | 19.8 us                                                | 27.9 us: 1.41x slower                                          |
| pyflate                    | 448 ms                                                 | 637 ms: 1.42x slower                                           |
| richards                   | 45.9 ms                                                | 65.5 ms: 1.43x slower                                          |
| django_template            | 34.7 ms                                                | 50.1 ms: 1.45x slower                                          |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                           |
| unpickle_pure_python       | 221 us                                                 | 322 us: 1.46x slower                                           |
| richards_super             | 51.9 ms                                                | 76.5 ms: 1.47x slower                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 102 ms: 1.50x slower                                           |
| hexiom                     | 6.17 ms                                                | 9.28 ms: 1.50x slower                                          |
| chaos                      | 62.8 ms                                                | 94.7 ms: 1.51x slower                                          |
| scimark_sor                | 130 ms                                                 | 202 ms: 1.55x slower                                           |
| mako                       | 11.0 ms                                                | 17.2 ms: 1.56x slower                                          |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                          |
| pickle_pure_python         | 308 us                                                 | 492 us: 1.60x slower                                           |
| sqlglot_transpile          | 1.67 ms                                                | 2.68 ms: 1.60x slower                                          |
| raytrace                   | 299 ms                                                 | 490 ms: 1.64x slower                                           |
| go                         | 139 ms                                                 | 231 ms: 1.66x slower                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                          |
| logging_silent             | 109 ns                                                 | 182 ns: 1.67x slower                                           |
| sqlglot_parse              | 1.36 ms                                                | 2.32 ms: 1.71x slower                                          |
| deltablue                  | 3.45 ms                                                | 7.35 ms: 2.13x slower                                          |
| bench_thread_pool          | 941 us                                                 | 3.36 ms: 3.56x slower                                          |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.28x slower                                           |
| Geometric mean             | (ref)                                                  | 1.24x slower                                                   |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250113-3.14.0a3+-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3+-1433cd3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.161x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.33x