# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 40f5577
- commit date: 2024-12-17
- overall geometric mean: 1.215x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 360 ms: 1.39x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.06 sec: 1.17x slower                                                |
| html5lib       | 67.0 ms                                                      | 94.1 ms: 1.40x slower                                                 |
| Geometric mean | (ref)                                                        | 1.32x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 732 ms: 1.25x faster                                                  |
| async_tree_io              | 876 ms                                                       | 760 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 600 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 579 ms: 1.10x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 323 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 448 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| float          | 77.5 ms                                                      | 111 ms: 1.43x slower                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                        | 1.21x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.98 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                 |
| regex_compile  | 132 ms                                                       | 170 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 73.9 ms: 1.24x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.53 sec: 1.26x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.0 ms: 1.33x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 327 us: 1.56x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 504 us: 1.71x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.6 ms: 1.28x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 30.0 ms: 1.39x slower                                                 |
| django_template | 34.1 ms                                                      | 50.0 ms: 1.46x slower                                                 |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 732 ms: 1.25x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| async_tree_io              | 876 ms                                                       | 760 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 600 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 579 ms: 1.10x faster                                                  |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.2 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 323 ms: 1.04x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.98 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.8 us: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.6 ms: 1.02x slower                                                 |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.28 ms: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| scimark_fft                | 349 ms                                                       | 372 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.42 us: 1.10x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.65 ms: 1.11x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.96 sec: 1.11x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.69 sec: 1.14x slower                                                |
| pylint                     | 317 ms                                                       | 365 ms: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.42 ms: 1.15x slower                                                 |
| docutils                   | 2.62 sec                                                     | 3.06 sec: 1.17x slower                                                |
| async_generators           | 377 ms                                                       | 448 ms: 1.19x slower                                                  |
| coverage                   | 83.0 ms                                                      | 100 ms: 1.21x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 91.2 ms: 1.22x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 73.9 ms: 1.24x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 65.8 ms: 1.25x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 98.2 ms: 1.25x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.40 sec: 1.25x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.53 sec: 1.26x slower                                                |
| thrift                     | 778 us                                                       | 987 us: 1.27x slower                                                  |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| regex_compile              | 132 ms                                                       | 170 ms: 1.28x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 62.6 ms: 1.28x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 961 ms: 1.30x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.0 ms: 1.31x slower                                                 |
| fannkuch                   | 370 ms                                                       | 486 ms: 1.31x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.0 ms: 1.33x slower                                                 |
| generators                 | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.34x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.80 ms: 1.34x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 208 us: 1.35x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| 2to3                       | 260 ms                                                       | 360 ms: 1.39x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 30.0 ms: 1.39x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 94.1 ms: 1.40x slower                                                 |
| float                      | 77.5 ms                                                      | 111 ms: 1.43x slower                                                  |
| pyflate                    | 449 ms                                                       | 650 ms: 1.45x slower                                                  |
| django_template            | 34.1 ms                                                      | 50.0 ms: 1.46x slower                                                 |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                  |
| logging_simple             | 6.16 us                                                      | 9.08 us: 1.47x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.4 ms: 1.48x slower                                                 |
| logging_format             | 6.84 us                                                      | 10.2 us: 1.49x slower                                                 |
| richards_super             | 51.6 ms                                                      | 77.5 ms: 1.50x slower                                                 |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                 |
| richards                   | 45.2 ms                                                      | 68.9 ms: 1.52x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 327 us: 1.56x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 105 ms: 1.61x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 183 ms: 1.62x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.72 ms: 1.62x slower                                                 |
| chaos                      | 57.3 ms                                                      | 95.1 ms: 1.66x slower                                                 |
| comprehensions             | 16.5 us                                                      | 27.5 us: 1.67x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 504 us: 1.71x slower                                                  |
| scimark_sor                | 134 ms                                                       | 231 ms: 1.71x slower                                                  |
| go                         | 141 ms                                                       | 243 ms: 1.73x slower                                                  |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.70 ms: 1.73x slower                                                 |
| logging_silent             | 103 ns                                                       | 185 ns: 1.80x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.34 ms: 1.87x slower                                                 |
| raytrace                   | 253 ms                                                       | 498 ms: 1.97x slower                                                  |
| sympy_expand               | 457 ms                                                       | 956 ms: 2.09x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 347 ms: 2.23x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 7.60 ms: 2.43x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.67x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 107 ms: 9.73x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.32x slower                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a3+-40f5577-NOGIL/bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.215x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.31x