# Results vs. 3.13.0rc2

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.254x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 371 ms: 1.43x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                 |
| html5lib       | 67.0 ms                                                      | 98.7 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 646 ms: 1.03x faster                                                   |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.08x slower                                                   |
| async_tree_none            | 354 ms                                                       | 385 ms: 1.09x slower                                                   |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| float          | 77.5 ms                                                      | 140 ms: 1.81x slower                                                   |
| Geometric mean | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| regex_compile  | 132 ms                                                       | 182 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 97.9 ms: 1.15x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 77.9 ms: 1.31x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.70 sec: 1.35x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 335 us: 1.59x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 514 us: 1.74x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 65.0 ms: 1.33x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 31.9 ms: 1.48x slower                                                  |
| django_template | 34.1 ms                                                      | 50.8 ms: 1.49x slower                                                  |
| mako            | 11.3 ms                                                      | 17.9 ms: 1.58x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.47x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.11x faster                                                   |
| deepcopy                   | 355 us                                                       | 329 us: 1.08x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 646 ms: 1.03x faster                                                   |
| async_tree_io              | 876 ms                                                       | 850 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 40.4 us: 1.03x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.28 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.10 ms: 1.03x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 20.2 ms: 1.05x slower                                                  |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.08x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| async_tree_none            | 354 ms                                                       | 385 ms: 1.09x slower                                                   |
| spectral_norm              | 111 ms                                                       | 123 ms: 1.11x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.71 ms: 1.11x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 5.04 sec: 1.13x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.53 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.9 ms: 1.15x slower                                                  |
| scimark_fft                | 349 ms                                                       | 412 ms: 1.18x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                  |
| pylint                     | 317 ms                                                       | 384 ms: 1.21x slower                                                   |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 97.9 ms: 1.25x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.96 sec: 1.26x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 97.0 ms: 1.30x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 6.12 ms: 1.30x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 138 ms: 1.30x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 77.9 ms: 1.31x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 69.7 ms: 1.32x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 65.0 ms: 1.33x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 988 ms: 1.34x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.70 sec: 1.35x slower                                                 |
| generators                 | 28.8 ms                                                      | 38.8 ms: 1.35x slower                                                  |
| fannkuch                   | 370 ms                                                       | 501 ms: 1.36x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 92.2 ms: 1.36x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 2.04 sec: 1.36x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                  |
| regex_compile              | 132 ms                                                       | 182 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.57 sec: 1.40x slower                                                 |
| 2to3                       | 260 ms                                                       | 371 ms: 1.43x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 98.7 ms: 1.47x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 31.9 ms: 1.48x slower                                                  |
| django_template            | 34.1 ms                                                      | 50.8 ms: 1.49x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                  |
| thrift                     | 778 us                                                       | 1.18 ms: 1.52x slower                                                  |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                   |
| pyflate                    | 449 ms                                                       | 694 ms: 1.55x slower                                                   |
| mako                       | 11.3 ms                                                      | 17.9 ms: 1.58x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 335 us: 1.59x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.89 ms: 1.65x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 187 ms: 1.66x slower                                                   |
| comprehensions             | 16.5 us                                                      | 27.5 us: 1.67x slower                                                  |
| richards                   | 45.2 ms                                                      | 77.2 ms: 1.71x slower                                                  |
| richards_super             | 51.6 ms                                                      | 88.5 ms: 1.71x slower                                                  |
| sympy_str                  | 275 ms                                                       | 478 ms: 1.74x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 514 us: 1.74x slower                                                   |
| logging_simple             | 6.16 us                                                      | 10.9 us: 1.76x slower                                                  |
| logging_format             | 6.84 us                                                      | 12.1 us: 1.76x slower                                                  |
| scimark_sor                | 134 ms                                                       | 238 ms: 1.77x slower                                                   |
| float                      | 77.5 ms                                                      | 140 ms: 1.81x slower                                                   |
| logging_silent             | 103 ns                                                       | 188 ns: 1.83x slower                                                   |
| chaos                      | 57.3 ms                                                      | 105 ms: 1.84x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 120 ms: 1.84x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.99 ms: 1.92x slower                                                  |
| go                         | 141 ms                                                       | 272 ms: 1.93x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 2.61 ms: 2.09x slower                                                  |
| sympy_expand               | 457 ms                                                       | 961 ms: 2.10x slower                                                   |
| raytrace                   | 253 ms                                                       | 551 ms: 2.18x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 350 ms: 2.25x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 7.95 ms: 2.54x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.42 ms: 3.73x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.93x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.39x slower                                                           |

Benchmark hidden because not significant (1): async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.254x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.20x

# Memory
- memory change: 1.31x