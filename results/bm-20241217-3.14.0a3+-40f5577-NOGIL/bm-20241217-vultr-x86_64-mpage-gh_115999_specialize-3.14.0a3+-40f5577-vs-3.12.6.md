# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 40f5577
- commit date: 2024-12-17
- overall geometric mean: 1.189x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 360 ms: 1.37x slower                                                  |
| docutils       | 2.64 sec                                               | 3.06 sec: 1.16x slower                                                |
| html5lib       | 63.6 ms                                                | 94.1 ms: 1.48x slower                                                 |
| Geometric mean | (ref)                                                  | 1.33x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 732 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 405 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 323 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 356 ms: 1.30x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 579 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 600 ms: 1.19x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                 | 448 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 111 ms: 1.37x slower                                                  |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                  |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                  |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 73.9 ms: 1.25x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 327 us: 1.48x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 504 us: 1.64x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.6 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.0 ms: 1.32x slower                                                 |
| django_template | 34.7 ms                                                | 50.0 ms: 1.44x slower                                                 |
| mako            | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 732 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 405 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 323 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 356 ms: 1.30x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 579 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 600 ms: 1.19x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.98 ms: 1.06x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.28 ms: 1.06x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.16 us: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 39.8 us: 1.01x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                 |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.96 sec: 1.05x slower                                                |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 372 ms: 1.09x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.42 us: 1.11x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.69 sec: 1.11x slower                                                |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                 |
| pylint                     | 319 ms                                                 | 365 ms: 1.15x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 91.2 ms: 1.16x slower                                                 |
| docutils                   | 2.64 sec                                               | 3.06 sec: 1.16x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 89.0 ms: 1.16x slower                                                 |
| async_generators           | 384 ms                                                 | 448 ms: 1.17x slower                                                  |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                  |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.40 sec: 1.20x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                |
| regex_v8                   | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                 |
| nqueens                    | 80.1 ms                                                | 98.2 ms: 1.23x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.42 ms: 1.23x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 65.8 ms: 1.23x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.24x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 62.6 ms: 1.25x slower                                                 |
| thrift                     | 791 us                                                 | 987 us: 1.25x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 73.9 ms: 1.25x slower                                                 |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.28x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.8 ms: 1.28x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 961 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 486 ms: 1.31x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.32x slower                                                |
| genshi_text                | 22.8 ms                                                | 30.0 ms: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.65 ms: 1.33x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| 2to3                       | 264 ms                                                 | 360 ms: 1.37x slower                                                  |
| logging_simple             | 6.63 us                                                | 9.08 us: 1.37x slower                                                 |
| float                      | 80.8 ms                                                | 111 ms: 1.37x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 197 ms: 1.38x slower                                                  |
| logging_format             | 7.35 us                                                | 10.2 us: 1.39x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                 |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 100 ms: 1.40x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                 |
| django_template            | 34.7 ms                                                | 50.0 ms: 1.44x slower                                                 |
| pyflate                    | 448 ms                                                 | 650 ms: 1.45x slower                                                  |
| html5lib                   | 63.6 ms                                                | 94.1 ms: 1.48x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 327 us: 1.48x slower                                                  |
| richards_super             | 51.9 ms                                                | 77.5 ms: 1.49x slower                                                 |
| richards                   | 45.9 ms                                                | 68.9 ms: 1.50x slower                                                 |
| chaos                      | 62.8 ms                                                | 95.1 ms: 1.51x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 105 ms: 1.54x slower                                                  |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                 |
| hexiom                     | 6.17 ms                                                | 9.72 ms: 1.57x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 183 ms: 1.60x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.70 ms: 1.62x slower                                                 |
| sympy_str                  | 292 ms                                                 | 475 ms: 1.63x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 504 us: 1.64x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                 |
| raytrace                   | 299 ms                                                 | 498 ms: 1.66x slower                                                  |
| logging_silent             | 109 ns                                                 | 185 ns: 1.69x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 2.34 ms: 1.73x slower                                                 |
| go                         | 139 ms                                                 | 243 ms: 1.75x slower                                                  |
| scimark_sor                | 130 ms                                                 | 231 ms: 1.78x slower                                                  |
| sympy_expand               | 468 ms                                                 | 956 ms: 2.04x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 347 ms: 2.09x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.60 ms: 2.20x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 107 ms: 9.91x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.28x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a3+-40f5577-NOGIL/bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.189x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x