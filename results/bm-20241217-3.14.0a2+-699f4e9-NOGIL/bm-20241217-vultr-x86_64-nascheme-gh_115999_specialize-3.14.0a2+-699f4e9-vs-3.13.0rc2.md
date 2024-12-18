# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.231x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 371 ms: 1.43x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.12 sec: 1.19x slower                                                   |
| html5lib       | 67.0 ms                                                      | 98.4 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                        | 1.36x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                     |
| async_tree_io              | 876 ms                                                       | 789 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 613 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 446 ms: 1.03x faster                                                     |
| async_tree_none            | 354 ms                                                       | 368 ms: 1.04x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 25.3 ms: 1.07x slower                                                    |
| async_generators           | 377 ms                                                       | 450 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| float          | 77.5 ms                                                      | 112 ms: 1.45x slower                                                     |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| Geometric mean | (ref)                                                        | 1.23x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                    |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                    |
| regex_compile  | 132 ms                                                       | 174 ms: 1.31x slower                                                     |
| Geometric mean | (ref)                                                        | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 74.3 ms: 1.25x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.56 sec: 1.28x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 346 us: 1.65x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 535 us: 1.82x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                    |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                    |
| django_template | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 759 ms: 1.20x faster                                                     |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| async_tree_io              | 876 ms                                                       | 789 ms: 1.11x faster                                                     |
| deepcopy                   | 355 us                                                       | 321 us: 1.11x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 613 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 446 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.14 us: 1.03x faster                                                    |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                    |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                     |
| json                       | 4.93 ms                                                      | 5.10 ms: 1.03x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 40.5 us: 1.04x slower                                                    |
| async_tree_none            | 354 ms                                                       | 368 ms: 1.04x slower                                                     |
| gc_traversal               | 3.14 ms                                                      | 3.27 ms: 1.04x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 25.3 ms: 1.07x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                    |
| scimark_fft                | 349 ms                                                       | 376 ms: 1.08x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.45 us: 1.11x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.98 sec: 1.12x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.79 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.35 ms: 1.14x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 98.4 ms: 1.15x slower                                                    |
| pylint                     | 317 ms                                                       | 369 ms: 1.16x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.12 sec: 1.19x slower                                                   |
| async_generators           | 377 ms                                                       | 450 ms: 1.19x slower                                                     |
| coverage                   | 83.0 ms                                                      | 100 ms: 1.21x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.87 sec: 1.22x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 91.5 ms: 1.22x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 97.9 ms: 1.25x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 74.3 ms: 1.25x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 66.1 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 134 ms: 1.26x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.56 sec: 1.28x slower                                                   |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| thrift                     | 778 us                                                       | 1.00 ms: 1.29x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.44 sec: 1.29x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 64.0 ms: 1.31x slower                                                    |
| regex_compile              | 132 ms                                                       | 174 ms: 1.31x slower                                                     |
| fannkuch                   | 370 ms                                                       | 487 ms: 1.32x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 90.6 ms: 1.34x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 987 ms: 1.34x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 2.04 sec: 1.36x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| generators                 | 28.8 ms                                                      | 40.1 ms: 1.39x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                    |
| 2to3                       | 260 ms                                                       | 371 ms: 1.43x slower                                                     |
| float                      | 77.5 ms                                                      | 112 ms: 1.45x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 98.4 ms: 1.47x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 29.7 ms: 1.50x slower                                                    |
| logging_format             | 6.84 us                                                      | 10.3 us: 1.50x slower                                                    |
| logging_simple             | 6.16 us                                                      | 9.28 us: 1.51x slower                                                    |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                    |
| django_template            | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                    |
| pyflate                    | 449 ms                                                       | 681 ms: 1.52x slower                                                     |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                    |
| richards_super             | 51.6 ms                                                      | 83.0 ms: 1.61x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 346 us: 1.65x slower                                                     |
| richards                   | 45.2 ms                                                      | 75.2 ms: 1.66x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 189 ms: 1.68x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 10.2 ms: 1.71x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 113 ms: 1.73x slower                                                     |
| sympy_str                  | 275 ms                                                       | 476 ms: 1.73x slower                                                     |
| comprehensions             | 16.5 us                                                      | 28.7 us: 1.75x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 2.73 ms: 1.75x slower                                                    |
| chaos                      | 57.3 ms                                                      | 101 ms: 1.76x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 535 us: 1.82x slower                                                     |
| scimark_sor                | 134 ms                                                       | 245 ms: 1.83x slower                                                     |
| go                         | 141 ms                                                       | 267 ms: 1.90x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.37 ms: 1.90x slower                                                    |
| logging_silent             | 103 ns                                                       | 201 ns: 1.96x slower                                                     |
| sympy_expand               | 457 ms                                                       | 954 ms: 2.09x slower                                                     |
| raytrace                   | 253 ms                                                       | 534 ms: 2.11x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.24x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 8.28 ms: 2.65x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.40 ms: 3.70x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 107 ms: 9.76x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.35x slower                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.231x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.31x