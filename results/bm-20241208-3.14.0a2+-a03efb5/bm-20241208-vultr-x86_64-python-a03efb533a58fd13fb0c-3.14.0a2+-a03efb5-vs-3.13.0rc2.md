# Results vs. 3.13.0rc2

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.030x faster
- HPT reliability: 99.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.44x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 339 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 332 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 274 ms: 1.23x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                  |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 79.6 ms: 1.03x slower                                                  |
| nbody          | 85.1 ms                                                      | 94.8 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 129 ms: 1.03x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 126 ms: 1.08x faster                                                   |
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 85.1 ms: 1.00x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 323 us: 1.10x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 619 ms: 1.48x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.44x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 339 ms: 1.36x faster                                                   |
| deepcopy                   | 355 us                                                       | 262 us: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.5 us: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 332 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 274 ms: 1.23x faster                                                   |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                  |
| json                       | 4.93 ms                                                      | 4.53 ms: 1.09x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.19 ms: 1.09x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 126 ms: 1.08x faster                                                   |
| json_loads                 | 27.0 us                                                      | 25.0 us: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.06x faster                                                  |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.8 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 752 us: 1.04x faster                                                   |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                   |
| regex_compile              | 132 ms                                                       | 129 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.58 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.33 sec: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.03 us: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.89 ms: 1.02x faster                                                  |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 727 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.7 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.49 sec: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| pyflate                    | 449 ms                                                       | 446 ms: 1.01x faster                                                   |
| richards_super             | 51.6 ms                                                      | 51.4 ms: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.6 ms: 1.00x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 85.1 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                   |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 75.4 ms: 1.01x slower                                                  |
| sympy_expand               | 457 ms                                                       | 461 ms: 1.01x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 79.5 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 53.7 ms: 1.02x slower                                                  |
| chaos                      | 57.3 ms                                                      | 58.4 ms: 1.02x slower                                                  |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| fannkuch                   | 370 ms                                                       | 378 ms: 1.02x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                  |
| float                      | 77.5 ms                                                      | 79.6 ms: 1.03x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                                   |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.9 ms: 1.04x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.48 sec: 1.05x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 323 us: 1.10x slower                                                   |
| nbody                      | 85.1 ms                                                      | 94.8 ms: 1.11x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.71 ms: 1.28x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.07 ms: 1.30x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 85.7 ms: 7.80x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (7): pycparser, sympy_str, generators, xml_etree_process, logging_format, richards, scimark_lu
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241208-3.14.0a2+-a03efb5/bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 99.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x