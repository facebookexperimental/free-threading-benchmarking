# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 73aa5a2
- commit date: 2025-01-15
- overall geometric mean: 1.058x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                  |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.07x slower                                                |
| html5lib       | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                                  |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                 |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                 |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 371 us: 1.21x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| django_template | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 86.7 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                 |
| generators                 | 32.2 ms                                                | 30.9 ms: 1.04x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                  |
| go                         | 139 ms                                                 | 138 ms: 1.01x faster                                                  |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                                |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                  |
| json                       | 5.02 ms                                                | 5.32 ms: 1.06x slower                                                 |
| spectral_norm              | 110 ms                                                 | 117 ms: 1.06x slower                                                  |
| logging_silent             | 109 ns                                                 | 116 ns: 1.06x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.68 ms: 1.06x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.07x slower                                                |
| comprehensions             | 19.8 us                                                | 21.2 us: 1.07x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.30 us: 1.07x slower                                                 |
| html5lib                   | 63.6 ms                                                | 68.8 ms: 1.08x slower                                                 |
| pyflate                    | 448 ms                                                 | 486 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.28 us: 1.10x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 822 ms: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                |
| logging_format             | 7.35 us                                                | 8.28 us: 1.13x slower                                                 |
| chaos                      | 62.8 ms                                                | 71.0 ms: 1.13x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                  |
| scimark_fft                | 342 ms                                                 | 387 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                 |
| thrift                     | 791 us                                                 | 905 us: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.6 ms: 1.14x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                  |
| sympy_str                  | 292 ms                                                 | 338 ms: 1.16x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 62.2 ms: 1.17x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                                 |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.6 ms: 1.18x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 24.4 ms: 1.19x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.3 ms: 1.20x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 371 us: 1.21x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.32 ms: 1.21x slower                                                 |
| richards                   | 45.9 ms                                                | 55.6 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.3 ms: 1.22x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.55 ms: 1.22x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 140 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                                  |
| genshi_text                | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| django_template            | 34.7 ms                                                | 43.6 ms: 1.26x slower                                                 |
| richards_super             | 51.9 ms                                                | 66.3 ms: 1.28x slower                                                 |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.28x slower                                                  |
| fannkuch                   | 372 ms                                                 | 479 ms: 1.29x slower                                                  |
| telco                      | 6.53 ms                                                | 8.42 ms: 1.29x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.66 ms: 1.35x slower                                                 |
| coverage                   | 71.4 ms                                                | 97.6 ms: 1.37x slower                                                 |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                 |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.54x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.2 ms: 8.73x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (4): coroutines, bpe_tokeniser, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250115-3.14.0a4+-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x