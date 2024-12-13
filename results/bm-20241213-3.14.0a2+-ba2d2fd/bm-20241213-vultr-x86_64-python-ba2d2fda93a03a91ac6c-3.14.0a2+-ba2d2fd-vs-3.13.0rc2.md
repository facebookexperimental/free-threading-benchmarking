# Results vs. 3.13.0rc2

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.042x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 624 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 333 ms: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                   |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.4 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| nbody          | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.10x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.51x faster                                                   |
| async_tree_io              | 876 ms                                                       | 624 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 333 ms: 1.38x faster                                                   |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 482 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.7 us: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.29x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.60 us: 1.20x faster                                                  |
| go                         | 141 ms                                                       | 118 ms: 1.20x faster                                                   |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.4 ms: 1.10x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.82 ms: 1.10x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.26 ms: 1.08x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.1 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 699 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.1 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                 |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                                   |
| coverage                   | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                                 |
| scimark_fft                | 349 ms                                                       | 335 ms: 1.04x faster                                                   |
| json                       | 4.93 ms                                                      | 4.74 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.53 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 750 us: 1.04x faster                                                   |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.61 us: 1.03x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.95 us: 1.03x faster                                                  |
| json_loads                 | 27.0 us                                                      | 26.2 us: 1.03x faster                                                  |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.81 ms: 1.03x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.6 ms: 1.03x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 151 ms: 1.03x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.7 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.02x faster                                                   |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.9 ms: 1.02x faster                                                  |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.2 ms: 1.01x faster                                                  |
| pyflate                    | 449 ms                                                       | 445 ms: 1.01x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 52.4 ms: 1.01x faster                                                  |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                   |
| sympy_expand               | 457 ms                                                       | 455 ms: 1.00x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.00x faster                                                 |
| richards_super             | 51.6 ms                                                      | 51.4 ms: 1.00x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                   |
| richards                   | 45.2 ms                                                      | 45.4 ms: 1.00x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.22 us: 1.01x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.4 ms: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.16 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                  |
| chaos                      | 57.3 ms                                                      | 58.5 ms: 1.02x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.0 ms: 1.03x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.06 sec: 1.03x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.0 ms: 1.03x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.0 us: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                                   |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.47 sec: 1.05x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.2 ms: 1.07x slower                                                  |
| nbody                      | 85.1 ms                                                      | 91.1 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 88.8 ms: 8.08x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (4): fannkuch, genshi_text, typing_runtime_protocols, float
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.042x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x