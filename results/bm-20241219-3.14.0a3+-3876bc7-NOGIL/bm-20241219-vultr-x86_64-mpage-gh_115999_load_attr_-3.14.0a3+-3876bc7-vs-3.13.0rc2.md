# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 3876bc7
- commit date: 2024-12-19
- overall geometric mean: 1.120x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 324 ms: 1.25x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.86 sec: 1.09x slower                                                |
| html5lib       | 67.0 ms                                                      | 74.1 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 524 ms: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| async_generators           | 377 ms                                                       | 430 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| float          | 77.5 ms                                                      | 82.7 ms: 1.07x slower                                                 |
| nbody          | 85.1 ms                                                      | 135 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| regex_compile  | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.2 ms: 1.17x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 252 us: 1.20x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.50 sec: 1.25x slower                                                |
| pickle_pure_python   | 294 us                                                       | 372 us: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.8 ms: 1.25x slower                                                 |
| django_template | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                 |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 605 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 524 ms: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| pidigits                   | 217 ms                                                       | 181 ms: 1.19x faster                                                  |
| deepcopy                   | 355 us                                                       | 314 us: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.8 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.3 us: 1.01x slower                                                 |
| json                       | 4.93 ms                                                      | 5.00 ms: 1.01x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                 |
| go                         | 141 ms                                                       | 144 ms: 1.03x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.23 us: 1.04x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| float                      | 77.5 ms                                                      | 82.7 ms: 1.07x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.81 sec: 1.08x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.21 sec: 1.09x slower                                                |
| generators                 | 28.8 ms                                                      | 31.3 ms: 1.09x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.86 sec: 1.09x slower                                                |
| pylint                     | 317 ms                                                       | 347 ms: 1.09x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.62 ms: 1.10x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 74.1 ms: 1.11x slower                                                 |
| scimark_fft                | 349 ms                                                       | 386 ms: 1.11x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.8 ms: 1.11x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.61 sec: 1.11x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 3.50 ms: 1.11x slower                                                 |
| logging_silent             | 103 ns                                                       | 115 ns: 1.12x slower                                                  |
| pyflate                    | 449 ms                                                       | 504 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                 |
| async_generators           | 377 ms                                                       | 430 ms: 1.14x slower                                                  |
| regex_compile              | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.15x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 849 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 61.2 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.2 ms: 1.17x slower                                                 |
| thrift                     | 778 us                                                       | 911 us: 1.17x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.76 sec: 1.17x slower                                                |
| logging_simple             | 6.16 us                                                      | 7.26 us: 1.18x slower                                                 |
| coverage                   | 83.0 ms                                                      | 98.6 ms: 1.19x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 252 us: 1.20x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.26 us: 1.21x slower                                                 |
| scimark_sor                | 134 ms                                                       | 162 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.78 ms: 1.23x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 97.4 ms: 1.24x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.94 ms: 1.25x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.50 sec: 1.25x slower                                                |
| genshi_xml                 | 48.8 ms                                                      | 60.8 ms: 1.25x slower                                                 |
| 2to3                       | 260 ms                                                       | 324 ms: 1.25x slower                                                  |
| richards                   | 45.2 ms                                                      | 56.5 ms: 1.25x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 141 ms: 1.25x slower                                                  |
| django_template            | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 372 us: 1.26x slower                                                  |
| chaos                      | 57.3 ms                                                      | 72.4 ms: 1.26x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.61 ms: 1.27x slower                                                 |
| richards_super             | 51.6 ms                                                      | 65.8 ms: 1.27x slower                                                 |
| raytrace                   | 253 ms                                                       | 322 ms: 1.27x slower                                                  |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.61 ms: 1.29x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 88.0 ms: 1.30x slower                                                 |
| fannkuch                   | 370 ms                                                       | 488 ms: 1.32x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 86.9 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.9 ms: 1.46x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.84 ms: 1.55x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.56x slower                                                 |
| nbody                      | 85.1 ms                                                      | 135 ms: 1.59x slower                                                  |
| sympy_str                  | 275 ms                                                       | 461 ms: 1.68x slower                                                  |
| sympy_expand               | 457 ms                                                       | 931 ms: 2.04x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 342 ms: 2.20x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 106 ms: 9.62x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.18x slower                                                          |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241219-3.14.0a3+-3876bc7-NOGIL/bm-20241219-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-3876bc7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.120x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.33x