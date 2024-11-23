# Results vs. 3.12.6

- fork: colesbury
- ref: gh_127022_py_eval_fr
- machine: linux-x86_64
- commit hash: 9e69bca
- commit date: 2024-11-22
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 380 ms: 1.44x slower                                                      |
| docutils       | 2.64 sec                                               | 3.23 sec: 1.22x slower                                                    |
| html5lib       | 63.6 ms                                                | 103 ms: 1.61x slower                                                      |
| Geometric mean | (ref)                                                  | 1.42x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 891 ms: 1.21x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 369 ms: 1.21x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 466 ms: 1.20x faster                                                      |
| async_tree_none            | 464 ms                                                 | 401 ms: 1.16x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 628 ms: 1.15x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 653 ms: 1.09x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                      |
| coroutines                 | 23.9 ms                                                | 28.0 ms: 1.17x slower                                                     |
| async_generators           | 384 ms                                                 | 476 ms: 1.24x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| float          | 80.8 ms                                                | 144 ms: 1.78x slower                                                      |
| nbody          | 89.3 ms                                                | 160 ms: 1.79x slower                                                      |
| Geometric mean | (ref)                                                  | 1.47x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                     |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                     |
| regex_compile  | 142 ms                                                 | 195 ms: 1.37x slower                                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 95.5 ms: 1.01x faster                                                     |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.95 sec: 1.40x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 378 us: 1.71x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 562 us: 1.83x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                     |
| python_startup         | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.60x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 67.0 ms: 1.34x slower                                                     |
| genshi_text     | 22.8 ms                                                | 34.0 ms: 1.49x slower                                                     |
| django_template | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                     |
| mako            | 11.0 ms                                                | 19.7 ms: 1.79x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 865 ms: 1.28x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 891 ms: 1.21x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 369 ms: 1.21x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 466 ms: 1.20x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                     |
| async_tree_none            | 464 ms                                                 | 401 ms: 1.16x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 628 ms: 1.15x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 653 ms: 1.09x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                      |
| pathlib                    | 21.5 ms                                                | 20.6 ms: 1.05x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 95.5 ms: 1.01x faster                                                     |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                      |
| deepcopy                   | 352 us                                                 | 358 us: 1.02x slower                                                      |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                     |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                     |
| sqlite_synth               | 2.20 us                                                | 2.32 us: 1.05x slower                                                     |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                      |
| deepcopy_memo              | 40.3 us                                                | 45.7 us: 1.13x slower                                                     |
| coroutines                 | 23.9 ms                                                | 28.0 ms: 1.17x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 5.62 sec: 1.19x slower                                                    |
| scimark_fft                | 342 ms                                                 | 406 ms: 1.19x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 24.5 ms: 1.19x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                      |
| spectral_norm              | 110 ms                                                 | 132 ms: 1.20x slower                                                      |
| mdp                        | 2.42 sec                                               | 2.94 sec: 1.21x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.75 us: 1.22x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.23 sec: 1.22x slower                                                    |
| async_generators           | 384 ms                                                 | 476 ms: 1.24x slower                                                      |
| pylint                     | 319 ms                                                 | 398 ms: 1.25x slower                                                      |
| dulwich_log                | 78.9 ms                                                | 98.8 ms: 1.25x slower                                                     |
| generators                 | 32.2 ms                                                | 40.6 ms: 1.26x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.56 ms: 1.27x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 212 us: 1.30x slower                                                      |
| meteor_contest             | 104 ms                                                 | 136 ms: 1.32x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 67.0 ms: 1.34x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 103 ms: 1.35x slower                                                      |
| telco                      | 6.53 ms                                                | 8.89 ms: 1.36x slower                                                     |
| regex_compile              | 142 ms                                                 | 195 ms: 1.37x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.61 sec: 1.38x slower                                                    |
| nqueens                    | 80.1 ms                                                | 110 ms: 1.38x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.95 sec: 1.40x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 150 ms: 1.41x slower                                                      |
| sqlglot_optimize           | 53.3 ms                                                | 75.6 ms: 1.42x slower                                                     |
| coverage                   | 71.4 ms                                                | 103 ms: 1.44x slower                                                      |
| 2to3                       | 264 ms                                                 | 380 ms: 1.44x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 1.08 sec: 1.45x slower                                                    |
| fannkuch                   | 372 ms                                                 | 543 ms: 1.46x slower                                                      |
| comprehensions             | 19.8 us                                                | 29.0 us: 1.46x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 2.23 sec: 1.47x slower                                                    |
| genshi_text                | 22.8 ms                                                | 34.0 ms: 1.49x slower                                                     |
| thrift                     | 791 us                                                 | 1.21 ms: 1.53x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 31.4 ms: 1.53x slower                                                     |
| django_template            | 34.7 ms                                                | 55.7 ms: 1.61x slower                                                     |
| html5lib                   | 63.6 ms                                                | 103 ms: 1.61x slower                                                      |
| logging_format             | 7.35 us                                                | 12.1 us: 1.65x slower                                                     |
| logging_simple             | 6.63 us                                                | 11.1 us: 1.67x slower                                                     |
| pyflate                    | 448 ms                                                 | 750 ms: 1.67x slower                                                      |
| sympy_str                  | 292 ms                                                 | 496 ms: 1.70x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 378 us: 1.71x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 196 ms: 1.72x slower                                                      |
| python_startup             | 9.93 ms                                                | 17.6 ms: 1.77x slower                                                     |
| float                      | 80.8 ms                                                | 144 ms: 1.78x slower                                                      |
| logging_silent             | 109 ns                                                 | 194 ns: 1.78x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 122 ms: 1.78x slower                                                      |
| mako                       | 11.0 ms                                                | 19.7 ms: 1.79x slower                                                     |
| nbody                      | 89.3 ms                                                | 160 ms: 1.79x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 562 us: 1.83x slower                                                      |
| chaos                      | 62.8 ms                                                | 115 ms: 1.83x slower                                                      |
| richards                   | 45.9 ms                                                | 84.5 ms: 1.84x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 3.08 ms: 1.84x slower                                                     |
| scimark_sor                | 130 ms                                                 | 241 ms: 1.86x slower                                                      |
| hexiom                     | 6.17 ms                                                | 11.5 ms: 1.86x slower                                                     |
| richards_super             | 51.9 ms                                                | 99.9 ms: 1.93x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.67 ms: 1.97x slower                                                     |
| raytrace                   | 299 ms                                                 | 608 ms: 2.03x slower                                                      |
| go                         | 139 ms                                                 | 287 ms: 2.06x slower                                                      |
| sympy_expand               | 468 ms                                                 | 986 ms: 2.11x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 358 ms: 2.15x slower                                                      |
| deltablue                  | 3.45 ms                                                | 8.80 ms: 2.55x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 111 ms: 10.25x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.41x slower                                                              |

Benchmark hidden because not significant (1): json
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-9e69bca-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.34x