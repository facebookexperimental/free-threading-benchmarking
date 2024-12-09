# Results vs. 3.12.6

- fork: python
- ref: a03efb533a58fd13fb0c
- machine: linux-x86_64
- commit hash: a03efb5
- commit date: 2024-12-08
- overall geometric mean: 1.229x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 371 ms: 1.41x slower                                                   |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                 |
| html5lib       | 63.6 ms                                                | 98.7 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                  | 1.37x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                                   |
| async_tree_none            | 464 ms                                                 | 385 ms: 1.21x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 471 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 615 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 646 ms: 1.11x faster                                                   |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                  |
| async_generators           | 384 ms                                                 | 459 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| float          | 80.8 ms                                                | 140 ms: 1.74x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| regex_compile  | 142 ms                                                 | 182 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.9 ms: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.8 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.9 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.70 sec: 1.28x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 77.9 ms: 1.32x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 335 us: 1.52x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 514 us: 1.67x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 65.0 ms: 1.30x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.9 ms: 1.40x slower                                                  |
| django_template | 34.7 ms                                                | 50.8 ms: 1.46x slower                                                  |
| mako            | 11.0 ms                                                | 17.9 ms: 1.63x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.44x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 827 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 445 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                                   |
| async_tree_none            | 464 ms                                                 | 385 ms: 1.21x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 471 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 615 ms: 1.18x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 646 ms: 1.11x faster                                                   |
| deepcopy                   | 352 us                                                 | 329 us: 1.07x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.9 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| json                       | 5.02 ms                                                | 5.10 ms: 1.02x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.04x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.09x slower                                                  |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.12x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.53 us: 1.15x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.9 ms: 1.15x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.18x slower                                                 |
| async_generators           | 384 ms                                                 | 459 ms: 1.19x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 92.2 ms: 1.20x slower                                                  |
| generators                 | 32.2 ms                                                | 38.8 ms: 1.20x slower                                                  |
| scimark_fft                | 342 ms                                                 | 412 ms: 1.21x slower                                                   |
| pylint                     | 319 ms                                                 | 384 ms: 1.21x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.96 sec: 1.22x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.9 ms: 1.22x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 97.0 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                   |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                   |
| regex_compile              | 142 ms                                                 | 182 ms: 1.28x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.70 sec: 1.28x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 138 ms: 1.29x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 65.0 ms: 1.30x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 69.7 ms: 1.31x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 77.9 ms: 1.32x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 988 ms: 1.33x slower                                                   |
| telco                      | 6.53 ms                                                | 8.71 ms: 1.33x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.57 sec: 1.34x slower                                                 |
| fannkuch                   | 372 ms                                                 | 501 ms: 1.35x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.7 ms: 1.36x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.12 ms: 1.39x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.9 ms: 1.40x slower                                                  |
| 2to3                       | 264 ms                                                 | 371 ms: 1.41x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.44x slower                                                  |
| django_template            | 34.7 ms                                                | 50.8 ms: 1.46x slower                                                  |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| thrift                     | 791 us                                                 | 1.18 ms: 1.50x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 335 us: 1.52x slower                                                   |
| pyflate                    | 448 ms                                                 | 694 ms: 1.55x slower                                                   |
| html5lib                   | 63.6 ms                                                | 98.7 ms: 1.55x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.89 ms: 1.60x slower                                                  |
| mako                       | 11.0 ms                                                | 17.9 ms: 1.63x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 187 ms: 1.63x slower                                                   |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.64x slower                                                  |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                                   |
| logging_format             | 7.35 us                                                | 12.1 us: 1.64x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 514 us: 1.67x slower                                                   |
| chaos                      | 62.8 ms                                                | 105 ms: 1.68x slower                                                   |
| richards                   | 45.9 ms                                                | 77.2 ms: 1.68x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                  |
| richards_super             | 51.9 ms                                                | 88.5 ms: 1.71x slower                                                  |
| logging_silent             | 109 ns                                                 | 188 ns: 1.72x slower                                                   |
| float                      | 80.8 ms                                                | 140 ms: 1.74x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.76x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.99 ms: 1.79x slower                                                  |
| scimark_sor                | 130 ms                                                 | 238 ms: 1.83x slower                                                   |
| raytrace                   | 299 ms                                                 | 551 ms: 1.84x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.61 ms: 1.92x slower                                                  |
| go                         | 139 ms                                                 | 272 ms: 1.95x slower                                                   |
| sympy_expand               | 468 ms                                                 | 961 ms: 2.05x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                   |
| deltablue                  | 3.45 ms                                                | 7.95 ms: 2.31x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.42 ms: 3.64x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.11x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241208-3.14.0a2+-a03efb5-NOGIL/bm-20241208-vultr-x86_64-python-a03efb533a58fd13fb0c-3.14.0a2+-a03efb5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.229x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.32x