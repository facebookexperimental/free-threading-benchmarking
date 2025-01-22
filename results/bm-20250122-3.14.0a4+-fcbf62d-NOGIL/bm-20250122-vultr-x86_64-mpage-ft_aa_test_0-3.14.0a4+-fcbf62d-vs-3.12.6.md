# Results vs. 3.12.6

- fork: mpage
- ref: ft_aa_test_0
- machine: linux-x86_64
- commit hash: fcbf62d
- commit date: 2025-01-22
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 314 ms: 1.19x slower                                          |
| docutils       | 2.64 sec                                               | 2.86 sec: 1.08x slower                                        |
| html5lib       | 63.6 ms                                                | 74.9 ms: 1.18x slower                                         |
| Geometric mean | (ref)                                                  | 1.15x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                          |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                          |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.56x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                          |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                          |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                          |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                         |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.0 ms: 1.04x faster                                         |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                          |
| nbody          | 89.3 ms                                                | 141 ms: 1.58x slower                                          |
| Geometric mean | (ref)                                                  | 1.17x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                         |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                          |
| regex_compile  | 142 ms                                                 | 160 ms: 1.12x slower                                          |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                         |
| Geometric mean | (ref)                                                  | 1.07x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                         |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                          |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                         |
| xml_etree_generate   | 85.2 ms                                                | 99.0 ms: 1.16x slower                                         |
| tomli_loads          | 2.11 sec                                               | 2.49 sec: 1.18x slower                                        |
| unpickle_pure_python | 221 us                                                 | 275 us: 1.25x slower                                          |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                         |
| xml_etree_process    | 59.0 ms                                                | 75.6 ms: 1.28x slower                                         |
| pickle_pure_python   | 308 us                                                 | 399 us: 1.30x slower                                          |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.53 ms: 1.33x slower                                         |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                         |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.0 ms: 1.28x slower                                         |
| django_template | 34.7 ms                                                | 45.0 ms: 1.30x slower                                         |
| genshi_text     | 22.8 ms                                                | 29.9 ms: 1.31x slower                                         |
| mako            | 11.0 ms                                                | 16.3 ms: 1.48x slower                                         |
| Geometric mean  | (ref)                                                  | 1.34x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.81x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                          |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                          |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.56x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                          |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                         |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                         |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                          |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                         |
| deepcopy                   | 352 us                                                 | 328 us: 1.07x faster                                          |
| gc_traversal               | 3.46 ms                                                | 3.25 ms: 1.06x faster                                         |
| float                      | 80.8 ms                                                | 78.0 ms: 1.04x faster                                         |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                          |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                          |
| deepcopy_memo              | 40.3 us                                                | 40.8 us: 1.01x slower                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.82 sec: 1.02x slower                                        |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                          |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                         |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                          |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                          |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                         |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                         |
| dulwich_log                | 78.9 ms                                                | 83.8 ms: 1.06x slower                                         |
| pycparser                  | 1.17 sec                                               | 1.24 sec: 1.06x slower                                        |
| comprehensions             | 19.8 us                                                | 21.3 us: 1.08x slower                                         |
| docutils                   | 2.64 sec                                               | 2.86 sec: 1.08x slower                                        |
| scimark_sor                | 130 ms                                                 | 141 ms: 1.08x slower                                          |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                          |
| logging_silent             | 109 ns                                                 | 121 ns: 1.11x slower                                          |
| deepcopy_reduce            | 3.08 us                                                | 3.44 us: 1.12x slower                                         |
| regex_compile              | 142 ms                                                 | 160 ms: 1.12x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                         |
| mdp                        | 2.42 sec                                               | 2.74 sec: 1.13x slower                                        |
| sqlalchemy_declarative     | 143 ms                                                 | 162 ms: 1.13x slower                                          |
| raytrace                   | 299 ms                                                 | 340 ms: 1.14x slower                                          |
| chaos                      | 62.8 ms                                                | 72.1 ms: 1.15x slower                                         |
| sympy_sum                  | 166 ms                                                 | 191 ms: 1.15x slower                                          |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                         |
| pprint_safe_repr           | 743 ms                                                 | 859 ms: 1.16x slower                                          |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                         |
| crypto_pyaes               | 76.6 ms                                                | 88.9 ms: 1.16x slower                                         |
| xml_etree_generate         | 85.2 ms                                                | 99.0 ms: 1.16x slower                                         |
| sqlglot_normalize          | 107 ms                                                 | 124 ms: 1.16x slower                                          |
| scimark_fft                | 342 ms                                                 | 398 ms: 1.16x slower                                          |
| pprint_pformat             | 1.52 sec                                               | 1.78 sec: 1.17x slower                                        |
| thrift                     | 791 us                                                 | 925 us: 1.17x slower                                          |
| pyflate                    | 448 ms                                                 | 525 ms: 1.17x slower                                          |
| sqlglot_optimize           | 53.3 ms                                                | 62.5 ms: 1.17x slower                                         |
| logging_simple             | 6.63 us                                                | 7.80 us: 1.18x slower                                         |
| html5lib                   | 63.6 ms                                                | 74.9 ms: 1.18x slower                                         |
| tomli_loads                | 2.11 sec                                               | 2.49 sec: 1.18x slower                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.61 ms: 1.19x slower                                         |
| sympy_str                  | 292 ms                                                 | 346 ms: 1.19x slower                                          |
| 2to3                       | 264 ms                                                 | 314 ms: 1.19x slower                                          |
| sqlglot_transpile          | 1.67 ms                                                | 2.00 ms: 1.19x slower                                         |
| sympy_expand               | 468 ms                                                 | 561 ms: 1.20x slower                                          |
| logging_format             | 7.35 us                                                | 8.81 us: 1.20x slower                                         |
| create_gc_cycles           | 1.09 ms                                                | 1.32 ms: 1.21x slower                                         |
| sympy_integrate            | 20.5 ms                                                | 24.9 ms: 1.21x slower                                         |
| richards                   | 45.9 ms                                                | 56.6 ms: 1.23x slower                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 84.3 ms: 1.23x slower                                         |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.25x slower                                          |
| unpickle_pure_python       | 221 us                                                 | 275 us: 1.25x slower                                          |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                         |
| nqueens                    | 80.1 ms                                                | 101 ms: 1.26x slower                                          |
| hexiom                     | 6.17 ms                                                | 7.77 ms: 1.26x slower                                         |
| richards_super             | 51.9 ms                                                | 66.0 ms: 1.27x slower                                         |
| genshi_xml                 | 50.2 ms                                                | 64.0 ms: 1.28x slower                                         |
| xml_etree_process          | 59.0 ms                                                | 75.6 ms: 1.28x slower                                         |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.28x slower                                          |
| typing_runtime_protocols   | 163 us                                                 | 211 us: 1.29x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                         |
| pickle_pure_python         | 308 us                                                 | 399 us: 1.30x slower                                          |
| django_template            | 34.7 ms                                                | 45.0 ms: 1.30x slower                                         |
| genshi_text                | 22.8 ms                                                | 29.9 ms: 1.31x slower                                         |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                         |
| python_startup_no_site     | 7.16 ms                                                | 9.53 ms: 1.33x slower                                         |
| fannkuch                   | 372 ms                                                 | 502 ms: 1.35x slower                                          |
| coverage                   | 71.4 ms                                                | 98.8 ms: 1.38x slower                                         |
| deltablue                  | 3.45 ms                                                | 4.77 ms: 1.38x slower                                         |
| mako                       | 11.0 ms                                                | 16.3 ms: 1.48x slower                                         |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                         |
| nbody                      | 89.3 ms                                                | 141 ms: 1.58x slower                                          |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                         |
| bench_mp_pool              | 10.8 ms                                                | 95.4 ms: 8.84x slower                                         |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                  |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250122-3.14.0a4+-fcbf62d-NOGIL/bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4+-fcbf62d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x