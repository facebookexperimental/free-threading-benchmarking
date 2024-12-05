# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: de73a27
- commit date: 2024-12-04
- overall geometric mean: 1.223x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 365 ms: 1.39x slower                                                  |
| docutils       | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                |
| html5lib       | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                  | 1.36x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 798 ms: 1.39x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 818 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 437 ms: 1.28x faster                                                  |
| async_tree_none            | 464 ms                                                 | 379 ms: 1.22x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 602 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.8 ms: 1.08x slower                                                 |
| async_generators           | 384 ms                                                 | 454 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.15x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                  |
| float          | 80.8 ms                                                | 142 ms: 1.76x slower                                                  |
| Geometric mean | (ref)                                                  | 1.38x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| regex_compile  | 142 ms                                                 | 181 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.0 ms: 1.05x faster                                                 |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 98.2 ms: 1.15x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.68 sec: 1.27x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 78.6 ms: 1.33x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 338 us: 1.53x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 513 us: 1.67x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                 |
| django_template | 34.7 ms                                                | 50.6 ms: 1.46x slower                                                 |
| mako            | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.40x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 798 ms: 1.39x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 818 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 437 ms: 1.28x faster                                                  |
| async_tree_none            | 464 ms                                                 | 379 ms: 1.22x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 459 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 602 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 626 ms: 1.14x faster                                                  |
| deepcopy                   | 352 us                                                 | 323 us: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.0 ms: 1.05x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.31 ms: 1.05x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 40.0 us: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                 | 183 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.99 sec: 1.05x slower                                                |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.8 ms: 1.08x slower                                                 |
| spectral_norm              | 110 ms                                                 | 122 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.41 us: 1.11x slower                                                 |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 98.2 ms: 1.15x slower                                                 |
| scimark_fft                | 342 ms                                                 | 394 ms: 1.15x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                |
| docutils                   | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                |
| pylint                     | 319 ms                                                 | 372 ms: 1.17x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 89.7 ms: 1.17x slower                                                 |
| async_generators           | 384 ms                                                 | 454 ms: 1.18x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 95.0 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.23x slower                                                 |
| generators                 | 32.2 ms                                                | 39.6 ms: 1.23x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 67.3 ms: 1.26x slower                                                 |
| regex_compile              | 142 ms                                                 | 181 ms: 1.27x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.68 sec: 1.27x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 136 ms: 1.28x slower                                                  |
| meteor_contest             | 104 ms                                                 | 134 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.69 ms: 1.29x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.52 sec: 1.30x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 973 ms: 1.31x slower                                                  |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.9 ms: 1.33x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 2.02 sec: 1.33x slower                                                |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                                 |
| genshi_text                | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 78.6 ms: 1.33x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                 |
| 2to3                       | 264 ms                                                 | 365 ms: 1.39x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 201 ms: 1.41x slower                                                  |
| thrift                     | 791 us                                                 | 1.12 ms: 1.42x slower                                                 |
| comprehensions             | 19.8 us                                                | 28.1 us: 1.42x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 29.6 ms: 1.44x slower                                                 |
| django_template            | 34.7 ms                                                | 50.6 ms: 1.46x slower                                                 |
| coverage                   | 71.4 ms                                                | 104 ms: 1.46x slower                                                  |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                  |
| logging_format             | 7.35 us                                                | 11.1 us: 1.51x slower                                                 |
| logging_simple             | 6.63 us                                                | 10.1 us: 1.52x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 338 us: 1.53x slower                                                  |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.55x slower                                                 |
| html5lib                   | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                 |
| pyflate                    | 448 ms                                                 | 703 ms: 1.57x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 184 ms: 1.61x slower                                                  |
| hexiom                     | 6.17 ms                                                | 10.0 ms: 1.62x slower                                                 |
| sympy_str                  | 292 ms                                                 | 479 ms: 1.64x slower                                                  |
| chaos                      | 62.8 ms                                                | 104 ms: 1.66x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 513 us: 1.67x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                                 |
| richards_super             | 51.9 ms                                                | 89.5 ms: 1.73x slower                                                 |
| richards                   | 45.9 ms                                                | 79.4 ms: 1.73x slower                                                 |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.73x slower                                                 |
| logging_silent             | 109 ns                                                 | 190 ns: 1.74x slower                                                  |
| float                      | 80.8 ms                                                | 142 ms: 1.76x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 121 ms: 1.76x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.02 ms: 1.80x slower                                                 |
| scimark_sor                | 130 ms                                                 | 237 ms: 1.82x slower                                                  |
| raytrace                   | 299 ms                                                 | 559 ms: 1.87x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.62 ms: 1.93x slower                                                 |
| go                         | 139 ms                                                 | 275 ms: 1.97x slower                                                  |
| sympy_expand               | 468 ms                                                 | 961 ms: 2.06x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 349 ms: 2.11x slower                                                  |
| deltablue                  | 3.45 ms                                                | 8.34 ms: 2.42x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.33x slower                                                          |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241204-3.14.0a2+-de73a27-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-de73a27.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.223x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x