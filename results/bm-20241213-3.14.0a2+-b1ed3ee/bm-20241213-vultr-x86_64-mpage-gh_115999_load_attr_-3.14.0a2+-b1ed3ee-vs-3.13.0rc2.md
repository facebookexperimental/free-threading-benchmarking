# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.053x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 330 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 479 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.28x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                 |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 76.0 ms: 1.02x faster                                                 |
| nbody          | 85.1 ms                                                      | 88.8 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 315 us: 1.07x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                 |
| genshi_xml      | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| django_template | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 603 ms: 1.51x faster                                                  |
| deepcopy                   | 355 us                                                       | 249 us: 1.43x faster                                                  |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.42x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 330 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.0 us: 1.35x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 496 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 479 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 275 ms: 1.28x faster                                                  |
| go                         | 141 ms                                                       | 115 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.22x faster                                                 |
| spectral_norm              | 111 ms                                                       | 94.9 ms: 1.17x faster                                                 |
| pidigits                   | 217 ms                                                       | 186 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| scimark_sor                | 134 ms                                                       | 119 ms: 1.13x faster                                                  |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.30 ms: 1.10x faster                                                 |
| telco                      | 7.82 ms                                                      | 7.17 ms: 1.09x faster                                                 |
| thrift                     | 778 us                                                       | 723 us: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.9 ms: 1.08x faster                                                 |
| async_generators           | 377 ms                                                       | 354 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.3 ms: 1.05x faster                                                 |
| coverage                   | 83.0 ms                                                      | 78.8 ms: 1.05x faster                                                 |
| pyflate                    | 449 ms                                                       | 426 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 704 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.6 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.26 sec: 1.04x faster                                                |
| richards_super             | 51.6 ms                                                      | 49.5 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                                |
| json_loads                 | 27.0 us                                                      | 25.9 us: 1.04x faster                                                 |
| richards                   | 45.2 ms                                                      | 43.5 ms: 1.04x faster                                                 |
| json                       | 4.93 ms                                                      | 4.74 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.9 ms: 1.04x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.79 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.5 ms: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.2 ms: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.02x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.4 ms: 1.02x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                                  |
| float                      | 77.5 ms                                                      | 76.0 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 270 ms: 1.02x faster                                                  |
| mdp                        | 2.36 sec                                                     | 2.31 sec: 1.02x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 52.0 ms: 1.01x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 21.4 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                  |
| chaos                      | 57.3 ms                                                      | 57.6 ms: 1.00x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.2 ms: 1.00x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 79.1 ms: 1.01x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.15 ms: 1.01x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.23 us: 1.01x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                 |
| raytrace                   | 253 ms                                                       | 257 ms: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.00 us: 1.02x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.1 us: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 88.8 ms: 1.04x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.6 ms: 1.04x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 315 us: 1.07x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.4 ms: 8.04x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (7): sqlglot_transpile, sympy_expand, sqlglot_parse, sympy_integrate, pycparser, fannkuch, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.053x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x