# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.076x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 316 ms: 1.20x slower                                                 |
| docutils       | 2.64 sec                                               | 2.83 sec: 1.07x slower                                               |
| html5lib       | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                |
| Geometric mean | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 588 ms: 1.89x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                 |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 519 ms: 1.38x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| async_generators           | 384 ms                                                 | 413 ms: 1.07x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                 |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                                 |
| Geometric mean | (ref)                                                  | 1.12x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                 |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                                 |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                |
| Geometric mean | (ref)                                                  | 1.03x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 67.5 ms: 1.15x slower                                                |
| pickle_pure_python   | 308 us                                                 | 357 us: 1.16x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 17.0 ms: 1.72x slower                                                |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 588 ms: 1.89x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 600 ms: 1.80x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                 |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 519 ms: 1.38x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                |
| deepcopy                   | 352 us                                                 | 309 us: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 30.5 ms: 1.06x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                |
| go                         | 139 ms                                                 | 134 ms: 1.04x faster                                                 |
| float                      | 80.8 ms                                                | 79.1 ms: 1.02x faster                                                |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                 |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 81.0 ms: 1.03x slower                                                |
| comprehensions             | 19.8 us                                                | 20.4 us: 1.03x slower                                                |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.04x slower                                               |
| deepcopy_reduce            | 3.08 us                                                | 3.24 us: 1.05x slower                                                |
| raytrace                   | 299 ms                                                 | 315 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                |
| mdp                        | 2.42 sec                                               | 2.58 sec: 1.07x slower                                               |
| pylint                     | 319 ms                                                 | 341 ms: 1.07x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.83 sec: 1.07x slower                                               |
| pyflate                    | 448 ms                                                 | 481 ms: 1.07x slower                                                 |
| async_generators           | 384 ms                                                 | 413 ms: 1.07x slower                                                 |
| logging_silent             | 109 ns                                                 | 118 ns: 1.08x slower                                                 |
| scimark_fft                | 342 ms                                                 | 369 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                 |
| chaos                      | 62.8 ms                                                | 69.0 ms: 1.10x slower                                                |
| logging_simple             | 6.63 us                                                | 7.30 us: 1.10x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                               |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.3 ms: 1.11x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 86.4 ms: 1.13x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 844 ms: 1.14x slower                                                 |
| scimark_sor                | 130 ms                                                 | 148 ms: 1.14x slower                                                 |
| logging_format             | 7.35 us                                                | 8.38 us: 1.14x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                                |
| thrift                     | 791 us                                                 | 906 us: 1.15x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 67.5 ms: 1.15x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.15x slower                                               |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                |
| html5lib                   | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                |
| pickle_pure_python         | 308 us                                                 | 357 us: 1.16x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 80.0 ms: 1.17x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                |
| nqueens                    | 80.1 ms                                                | 95.7 ms: 1.20x slower                                                |
| 2to3                       | 264 ms                                                 | 316 ms: 1.20x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.41 ms: 1.20x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                 |
| richards                   | 45.9 ms                                                | 55.7 ms: 1.21x slower                                                |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.38 ms: 1.22x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 176 ms: 1.24x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.5 ms: 1.24x slower                                                |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                |
| fannkuch                   | 372 ms                                                 | 479 ms: 1.29x slower                                                 |
| telco                      | 6.53 ms                                                | 8.51 ms: 1.30x slower                                                |
| deltablue                  | 3.45 ms                                                | 4.62 ms: 1.34x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 28.3 ms: 1.38x slower                                                |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 167 ms: 1.46x slower                                                 |
| sympy_str                  | 292 ms                                                 | 455 ms: 1.56x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                |
| python_startup             | 9.93 ms                                                | 17.0 ms: 1.72x slower                                                |
| sympy_expand               | 468 ms                                                 | 924 ms: 1.98x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 339 ms: 2.04x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 105 ms: 9.76x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                         |

Benchmark hidden because not significant (1): bpe_tokeniser
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x