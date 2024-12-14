# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 316 ms: 1.22x slower                                                 |
| docutils       | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                               |
| html5lib       | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                        | 1.13x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 588 ms: 1.55x faster                                                 |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 519 ms: 1.28x faster                                                 |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                |
| async_generators           | 377 ms                                                       | 413 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                 |
| float          | 77.5 ms                                                      | 79.1 ms: 1.02x slower                                                |
| nbody          | 85.1 ms                                                      | 129 ms: 1.52x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                |
| unpickle_pure_python | 210 us                                                       | 239 us: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 67.5 ms: 1.14x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                               |
| pickle_pure_python   | 294 us                                                       | 357 us: 1.21x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| python_startup         | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                                |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.7 ms: 1.22x slower                                                |
| django_template | 34.1 ms                                                      | 43.3 ms: 1.27x slower                                                |
| genshi_text     | 21.5 ms                                                      | 27.7 ms: 1.29x slower                                                |
| mako            | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 588 ms: 1.55x faster                                                 |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 346 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 519 ms: 1.28x faster                                                 |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                                 |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                 |
| deepcopy                   | 355 us                                                       | 309 us: 1.15x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                |
| go                         | 141 ms                                                       | 134 ms: 1.05x faster                                                 |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.01x faster                                                 |
| float                      | 77.5 ms                                                      | 79.1 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.24 us: 1.04x slower                                                |
| json_loads                 | 27.0 us                                                      | 28.2 us: 1.04x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                |
| scimark_fft                | 349 ms                                                       | 369 ms: 1.06x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.5 ms: 1.06x slower                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                               |
| pyflate                    | 449 ms                                                       | 481 ms: 1.07x slower                                                 |
| pylint                     | 317 ms                                                       | 341 ms: 1.08x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                               |
| dulwich_log                | 74.8 ms                                                      | 81.0 ms: 1.08x slower                                                |
| telco                      | 7.82 ms                                                      | 8.51 ms: 1.09x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.09x slower                                               |
| async_generators           | 377 ms                                                       | 413 ms: 1.10x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.58 sec: 1.10x slower                                               |
| scimark_sor                | 134 ms                                                       | 148 ms: 1.10x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 239 us: 1.14x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 67.5 ms: 1.14x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.38 ms: 1.14x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 844 ms: 1.14x slower                                                 |
| logging_silent             | 103 ns                                                       | 118 ns: 1.15x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                |
| tomli_loads                | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                               |
| pprint_pformat             | 1.50 sec                                                     | 1.74 sec: 1.16x slower                                               |
| thrift                     | 778 us                                                       | 906 us: 1.16x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.30 us: 1.19x slower                                                |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                |
| chaos                      | 57.3 ms                                                      | 69.0 ms: 1.20x slower                                                |
| pickle_pure_python         | 294 us                                                       | 357 us: 1.21x slower                                                 |
| 2to3                       | 260 ms                                                       | 316 ms: 1.22x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 95.7 ms: 1.22x slower                                                |
| genshi_xml                 | 48.8 ms                                                      | 59.7 ms: 1.22x slower                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.0 ms: 1.22x slower                                                |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.22x slower                                                |
| logging_format             | 6.84 us                                                      | 8.38 us: 1.22x slower                                                |
| richards                   | 45.2 ms                                                      | 55.7 ms: 1.23x slower                                                |
| hexiom                     | 5.99 ms                                                      | 7.41 ms: 1.24x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                |
| comprehensions             | 16.5 us                                                      | 20.4 us: 1.24x slower                                                |
| raytrace                   | 253 ms                                                       | 315 ms: 1.25x slower                                                 |
| richards_super             | 51.6 ms                                                      | 64.5 ms: 1.25x slower                                                |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.27x slower                                                |
| django_template            | 34.1 ms                                                      | 43.3 ms: 1.27x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 86.4 ms: 1.27x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 198 us: 1.28x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 27.7 ms: 1.29x slower                                                |
| fannkuch                   | 370 ms                                                       | 479 ms: 1.30x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| sympy_integrate            | 19.8 ms                                                      | 28.3 ms: 1.43x slower                                                |
| deltablue                  | 3.12 ms                                                      | 4.62 ms: 1.48x slower                                                |
| scimark_lu                 | 113 ms                                                       | 167 ms: 1.48x slower                                                 |
| nbody                      | 85.1 ms                                                      | 129 ms: 1.52x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                                |
| sympy_str                  | 275 ms                                                       | 455 ms: 1.66x slower                                                 |
| sympy_expand               | 457 ms                                                       | 924 ms: 2.02x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 339 ms: 2.18x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 105 ms: 9.59x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.33x