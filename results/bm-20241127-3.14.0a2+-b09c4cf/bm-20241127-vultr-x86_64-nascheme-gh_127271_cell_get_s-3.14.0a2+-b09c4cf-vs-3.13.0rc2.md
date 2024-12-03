# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127271_cell_get_s
- machine: linux-x86_64
- commit hash: b09c4cf
- commit date: 2024-11-27
- overall geometric mean: 1.002x slower
- HPT reliability: 94.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 410 ms: 1.13x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                    |
| async_tree_none            | 354 ms                                                       | 333 ms: 1.06x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 883 ms: 1.03x faster                                                     |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                             |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 226 ms: 1.04x slower                                                     |
| float          | 77.5 ms                                                      | 81.4 ms: 1.05x slower                                                    |
| nbody          | 85.1 ms                                                      | 95.9 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                        | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                     |
| regex_compile  | 132 ms                                                       | 135 ms: 1.02x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 86.4 ms: 1.01x slower                                                    |
| xml_etree_parse      | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.5 ms: 1.04x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 315 us: 1.07x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                        | 1.15x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deepcopy                   | 355 us                                                       | 260 us: 1.37x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.3 us: 1.29x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                    |
| pylint                     | 317 ms                                                       | 269 ms: 1.18x faster                                                     |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 410 ms: 1.13x faster                                                     |
| json                       | 4.93 ms                                                      | 4.50 ms: 1.10x faster                                                    |
| json_loads                 | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                    |
| telco                      | 7.82 ms                                                      | 7.28 ms: 1.07x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.43 ms: 1.06x faster                                                    |
| async_tree_none            | 354 ms                                                       | 333 ms: 1.06x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                    |
| thrift                     | 778 us                                                       | 746 us: 1.04x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 883 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 716 ms: 1.03x faster                                                     |
| scimark_fft                | 349 ms                                                       | 340 ms: 1.03x faster                                                     |
| meteor_contest             | 102 ms                                                       | 99.4 ms: 1.02x faster                                                    |
| coverage                   | 83.0 ms                                                      | 81.4 ms: 1.02x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                     |
| hexiom                     | 5.99 ms                                                      | 5.95 ms: 1.01x faster                                                    |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                     |
| mdp                        | 2.36 sec                                                     | 2.35 sec: 1.00x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.46 sec: 1.00x slower                                                   |
| sympy_expand               | 457 ms                                                       | 459 ms: 1.00x slower                                                     |
| pyflate                    | 449 ms                                                       | 451 ms: 1.00x slower                                                     |
| scimark_sor                | 134 ms                                                       | 135 ms: 1.01x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 79.2 ms: 1.01x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 66.0 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 86.4 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.7 ms: 1.01x slower                                                    |
| xml_etree_parse            | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| logging_format             | 6.84 us                                                      | 6.94 us: 1.01x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 107 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 53.9 ms: 1.02x slower                                                    |
| generators                 | 28.8 ms                                                      | 29.5 ms: 1.02x slower                                                    |
| regex_compile              | 132 ms                                                       | 135 ms: 1.02x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                    |
| richards                   | 45.2 ms                                                      | 46.4 ms: 1.03x slower                                                    |
| chaos                      | 57.3 ms                                                      | 58.8 ms: 1.03x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                                    |
| richards_super             | 51.6 ms                                                      | 53.5 ms: 1.04x slower                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 98.5 ms: 1.04x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 664 ms: 1.04x slower                                                     |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                     |
| pidigits                   | 217 ms                                                       | 226 ms: 1.04x slower                                                     |
| fannkuch                   | 370 ms                                                       | 386 ms: 1.04x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.26 ms: 1.04x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                     |
| float                      | 77.5 ms                                                      | 81.4 ms: 1.05x slower                                                    |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 315 us: 1.07x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                    |
| nbody                      | 85.1 ms                                                      | 95.9 ms: 1.13x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.74 ms: 1.19x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 85.8 ms: 7.80x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (9): async_tree_io, sympy_str, docutils, crypto_pyaes, python_startup_no_site, logging_simple, scimark_lu, async_tree_cpu_io_mixed, async_tree_none_tg
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241127-3.14.0a2+-b09c4cf/bm-20241127-vultr-x86_64-nascheme-gh_127271_cell_get_s-3.14.0a2+-b09c4cf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 94.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x