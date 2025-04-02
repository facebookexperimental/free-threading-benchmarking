# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 314 ms: 1.19x slower                                                     |
| docutils       | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                   |
| html5lib       | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.15x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                     |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                     |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 81.3 ms: 1.01x slower                                                    |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                     |
| nbody          | 89.3 ms                                                | 148 ms: 1.66x slower                                                     |
| Geometric mean | (ref)                                                  | 1.21x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                     |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                    |
| regex_compile  | 142 ms                                                 | 170 ms: 1.20x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                    |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.56 sec: 1.22x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 279 us: 1.26x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 74.6 ms: 1.27x slower                                                    |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 393 us: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 45.1 ms: 1.30x slower                                                    |
| genshi_xml      | 50.2 ms                                                | 66.4 ms: 1.32x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                    |
| mako            | 11.0 ms                                                | 16.5 ms: 1.50x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.37x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.80 ms: 1.92x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.47 sec: 1.65x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 521 ms: 1.37x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                    |
| deepcopy                   | 352 us                                                 | 338 us: 1.04x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 77.3 ms: 1.02x faster                                                    |
| float                      | 80.8 ms                                                | 81.3 ms: 1.01x slower                                                    |
| async_generators           | 384 ms                                                 | 388 ms: 1.01x slower                                                     |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                    |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                    |
| deepcopy_memo              | 40.3 us                                                | 42.7 us: 1.06x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.03 sec: 1.06x slower                                                   |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.27 sec: 1.08x slower                                                   |
| spectral_norm              | 110 ms                                                 | 120 ms: 1.09x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.37 us: 1.10x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                   |
| comprehensions             | 19.8 us                                                | 22.4 us: 1.13x slower                                                    |
| go                         | 139 ms                                                 | 157 ms: 1.13x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 162 ms: 1.14x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.9 ms: 1.14x slower                                                    |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                    |
| logging_silent             | 109 ns                                                 | 126 ns: 1.16x slower                                                     |
| html5lib                   | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.18x slower                                                     |
| raytrace                   | 299 ms                                                 | 353 ms: 1.18x slower                                                     |
| 2to3                       | 264 ms                                                 | 314 ms: 1.19x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 24.5 ms: 1.19x slower                                                    |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                    |
| chaos                      | 62.8 ms                                                | 75.2 ms: 1.20x slower                                                    |
| regex_compile              | 142 ms                                                 | 170 ms: 1.20x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                     |
| scimark_fft                | 342 ms                                                 | 411 ms: 1.20x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 896 ms: 1.21x slower                                                     |
| pyflate                    | 448 ms                                                 | 541 ms: 1.21x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.56 sec: 1.22x slower                                                   |
| sympy_str                  | 292 ms                                                 | 355 ms: 1.22x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.86 sec: 1.22x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 94.3 ms: 1.23x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.25x slower                                                    |
| logging_simple             | 6.63 us                                                | 8.30 us: 1.25x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 279 us: 1.26x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 74.6 ms: 1.27x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                    |
| sympy_expand               | 468 ms                                                 | 595 ms: 1.27x slower                                                     |
| scimark_sor                | 130 ms                                                 | 165 ms: 1.27x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.27x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 393 us: 1.28x slower                                                     |
| logging_format             | 7.35 us                                                | 9.41 us: 1.28x slower                                                    |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.28x slower                                                     |
| django_template            | 34.7 ms                                                | 45.1 ms: 1.30x slower                                                    |
| deltablue                  | 3.45 ms                                                | 4.55 ms: 1.32x slower                                                    |
| hexiom                     | 6.17 ms                                                | 8.14 ms: 1.32x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 66.4 ms: 1.32x slower                                                    |
| richards                   | 45.9 ms                                                | 61.0 ms: 1.33x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 90.9 ms: 1.33x slower                                                    |
| richards_super             | 51.9 ms                                                | 68.9 ms: 1.33x slower                                                    |
| meteor_contest             | 104 ms                                                 | 138 ms: 1.33x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 153 ms: 1.34x slower                                                     |
| genshi_text                | 22.8 ms                                                | 31.0 ms: 1.36x slower                                                    |
| telco                      | 6.53 ms                                                | 8.97 ms: 1.37x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.10 ms: 1.39x slower                                                    |
| fannkuch                   | 372 ms                                                 | 536 ms: 1.44x slower                                                     |
| mako                       | 11.0 ms                                                | 16.5 ms: 1.50x slower                                                    |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| nbody                      | 89.3 ms                                                | 148 ms: 1.66x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.20 ms: 3.40x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 97.9 ms: 9.06x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.14x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.37x