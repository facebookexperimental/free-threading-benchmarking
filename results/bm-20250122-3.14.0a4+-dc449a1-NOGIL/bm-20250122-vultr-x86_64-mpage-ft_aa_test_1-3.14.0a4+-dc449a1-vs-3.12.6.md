# Results vs. 3.12.6

- fork: mpage
- ref: ft_aa_test_1
- machine: linux-x86_64
- commit hash: dc449a1
- commit date: 2025-01-22
- overall geometric mean: 1.079x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 314 ms: 1.19x slower                                          |
| docutils       | 2.64 sec                                               | 2.87 sec: 1.09x slower                                        |
| html5lib       | 63.6 ms                                                | 74.6 ms: 1.17x slower                                         |
| Geometric mean | (ref)                                                  | 1.15x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 585 ms: 1.90x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.76x faster                                          |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                          |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                          |
| async_generators           | 384 ms                                                 | 378 ms: 1.02x faster                                          |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                         |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                  |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.5 ms: 1.04x faster                                         |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                          |
| nbody          | 89.3 ms                                                | 136 ms: 1.53x slower                                          |
| Geometric mean | (ref)                                                  | 1.15x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                         |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                          |
| regex_compile  | 142 ms                                                 | 159 ms: 1.12x slower                                          |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                         |
| Geometric mean | (ref)                                                  | 1.07x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.7 ms: 1.09x faster                                         |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                          |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                         |
| tomli_loads          | 2.11 sec                                               | 2.43 sec: 1.16x slower                                        |
| xml_etree_generate   | 85.2 ms                                                | 99.3 ms: 1.17x slower                                         |
| unpickle_pure_python | 221 us                                                 | 275 us: 1.25x slower                                          |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                         |
| pickle_pure_python   | 308 us                                                 | 395 us: 1.28x slower                                          |
| xml_etree_process    | 59.0 ms                                                | 77.1 ms: 1.31x slower                                         |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                         |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.54x slower                                         |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.0 ms: 1.28x slower                                         |
| django_template | 34.7 ms                                                | 45.0 ms: 1.30x slower                                         |
| genshi_text     | 22.8 ms                                                | 30.3 ms: 1.33x slower                                         |
| mako            | 11.0 ms                                                | 16.3 ms: 1.48x slower                                         |
| Geometric mean  | (ref)                                                  | 1.34x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 585 ms: 1.90x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 246 ms: 1.82x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.76x faster                                          |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                          |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                          |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                         |
| gc_traversal               | 3.46 ms                                                | 3.13 ms: 1.11x faster                                         |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                         |
| xml_etree_iterparse        | 96.7 ms                                                | 88.7 ms: 1.09x faster                                         |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                          |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                         |
| deepcopy                   | 352 us                                                 | 330 us: 1.07x faster                                          |
| float                      | 80.8 ms                                                | 77.5 ms: 1.04x faster                                         |
| async_generators           | 384 ms                                                 | 378 ms: 1.02x faster                                          |
| deepcopy_memo              | 40.3 us                                                | 41.0 us: 1.02x slower                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.82 sec: 1.02x slower                                        |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                          |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                          |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                          |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                         |
| generators                 | 32.2 ms                                                | 33.9 ms: 1.05x slower                                         |
| json                       | 5.02 ms                                                | 5.32 ms: 1.06x slower                                         |
| pycparser                  | 1.17 sec                                               | 1.24 sec: 1.06x slower                                        |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                          |
| dulwich_log                | 78.9 ms                                                | 84.5 ms: 1.07x slower                                         |
| comprehensions             | 19.8 us                                                | 21.3 us: 1.07x slower                                         |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                          |
| docutils                   | 2.64 sec                                               | 2.87 sec: 1.09x slower                                        |
| deepcopy_reduce            | 3.08 us                                                | 3.39 us: 1.10x slower                                         |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                        |
| logging_silent             | 109 ns                                                 | 121 ns: 1.11x slower                                          |
| regex_compile              | 142 ms                                                 | 159 ms: 1.12x slower                                          |
| scimark_fft                | 342 ms                                                 | 382 ms: 1.12x slower                                          |
| raytrace                   | 299 ms                                                 | 338 ms: 1.13x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.6 ms: 1.13x slower                                         |
| crypto_pyaes               | 76.6 ms                                                | 86.9 ms: 1.13x slower                                         |
| chaos                      | 62.8 ms                                                | 71.6 ms: 1.14x slower                                         |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                         |
| pyflate                    | 448 ms                                                 | 515 ms: 1.15x slower                                          |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                          |
| pprint_safe_repr           | 743 ms                                                 | 858 ms: 1.16x slower                                          |
| tomli_loads                | 2.11 sec                                               | 2.43 sec: 1.16x slower                                        |
| pprint_pformat             | 1.52 sec                                               | 1.77 sec: 1.16x slower                                        |
| sympy_sum                  | 166 ms                                                 | 193 ms: 1.16x slower                                          |
| xml_etree_generate         | 85.2 ms                                                | 99.3 ms: 1.17x slower                                         |
| thrift                     | 791 us                                                 | 925 us: 1.17x slower                                          |
| sqlglot_normalize          | 107 ms                                                 | 125 ms: 1.17x slower                                          |
| html5lib                   | 63.6 ms                                                | 74.6 ms: 1.17x slower                                         |
| sqlglot_optimize           | 53.3 ms                                                | 62.7 ms: 1.18x slower                                         |
| logging_simple             | 6.63 us                                                | 7.82 us: 1.18x slower                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                         |
| sqlglot_transpile          | 1.67 ms                                                | 1.99 ms: 1.19x slower                                         |
| sympy_str                  | 292 ms                                                 | 347 ms: 1.19x slower                                          |
| 2to3                       | 264 ms                                                 | 314 ms: 1.19x slower                                          |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                         |
| create_gc_cycles           | 1.09 ms                                                | 1.31 ms: 1.20x slower                                         |
| logging_format             | 7.35 us                                                | 8.90 us: 1.21x slower                                         |
| sympy_expand               | 468 ms                                                 | 567 ms: 1.21x slower                                          |
| sympy_integrate            | 20.5 ms                                                | 25.0 ms: 1.22x slower                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 83.7 ms: 1.22x slower                                         |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                          |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.43 ms: 1.24x slower                                         |
| hexiom                     | 6.17 ms                                                | 7.67 ms: 1.24x slower                                         |
| richards                   | 45.9 ms                                                | 57.3 ms: 1.25x slower                                         |
| unpickle_pure_python       | 221 us                                                 | 275 us: 1.25x slower                                          |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                         |
| nqueens                    | 80.1 ms                                                | 101 ms: 1.26x slower                                          |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 64.0 ms: 1.28x slower                                         |
| pickle_pure_python         | 308 us                                                 | 395 us: 1.28x slower                                          |
| django_template            | 34.7 ms                                                | 45.0 ms: 1.30x slower                                         |
| telco                      | 6.53 ms                                                | 8.50 ms: 1.30x slower                                         |
| richards_super             | 51.9 ms                                                | 67.7 ms: 1.30x slower                                         |
| xml_etree_process          | 59.0 ms                                                | 77.1 ms: 1.31x slower                                         |
| typing_runtime_protocols   | 163 us                                                 | 214 us: 1.31x slower                                          |
| genshi_text                | 22.8 ms                                                | 30.3 ms: 1.33x slower                                         |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                         |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.34x slower                                          |
| coverage                   | 71.4 ms                                                | 98.3 ms: 1.38x slower                                         |
| deltablue                  | 3.45 ms                                                | 4.78 ms: 1.39x slower                                         |
| mako                       | 11.0 ms                                                | 16.3 ms: 1.48x slower                                         |
| nbody                      | 89.3 ms                                                | 136 ms: 1.53x slower                                          |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.54x slower                                         |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                         |
| bench_mp_pool              | 10.8 ms                                                | 95.5 ms: 8.85x slower                                         |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                  |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250122-3.14.0a4+-dc449a1-NOGIL/bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4+-dc449a1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x