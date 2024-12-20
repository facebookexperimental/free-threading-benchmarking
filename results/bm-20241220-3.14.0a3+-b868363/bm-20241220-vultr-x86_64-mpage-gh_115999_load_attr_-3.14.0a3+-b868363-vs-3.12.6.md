# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b868363
- commit date: 2024-12-20
- overall geometric mean: 1.094x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 605 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 328 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.0 ms: 1.14x faster                                                 |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.6 ms: 1.08x faster                                                 |
| nbody          | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                 |
| pidigits       | 184 ms                                                 | 222 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| json_loads           | 26.5 us                                                | 25.8 us: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.5 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 605 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 328 ms: 1.69x faster                                                  |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.1 us: 1.38x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 576 ms: 1.26x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.55 us: 1.21x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.0 ms: 1.16x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| raytrace                   | 299 ms                                                 | 259 ms: 1.16x faster                                                  |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.2 us: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.7 ms: 1.15x faster                                                 |
| coroutines                 | 23.9 ms                                                | 21.0 ms: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                  |
| scimark_fft                | 342 ms                                                 | 306 ms: 1.11x faster                                                  |
| logging_format             | 7.35 us                                                | 6.61 us: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.2 ms: 1.10x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.02 us: 1.10x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.13 ms: 1.10x faster                                                 |
| chaos                      | 62.8 ms                                                | 57.4 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| async_generators           | 384 ms                                                 | 353 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.09x faster                                                 |
| float                      | 80.8 ms                                                | 74.6 ms: 1.08x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                 |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                  |
| richards                   | 45.9 ms                                                | 42.7 ms: 1.08x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 690 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 735 us: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| pyflate                    | 448 ms                                                 | 419 ms: 1.07x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.78 ms: 1.07x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.8 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                |
| json                       | 5.02 ms                                                | 4.76 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.0 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 102 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.23 ms: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.5 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 51.7 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.8 us: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.9 ms: 1.03x faster                                                 |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 368 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.01x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.44 sec: 1.01x slower                                                |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                 |
| telco                      | 6.53 ms                                                | 7.21 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.1 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                 |
| pidigits                   | 184 ms                                                 | 222 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.30 ms: 1.24x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.4 ms: 8.19x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-b868363/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-b868363.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x