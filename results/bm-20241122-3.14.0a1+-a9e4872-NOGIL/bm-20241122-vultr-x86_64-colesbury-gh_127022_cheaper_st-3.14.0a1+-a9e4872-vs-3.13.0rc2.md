# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: a9e4872
- commit date: 2024-11-22
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 411 ms: 1.58x slower                                                      |
| docutils       | 2.62 sec                                                     | 3.32 sec: 1.27x slower                                                    |
| html5lib       | 67.0 ms                                                      | 102 ms: 1.53x slower                                                      |
| Geometric mean | (ref)                                                        | 1.45x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.00x faster                                                      |
| async_tree_io             | 876 ms                                                       | 936 ms: 1.07x slower                                                      |
| async_tree_memoization    | 461 ms                                                       | 507 ms: 1.10x slower                                                      |
| async_tree_none_tg        | 336 ms                                                       | 373 ms: 1.11x slower                                                      |
| async_tree_memoization_tg | 414 ms                                                       | 474 ms: 1.15x slower                                                      |
| async_tree_none           | 354 ms                                                       | 412 ms: 1.16x slower                                                      |
| async_generators          | 377 ms                                                       | 473 ms: 1.25x slower                                                      |
| coroutines                | 23.6 ms                                                      | 30.1 ms: 1.28x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.10x slower                                                              |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                      |
| float          | 77.5 ms                                                      | 146 ms: 1.88x slower                                                      |
| nbody          | 85.1 ms                                                      | 189 ms: 2.22x slower                                                      |
| Geometric mean | (ref)                                                        | 1.53x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                     |
| regex_dna      | 180 ms                                                       | 181 ms: 1.01x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                     |
| regex_compile  | 132 ms                                                       | 222 ms: 1.68x slower                                                      |
| Geometric mean | (ref)                                                        | 1.14x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                      |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 108 ms: 1.14x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 111 ms: 1.29x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 15.2 ms: 1.44x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 90.6 ms: 1.53x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 3.14 sec: 1.56x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 413 us: 1.97x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 615 us: 2.09x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.41x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                     |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 78.8 ms: 1.62x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 39.0 ms: 1.81x slower                                                     |
| mako            | 11.3 ms                                                      | 20.9 ms: 1.85x slower                                                     |
| django_template | 34.1 ms                                                      | 63.1 ms: 1.85x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.78x slower                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872 |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                      |
| regex_effbot              | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                     |
| xml_etree_parse           | 136 ms                                                       | 133 ms: 1.03x faster                                                      |
| asyncio_websockets        | 520 ms                                                       | 518 ms: 1.00x faster                                                      |
| regex_dna                 | 180 ms                                                       | 181 ms: 1.01x slower                                                      |
| gc_traversal              | 3.14 ms                                                      | 3.31 ms: 1.05x slower                                                     |
| json                      | 4.93 ms                                                      | 5.23 ms: 1.06x slower                                                     |
| json_loads                | 27.0 us                                                      | 28.7 us: 1.06x slower                                                     |
| async_tree_io             | 876 ms                                                       | 936 ms: 1.07x slower                                                      |
| async_tree_memoization    | 461 ms                                                       | 507 ms: 1.10x slower                                                      |
| sqlite_synth              | 2.21 us                                                      | 2.43 us: 1.10x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 373 ms: 1.11x slower                                                      |
| regex_v8                  | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                     |
| scimark_fft               | 349 ms                                                       | 394 ms: 1.13x slower                                                      |
| xml_etree_iterparse       | 94.9 ms                                                      | 108 ms: 1.14x slower                                                      |
| async_tree_memoization_tg | 414 ms                                                       | 474 ms: 1.15x slower                                                      |
| pathlib                   | 19.2 ms                                                      | 22.0 ms: 1.15x slower                                                     |
| async_tree_none           | 354 ms                                                       | 412 ms: 1.16x slower                                                      |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.50 ms: 1.17x slower                                                     |
| deepcopy                  | 355 us                                                       | 424 us: 1.19x slower                                                      |
| telco                     | 7.82 ms                                                      | 9.51 ms: 1.22x slower                                                     |
| coverage                  | 83.0 ms                                                      | 103 ms: 1.24x slower                                                      |
| async_generators          | 377 ms                                                       | 473 ms: 1.25x slower                                                      |
| docutils                  | 2.62 sec                                                     | 3.32 sec: 1.27x slower                                                    |
| mdp                       | 2.36 sec                                                     | 2.99 sec: 1.27x slower                                                    |
| coroutines                | 23.6 ms                                                      | 30.1 ms: 1.28x slower                                                     |
| create_gc_cycles          | 1.34 ms                                                      | 1.73 ms: 1.29x slower                                                     |
| xml_etree_generate        | 85.4 ms                                                      | 111 ms: 1.29x slower                                                      |
| pylint                    | 317 ms                                                       | 415 ms: 1.31x slower                                                      |
| deepcopy_memo             | 39.1 us                                                      | 52.7 us: 1.35x slower                                                     |
| bpe_tokeniser             | 4.45 sec                                                     | 6.01 sec: 1.35x slower                                                    |
| generators                | 28.8 ms                                                      | 39.2 ms: 1.36x slower                                                     |
| dulwich_log               | 74.8 ms                                                      | 103 ms: 1.38x slower                                                      |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                     |
| meteor_contest            | 102 ms                                                       | 142 ms: 1.40x slower                                                      |
| spectral_norm             | 111 ms                                                       | 157 ms: 1.41x slower                                                      |
| deepcopy_reduce           | 3.11 us                                                      | 4.44 us: 1.43x slower                                                     |
| nqueens                   | 78.6 ms                                                      | 113 ms: 1.43x slower                                                      |
| json_dumps                | 10.5 ms                                                      | 15.2 ms: 1.44x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.67 sec: 1.50x slower                                                    |
| fannkuch                  | 370 ms                                                       | 554 ms: 1.50x slower                                                      |
| html5lib                  | 67.0 ms                                                      | 102 ms: 1.53x slower                                                      |
| xml_etree_process         | 59.3 ms                                                      | 90.6 ms: 1.53x slower                                                     |
| crypto_pyaes              | 67.9 ms                                                      | 105 ms: 1.55x slower                                                      |
| tomli_loads               | 2.01 sec                                                     | 3.14 sec: 1.56x slower                                                    |
| 2to3                      | 260 ms                                                       | 411 ms: 1.58x slower                                                      |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                     |
| genshi_xml                | 48.8 ms                                                      | 78.8 ms: 1.62x slower                                                     |
| typing_runtime_protocols  | 155 us                                                       | 250 us: 1.62x slower                                                      |
| thrift                    | 778 us                                                       | 1.26 ms: 1.62x slower                                                     |
| sympy_integrate           | 19.8 ms                                                      | 32.8 ms: 1.66x slower                                                     |
| regex_compile             | 132 ms                                                       | 222 ms: 1.68x slower                                                      |
| sqlglot_optimize          | 52.7 ms                                                      | 90.2 ms: 1.71x slower                                                     |
| sqlglot_normalize         | 106 ms                                                       | 181 ms: 1.71x slower                                                      |
| pyflate                   | 449 ms                                                       | 767 ms: 1.71x slower                                                      |
| pprint_safe_repr          | 738 ms                                                       | 1.30 sec: 1.77x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 39.0 ms: 1.81x slower                                                     |
| comprehensions            | 16.5 us                                                      | 29.8 us: 1.81x slower                                                     |
| pprint_pformat            | 1.50 sec                                                     | 2.72 sec: 1.82x slower                                                    |
| mako                      | 11.3 ms                                                      | 20.9 ms: 1.85x slower                                                     |
| django_template           | 34.1 ms                                                      | 63.1 ms: 1.85x slower                                                     |
| float                     | 77.5 ms                                                      | 146 ms: 1.88x slower                                                      |
| scimark_monte_carlo       | 65.4 ms                                                      | 124 ms: 1.89x slower                                                      |
| logging_format            | 6.84 us                                                      | 13.2 us: 1.93x slower                                                     |
| logging_simple            | 6.16 us                                                      | 11.9 us: 1.94x slower                                                     |
| scimark_sor               | 134 ms                                                       | 261 ms: 1.94x slower                                                      |
| sympy_str                 | 275 ms                                                       | 534 ms: 1.94x slower                                                      |
| richards                  | 45.2 ms                                                      | 88.7 ms: 1.96x slower                                                     |
| unpickle_pure_python      | 210 us                                                       | 413 us: 1.97x slower                                                      |
| hexiom                    | 5.99 ms                                                      | 12.3 ms: 2.05x slower                                                     |
| richards_super            | 51.6 ms                                                      | 106 ms: 2.06x slower                                                      |
| logging_silent            | 103 ns                                                       | 212 ns: 2.07x slower                                                      |
| go                        | 141 ms                                                       | 292 ms: 2.07x slower                                                      |
| chaos                     | 57.3 ms                                                      | 119 ms: 2.07x slower                                                      |
| sqlglot_transpile         | 1.56 ms                                                      | 3.25 ms: 2.08x slower                                                     |
| pickle_pure_python        | 294 us                                                       | 615 us: 2.09x slower                                                      |
| scimark_lu                | 113 ms                                                       | 243 ms: 2.15x slower                                                      |
| nbody                     | 85.1 ms                                                      | 189 ms: 2.22x slower                                                      |
| sqlglot_parse             | 1.25 ms                                                      | 2.79 ms: 2.24x slower                                                     |
| sympy_expand              | 457 ms                                                       | 1.05 sec: 2.29x slower                                                    |
| sympy_sum                 | 156 ms                                                       | 381 ms: 2.45x slower                                                      |
| raytrace                  | 253 ms                                                       | 626 ms: 2.48x slower                                                      |
| deltablue                 | 3.12 ms                                                      | 8.99 ms: 2.88x slower                                                     |
| bench_thread_pool         | 919 us                                                       | 3.49 ms: 3.80x slower                                                     |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.96x slower                                                      |
| Geometric mean            | (ref)                                                        | 1.54x slower                                                              |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a1+-a9e4872-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-a9e4872.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.31x