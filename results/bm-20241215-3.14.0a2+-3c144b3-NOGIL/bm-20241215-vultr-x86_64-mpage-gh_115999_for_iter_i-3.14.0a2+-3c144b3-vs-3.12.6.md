# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.080x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 316 ms: 1.20x slower                                                  |
| docutils       | 2.64 sec                                               | 2.85 sec: 1.08x slower                                                |
| html5lib       | 63.6 ms                                                | 75.2 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| async_generators           | 384 ms                                                 | 411 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 67.8 ms: 1.15x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 366 us: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.19x slower                                                 |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 586 ms: 1.89x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                 |
| json                       | 5.02 ms                                                | 4.91 ms: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| go                         | 139 ms                                                 | 138 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.01x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.54 ms: 1.02x slower                                                 |
| spectral_norm              | 110 ms                                                 | 116 ms: 1.05x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                                 |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.23 sec: 1.05x slower                                                |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.26 us: 1.06x slower                                                 |
| pyflate                    | 448 ms                                                 | 477 ms: 1.07x slower                                                  |
| async_generators           | 384 ms                                                 | 411 ms: 1.07x slower                                                  |
| pylint                     | 319 ms                                                 | 342 ms: 1.07x slower                                                  |
| logging_silent             | 109 ns                                                 | 117 ns: 1.07x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.85 sec: 1.08x slower                                                |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                  |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                  |
| scimark_fft                | 342 ms                                                 | 374 ms: 1.10x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.27 us: 1.10x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                                |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                                |
| chaos                      | 62.8 ms                                                | 70.3 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.9 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 836 ms: 1.12x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.14x slower                                                  |
| logging_format             | 7.35 us                                                | 8.36 us: 1.14x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 67.8 ms: 1.15x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.16x slower                                                 |
| scimark_sor                | 130 ms                                                 | 151 ms: 1.16x slower                                                  |
| thrift                     | 791 us                                                 | 920 us: 1.16x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                 |
| nqueens                    | 80.1 ms                                                | 93.7 ms: 1.17x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                 |
| html5lib                   | 63.6 ms                                                | 75.2 ms: 1.18x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.19x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 366 us: 1.19x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 81.5 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.24 ms: 1.19x slower                                                 |
| 2to3                       | 264 ms                                                 | 316 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.43 ms: 1.20x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                  |
| richards                   | 45.9 ms                                                | 56.9 ms: 1.24x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 177 ms: 1.24x slower                                                  |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                 |
| richards_super             | 51.9 ms                                                | 65.6 ms: 1.26x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.27x slower                                                 |
| telco                      | 6.53 ms                                                | 8.36 ms: 1.28x slower                                                 |
| fannkuch                   | 372 ms                                                 | 479 ms: 1.29x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.61 ms: 1.34x slower                                                 |
| coverage                   | 71.4 ms                                                | 98.6 ms: 1.38x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 28.4 ms: 1.38x slower                                                 |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 164 ms: 1.44x slower                                                  |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                                  |
| sympy_str                  | 292 ms                                                 | 454 ms: 1.56x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| sympy_expand               | 468 ms                                                 | 920 ms: 1.97x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 341 ms: 2.05x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 106 ms: 9.79x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                          |

Benchmark hidden because not significant (2): float, comprehensions
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241215-3.14.0a2+-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x