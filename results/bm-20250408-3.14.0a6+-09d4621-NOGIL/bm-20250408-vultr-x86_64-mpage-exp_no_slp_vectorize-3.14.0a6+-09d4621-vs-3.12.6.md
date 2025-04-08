# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.017x slower
- HPT reliability: 99.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                |
| html5lib       | 63.6 ms                                                | 70.7 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.89x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 532 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                  |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                 |
| pidigits       | 184 ms                                                 | 218 ms: 1.18x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                 |
| regex_compile  | 142 ms                                                 | 153 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 349 us: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.8 ms: 1.22x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 537 ms: 2.07x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.94x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.89x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.37 sec: 1.76x faster                                                |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 532 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                  |
| deepcopy                   | 352 us                                                 | 300 us: 1.17x faster                                                  |
| float                      | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.9 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.2 ms: 1.08x faster                                                 |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                                  |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                                |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.05 us: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| scimark_sor                | 130 ms                                                 | 129 ms: 1.00x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                 |
| comprehensions             | 19.8 us                                                | 20.3 us: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                 |
| raytrace                   | 299 ms                                                 | 309 ms: 1.03x slower                                                  |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                                 |
| scimark_fft                | 342 ms                                                 | 356 ms: 1.04x slower                                                  |
| chaos                      | 62.8 ms                                                | 65.4 ms: 1.04x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.26 sec: 1.07x slower                                                |
| regex_compile              | 142 ms                                                 | 153 ms: 1.07x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 811 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                  |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                 |
| pyflate                    | 448 ms                                                 | 494 ms: 1.10x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.7 ms: 1.11x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 159 ms: 1.11x slower                                                  |
| 2to3                       | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                                |
| logging_simple             | 6.63 us                                                | 7.40 us: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.88 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.3 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 330 ms: 1.13x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.3 ms: 1.13x slower                                                 |
| nqueens                    | 80.1 ms                                                | 90.7 ms: 1.13x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 349 us: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.1 ms: 1.14x slower                                                 |
| logging_format             | 7.35 us                                                | 8.37 us: 1.14x slower                                                 |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.16x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.27 ms: 1.18x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                                  |
| pidigits                   | 184 ms                                                 | 218 ms: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.22 ms: 1.19x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                 |
| richards                   | 45.9 ms                                                | 55.1 ms: 1.20x slower                                                 |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.8 ms: 1.22x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                 |
| richards_super             | 51.9 ms                                                | 63.4 ms: 1.22x slower                                                 |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 470 ms: 1.26x slower                                                  |
| telco                      | 6.53 ms                                                | 8.41 ms: 1.29x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                 |
| coverage                   | 71.4 ms                                                | 107 ms: 1.50x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 96.3 ms: 8.92x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (2): pylint, pycparser
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.017x slower

# HPT report

- Reliability score: 99.05% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x