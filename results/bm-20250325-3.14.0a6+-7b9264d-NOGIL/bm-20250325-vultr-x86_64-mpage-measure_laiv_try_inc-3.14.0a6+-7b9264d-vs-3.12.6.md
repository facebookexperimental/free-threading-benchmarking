# Results vs. 3.12.6

- fork: mpage
- ref: measure_laiv_try_inc
- machine: linux-x86_64
- commit hash: 7b9264d
- commit date: 2025-03-25
- overall geometric mean: 1.046x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 299 ms: 1.14x slower                                                  |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 582 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.2 ms: 1.03x faster                                                 |
| pidigits       | 184 ms                                                 | 211 ms: 1.15x slower                                                  |
| nbody          | 89.3 ms                                                | 136 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| regex_compile  | 142 ms                                                 | 158 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 257 us: 1.16x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 554 ms: 2.00x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.90x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 300 ms: 1.86x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 582 ms: 1.86x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                                 |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 78.2 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                                 |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.88 sec: 1.03x slower                                                |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                  |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.24 us: 1.05x slower                                                 |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.05x slower                                                 |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.61 sec: 1.08x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                                 |
| raytrace                   | 299 ms                                                 | 325 ms: 1.08x slower                                                  |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                 |
| chaos                      | 62.8 ms                                                | 68.8 ms: 1.09x slower                                                 |
| thrift                     | 791 us                                                 | 869 us: 1.10x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                  |
| regex_compile              | 142 ms                                                 | 158 ms: 1.11x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| pyflate                    | 448 ms                                                 | 497 ms: 1.11x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.36 us: 1.11x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.88 ms: 1.12x slower                                                 |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 842 ms: 1.13x slower                                                  |
| 2to3                       | 264 ms                                                 | 299 ms: 1.14x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                 |
| pidigits                   | 184 ms                                                 | 211 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 88.9 ms: 1.16x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 257 us: 1.16x slower                                                  |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                  |
| sympy_expand               | 468 ms                                                 | 554 ms: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.8 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 55.8 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.3 ms: 1.22x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 84.2 ms: 1.23x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.68 ms: 1.24x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.6 ms: 1.25x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.25x slower                                                  |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.70 ms: 1.30x slower                                                 |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                                  |
| telco                      | 6.53 ms                                                | 8.99 ms: 1.38x slower                                                 |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| coverage                   | 71.4 ms                                                | 108 ms: 1.51x slower                                                  |
| nbody                      | 89.3 ms                                                | 136 ms: 1.52x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 97.0 ms: 8.98x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250325-3.14.0a6+-7b9264d-NOGIL/bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x