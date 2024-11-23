# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_115999_store_subs
- machine: linux-x86_64
- commit hash: 2b63929
- commit date: 2024-11-22
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 379 ms: 1.46x slower                                                      |
| docutils       | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                    |
| html5lib       | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                                     |
| Geometric mean | (ref)                                                        | 1.39x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 874 ms: 1.05x faster                                                      |
| async_tree_io             | 876 ms                                                       | 898 ms: 1.03x slower                                                      |
| async_tree_memoization    | 461 ms                                                       | 496 ms: 1.08x slower                                                      |
| async_tree_none_tg        | 336 ms                                                       | 373 ms: 1.11x slower                                                      |
| async_tree_memoization_tg | 414 ms                                                       | 467 ms: 1.13x slower                                                      |
| async_tree_none           | 354 ms                                                       | 407 ms: 1.15x slower                                                      |
| coroutines                | 23.6 ms                                                      | 27.6 ms: 1.17x slower                                                     |
| async_generators          | 377 ms                                                       | 471 ms: 1.25x slower                                                      |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                              |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                      |
| nbody          | 85.1 ms                                                      | 144 ms: 1.69x slower                                                      |
| float          | 77.5 ms                                                      | 142 ms: 1.84x slower                                                      |
| Geometric mean | (ref)                                                        | 1.38x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                     |
| regex_dna      | 180 ms                                                       | 181 ms: 1.00x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                     |
| regex_compile  | 132 ms                                                       | 194 ms: 1.47x slower                                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                      |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                     |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 103 ms: 1.20x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.90 sec: 1.44x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 370 us: 1.76x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 561 us: 1.90x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.31x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                     |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 67.6 ms: 1.39x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                                     |
| django_template | 34.1 ms                                                      | 55.6 ms: 1.63x slower                                                     |
| mako            | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929 |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                      |
| regex_effbot              | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 874 ms: 1.05x faster                                                      |
| xml_etree_parse           | 136 ms                                                       | 132 ms: 1.03x faster                                                      |
| deepcopy                  | 355 us                                                       | 352 us: 1.01x faster                                                      |
| regex_dna                 | 180 ms                                                       | 181 ms: 1.00x slower                                                      |
| xml_etree_iterparse       | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                     |
| json                      | 4.93 ms                                                      | 5.01 ms: 1.02x slower                                                     |
| async_tree_io             | 876 ms                                                       | 898 ms: 1.03x slower                                                      |
| json_loads                | 27.0 us                                                      | 27.8 us: 1.03x slower                                                     |
| sqlite_synth              | 2.21 us                                                      | 2.29 us: 1.04x slower                                                     |
| async_tree_memoization    | 461 ms                                                       | 496 ms: 1.08x slower                                                      |
| pathlib                   | 19.2 ms                                                      | 20.7 ms: 1.08x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 373 ms: 1.11x slower                                                      |
| gc_traversal              | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 467 ms: 1.13x slower                                                      |
| deepcopy_memo             | 39.1 us                                                      | 44.1 us: 1.13x slower                                                     |
| scimark_fft               | 349 ms                                                       | 394 ms: 1.13x slower                                                      |
| telco                     | 7.82 ms                                                      | 8.99 ms: 1.15x slower                                                     |
| async_tree_none           | 354 ms                                                       | 407 ms: 1.15x slower                                                      |
| spectral_norm             | 111 ms                                                       | 129 ms: 1.16x slower                                                      |
| coroutines                | 23.6 ms                                                      | 27.6 ms: 1.17x slower                                                     |
| deepcopy_reduce           | 3.11 us                                                      | 3.68 us: 1.18x slower                                                     |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.61 ms: 1.19x slower                                                     |
| xml_etree_generate        | 85.4 ms                                                      | 103 ms: 1.20x slower                                                      |
| docutils                  | 2.62 sec                                                     | 3.21 sec: 1.23x slower                                                    |
| coverage                  | 83.0 ms                                                      | 102 ms: 1.23x slower                                                      |
| pylint                    | 317 ms                                                       | 393 ms: 1.24x slower                                                      |
| async_generators          | 377 ms                                                       | 471 ms: 1.25x slower                                                      |
| bpe_tokeniser             | 4.45 sec                                                     | 5.59 sec: 1.26x slower                                                    |
| mdp                       | 2.36 sec                                                     | 3.03 sec: 1.29x slower                                                    |
| meteor_contest            | 102 ms                                                       | 135 ms: 1.32x slower                                                      |
| dulwich_log               | 74.8 ms                                                      | 99.3 ms: 1.33x slower                                                     |
| nqueens                   | 78.6 ms                                                      | 105 ms: 1.34x slower                                                      |
| generators                | 28.8 ms                                                      | 38.6 ms: 1.34x slower                                                     |
| json_dumps                | 10.5 ms                                                      | 14.3 ms: 1.35x slower                                                     |
| typing_runtime_protocols  | 155 us                                                       | 211 us: 1.36x slower                                                      |
| create_gc_cycles          | 1.34 ms                                                      | 1.85 ms: 1.39x slower                                                     |
| genshi_xml                | 48.8 ms                                                      | 67.6 ms: 1.39x slower                                                     |
| xml_etree_process         | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                     |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                     |
| sqlglot_normalize         | 106 ms                                                       | 149 ms: 1.41x slower                                                      |
| sqlglot_optimize          | 52.7 ms                                                      | 74.9 ms: 1.42x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.60 sec: 1.43x slower                                                    |
| pprint_safe_repr          | 738 ms                                                       | 1.06 sec: 1.44x slower                                                    |
| fannkuch                  | 370 ms                                                       | 533 ms: 1.44x slower                                                      |
| tomli_loads               | 2.01 sec                                                     | 2.90 sec: 1.44x slower                                                    |
| 2to3                      | 260 ms                                                       | 379 ms: 1.46x slower                                                      |
| regex_compile             | 132 ms                                                       | 194 ms: 1.47x slower                                                      |
| pprint_pformat            | 1.50 sec                                                     | 2.20 sec: 1.47x slower                                                    |
| html5lib                  | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                                     |
| crypto_pyaes              | 67.9 ms                                                      | 103 ms: 1.52x slower                                                      |
| sympy_integrate           | 19.8 ms                                                      | 30.8 ms: 1.55x slower                                                     |
| thrift                    | 778 us                                                       | 1.22 ms: 1.57x slower                                                     |
| genshi_text               | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                                     |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.60x slower                                                     |
| pyflate                   | 449 ms                                                       | 728 ms: 1.62x slower                                                      |
| django_template           | 34.1 ms                                                      | 55.6 ms: 1.63x slower                                                     |
| nbody                     | 85.1 ms                                                      | 144 ms: 1.69x slower                                                      |
| mako                      | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                     |
| comprehensions            | 16.5 us                                                      | 28.7 us: 1.75x slower                                                     |
| unpickle_pure_python      | 210 us                                                       | 370 us: 1.76x slower                                                      |
| logging_simple            | 6.16 us                                                      | 11.0 us: 1.78x slower                                                     |
| scimark_lu                | 113 ms                                                       | 203 ms: 1.80x slower                                                      |
| sympy_str                 | 275 ms                                                       | 495 ms: 1.80x slower                                                      |
| scimark_sor               | 134 ms                                                       | 243 ms: 1.80x slower                                                      |
| logging_format            | 6.84 us                                                      | 12.4 us: 1.81x slower                                                     |
| richards                  | 45.2 ms                                                      | 82.1 ms: 1.82x slower                                                     |
| scimark_monte_carlo       | 65.4 ms                                                      | 120 ms: 1.83x slower                                                      |
| float                     | 77.5 ms                                                      | 142 ms: 1.84x slower                                                      |
| hexiom                    | 5.99 ms                                                      | 11.2 ms: 1.86x slower                                                     |
| richards_super            | 51.6 ms                                                      | 97.9 ms: 1.90x slower                                                     |
| pickle_pure_python        | 294 us                                                       | 561 us: 1.90x slower                                                      |
| logging_silent            | 103 ns                                                       | 196 ns: 1.91x slower                                                      |
| sqlglot_transpile         | 1.56 ms                                                      | 3.06 ms: 1.96x slower                                                     |
| go                        | 141 ms                                                       | 277 ms: 1.97x slower                                                      |
| chaos                     | 57.3 ms                                                      | 114 ms: 1.98x slower                                                      |
| sqlglot_parse             | 1.25 ms                                                      | 2.64 ms: 2.11x slower                                                     |
| sympy_expand              | 457 ms                                                       | 992 ms: 2.17x slower                                                      |
| sympy_sum                 | 156 ms                                                       | 357 ms: 2.30x slower                                                      |
| raytrace                  | 253 ms                                                       | 599 ms: 2.37x slower                                                      |
| deltablue                 | 3.12 ms                                                      | 8.53 ms: 2.73x slower                                                     |
| bench_thread_pool         | 919 us                                                       | 3.42 ms: 3.72x slower                                                     |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 10.00x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.44x slower                                                              |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2+-2b63929.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.32x