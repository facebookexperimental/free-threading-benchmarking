# Results vs. 3.13.0rc2

- fork: python
- ref: cfeaa992ba9bad9be268
- machine: linux-x86_64
- commit hash: cfeaa99
- commit date: 2024-12-16
- overall geometric mean: 1.049x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 622 ms: 1.41x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 333 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                  |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| nbody          | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.7 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.3 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.9 ms: 1.02x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.00x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 319 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 622 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 333 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.7 us: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                   |
| go                         | 141 ms                                                       | 117 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| spectral_norm              | 111 ms                                                       | 96.4 ms: 1.15x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.09 ms: 1.15x faster                                                  |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                   |
| telco                      | 7.82 ms                                                      | 7.14 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                  |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| coverage                   | 83.0 ms                                                      | 78.9 ms: 1.05x faster                                                  |
| thrift                     | 778 us                                                       | 741 us: 1.05x faster                                                   |
| pyflate                    | 449 ms                                                       | 427 ms: 1.05x faster                                                   |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 702 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.3 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.25 sec: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.7 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                 |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                   |
| json                       | 4.93 ms                                                      | 4.78 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 83.3 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.9 ms: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.68 us: 1.02x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.86 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.03 us: 1.02x faster                                                  |
| richards_super             | 51.6 ms                                                      | 50.6 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 51.7 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.7 ms: 1.02x faster                                                  |
| richards                   | 45.2 ms                                                      | 44.5 ms: 1.02x faster                                                  |
| fannkuch                   | 370 ms                                                       | 364 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.3 ms: 1.01x faster                                                  |
| sympy_expand               | 457 ms                                                       | 454 ms: 1.01x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.00x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 78.9 ms: 1.00x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.1 ms: 1.01x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.57 ms: 1.01x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.26 ms: 1.01x slower                                                  |
| chaos                      | 57.3 ms                                                      | 57.8 ms: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.17 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                   |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| logging_silent             | 103 ns                                                       | 105 ns: 1.02x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.44 sec: 1.04x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.1 us: 1.04x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 319 us: 1.08x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.39x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.45 ms: 1.42x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 89.6 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (5): float, regex_dna, sympy_integrate, pycparser, dulwich_log
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241216-3.14.0a2+-cfeaa99/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2+-cfeaa99.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x