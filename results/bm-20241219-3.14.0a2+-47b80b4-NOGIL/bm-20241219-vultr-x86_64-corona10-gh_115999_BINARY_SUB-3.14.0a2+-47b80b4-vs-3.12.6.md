# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 47b80b4
- commit date: 2024-12-19
- overall geometric mean: 1.221x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| html5lib       | 63.6 ms                                                | 98.8 ms: 1.55x slower                                                    |
| Geometric mean | (ref)                                                  | 1.36x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 823 ms: 1.35x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 852 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 443 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 472 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                                     |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                    |
| async_generators           | 384 ms                                                 | 452 ms: 1.18x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                     |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                     |
| float          | 80.8 ms                                                | 140 ms: 1.73x slower                                                     |
| Geometric mean | (ref)                                                  | 1.37x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| regex_compile  | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| Geometric mean | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 77.4 ms: 1.31x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 335 us: 1.52x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 511 us: 1.66x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.3 ms: 1.26x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                    |
| django_template | 34.7 ms                                                | 51.4 ms: 1.48x slower                                                    |
| mako            | 11.0 ms                                                | 17.7 ms: 1.61x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.43x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 823 ms: 1.35x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 852 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 443 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 358 ms: 1.25x faster                                                     |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 472 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| gc_traversal               | 3.46 ms                                                | 3.17 ms: 1.09x faster                                                    |
| deepcopy                   | 352 us                                                 | 327 us: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| pathlib                    | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 39.5 us: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                     |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.6 ms: 1.03x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.29 us: 1.04x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.00 sec: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                    |
| spectral_norm              | 110 ms                                                 | 120 ms: 1.09x slower                                                     |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.48 us: 1.13x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.84 sec: 1.17x slower                                                   |
| async_generators           | 384 ms                                                 | 452 ms: 1.18x slower                                                     |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                     |
| generators                 | 32.2 ms                                                | 38.1 ms: 1.18x slower                                                    |
| pylint                     | 319 ms                                                 | 381 ms: 1.20x slower                                                     |
| nqueens                    | 80.1 ms                                                | 96.0 ms: 1.20x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 92.1 ms: 1.20x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 95.5 ms: 1.21x slower                                                    |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                     |
| regex_compile              | 142 ms                                                 | 179 ms: 1.25x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 63.3 ms: 1.26x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.66 sec: 1.26x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 135 ms: 1.27x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 68.8 ms: 1.29x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 970 ms: 1.31x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 77.4 ms: 1.31x slower                                                    |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                     |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.02 sec: 1.33x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.93 ms: 1.35x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.7 ms: 1.36x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 156 ms: 1.37x slower                                                     |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                    |
| coverage                   | 71.4 ms                                                | 99.1 ms: 1.39x slower                                                    |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| genshi_text                | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 203 ms: 1.42x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                    |
| thrift                     | 791 us                                                 | 1.15 ms: 1.45x slower                                                    |
| django_template            | 34.7 ms                                                | 51.4 ms: 1.48x slower                                                    |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 335 us: 1.52x slower                                                     |
| pyflate                    | 448 ms                                                 | 691 ms: 1.54x slower                                                     |
| html5lib                   | 63.6 ms                                                | 98.8 ms: 1.55x slower                                                    |
| hexiom                     | 6.17 ms                                                | 9.72 ms: 1.58x slower                                                    |
| logging_simple             | 6.63 us                                                | 10.6 us: 1.60x slower                                                    |
| logging_format             | 7.35 us                                                | 11.8 us: 1.60x slower                                                    |
| mako                       | 11.0 ms                                                | 17.7 ms: 1.61x slower                                                    |
| sympy_str                  | 292 ms                                                 | 476 ms: 1.63x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 511 us: 1.66x slower                                                     |
| chaos                      | 62.8 ms                                                | 105 ms: 1.67x slower                                                     |
| richards                   | 45.9 ms                                                | 76.9 ms: 1.67x slower                                                    |
| richards_super             | 51.9 ms                                                | 86.9 ms: 1.68x slower                                                    |
| logging_silent             | 109 ns                                                 | 184 ns: 1.69x slower                                                     |
| scimark_sor                | 130 ms                                                 | 221 ms: 1.70x slower                                                     |
| float                      | 80.8 ms                                                | 140 ms: 1.73x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.76x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 2.97 ms: 1.78x slower                                                    |
| raytrace                   | 299 ms                                                 | 547 ms: 1.83x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.57 ms: 1.90x slower                                                    |
| go                         | 139 ms                                                 | 271 ms: 1.94x slower                                                     |
| sympy_expand               | 468 ms                                                 | 953 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                     |
| deltablue                  | 3.45 ms                                                | 7.98 ms: 2.32x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.64x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241219-3.14.0a2+-47b80b4-NOGIL/bm-20241219-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-47b80b4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.221x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x