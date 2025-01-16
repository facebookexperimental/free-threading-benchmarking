# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.053x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                                  |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                |
| html5lib       | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 500 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.2 ms: 1.05x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| regex_compile  | 142 ms                                                 | 149 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.1 ms: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.31 sec: 1.10x slower                                                |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                 |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                 |
| django_template | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 348 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 500 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.1 ms: 1.12x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                 |
| float                      | 80.8 ms                                                | 77.2 ms: 1.05x faster                                                 |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| generators                 | 32.2 ms                                                | 31.0 ms: 1.04x faster                                                 |
| go                         | 139 ms                                                 | 136 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                  |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.04x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| regex_compile              | 142 ms                                                 | 149 ms: 1.05x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.9 us: 1.05x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.27 us: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.08x slower                                                |
| pyflate                    | 448 ms                                                 | 483 ms: 1.08x slower                                                  |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.31 sec: 1.10x slower                                                |
| html5lib                   | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                                  |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                 |
| scimark_fft                | 342 ms                                                 | 381 ms: 1.11x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 829 ms: 1.12x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.40 us: 1.12x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                |
| chaos                      | 62.8 ms                                                | 70.6 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.9 ms: 1.14x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                  |
| logging_format             | 7.35 us                                                | 8.43 us: 1.15x slower                                                 |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                  |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.8 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                 |
| thrift                     | 791 us                                                 | 920 us: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.26 ms: 1.18x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.2 ms: 1.20x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                  |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                                 |
| nqueens                    | 80.1 ms                                                | 96.8 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.2 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                  |
| django_template            | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| fannkuch                   | 372 ms                                                 | 475 ms: 1.28x slower                                                  |
| telco                      | 6.53 ms                                                | 8.53 ms: 1.31x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.57 ms: 1.33x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.84 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.55 ms: 1.33x slower                                                 |
| coverage                   | 71.4 ms                                                | 96.9 ms: 1.36x slower                                                 |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.3 ms: 8.73x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250115-3.14.0a4+-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.053x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x