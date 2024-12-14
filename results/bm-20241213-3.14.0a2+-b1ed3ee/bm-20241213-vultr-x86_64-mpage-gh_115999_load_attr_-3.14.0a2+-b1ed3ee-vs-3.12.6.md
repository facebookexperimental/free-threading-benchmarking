# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: b1ed3ee
- commit date: 2024-12-13
- overall geometric mean: 1.091x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.0 ms: 1.06x faster                                                 |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| json_loads           | 26.5 us                                                | 25.9 us: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 315 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                 |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 303 ms: 1.85x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 603 ms: 1.84x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 479 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 496 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 249 us: 1.41x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 115 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                 |
| generators                 | 32.2 ms                                                | 27.3 ms: 1.18x faster                                                 |
| raytrace                   | 299 ms                                                 | 257 ms: 1.17x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.1 us: 1.16x faster                                                 |
| spectral_norm              | 110 ms                                                 | 94.9 ms: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.4 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                                 |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                  |
| thrift                     | 791 us                                                 | 723 us: 1.09x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.15 ms: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| chaos                      | 62.8 ms                                                | 57.6 ms: 1.09x faster                                                 |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.09x faster                                                 |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 62.9 ms: 1.09x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.79 ms: 1.07x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.23 us: 1.06x faster                                                 |
| float                      | 80.8 ms                                                | 76.0 ms: 1.06x faster                                                 |
| json                       | 5.02 ms                                                | 4.74 ms: 1.06x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                |
| richards                   | 45.9 ms                                                | 43.5 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 704 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.5 ms: 1.05x faster                                                 |
| pyflate                    | 448 ms                                                 | 426 ms: 1.05x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.05x faster                                                  |
| logging_format             | 7.35 us                                                | 7.00 us: 1.05x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.2 ms: 1.05x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.5 ms: 1.05x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.31 sec: 1.04x faster                                                |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 52.0 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.9 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.30 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.01x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 49.5 ms: 1.01x faster                                                 |
| nqueens                    | 80.1 ms                                                | 79.1 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 315 us: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                 |
| telco                      | 6.53 ms                                                | 7.17 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.41 ms: 1.28x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.4 ms: 8.19x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): nbody
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-b1ed3ee.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x