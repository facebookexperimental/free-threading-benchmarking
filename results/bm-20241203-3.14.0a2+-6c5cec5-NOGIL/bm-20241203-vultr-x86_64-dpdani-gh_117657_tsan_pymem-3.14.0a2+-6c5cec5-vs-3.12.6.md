# Results vs. 3.12.6

- fork: dpdani
- ref: gh_117657_tsan_pymem
- machine: linux-x86_64
- commit hash: 6c5cec5
- commit date: 2024-12-03
- overall geometric mean: 1.253x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 376 ms: 1.43x slower                                                   |
| docutils       | 2.64 sec                                               | 3.20 sec: 1.21x slower                                                 |
| html5lib       | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                  | 1.39x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 861 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 364 ms: 1.22x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 886 ms: 1.22x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 460 ms: 1.22x faster                                                   |
| async_tree_none            | 464 ms                                                 | 397 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 621 ms: 1.16x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 488 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 653 ms: 1.10x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.1 ms: 1.17x slower                                                  |
| async_generators           | 384 ms                                                 | 465 ms: 1.21x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| float          | 80.8 ms                                                | 143 ms: 1.77x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 26.0 ms: 1.26x slower                                                  |
| regex_compile  | 142 ms                                                 | 191 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 94.4 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.74 sec: 1.30x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 81.9 ms: 1.39x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 379 us: 1.72x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 556 us: 1.81x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.0 ms: 1.32x slower                                                  |
| genshi_text     | 22.8 ms                                                | 33.2 ms: 1.46x slower                                                  |
| django_template | 34.7 ms                                                | 55.4 ms: 1.60x slower                                                  |
| mako            | 11.0 ms                                                | 19.6 ms: 1.78x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.53x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 861 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 364 ms: 1.22x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 886 ms: 1.22x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 460 ms: 1.22x faster                                                   |
| async_tree_none            | 464 ms                                                 | 397 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 621 ms: 1.16x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 488 ms: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 653 ms: 1.10x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.6 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.4 ms: 1.02x faster                                                  |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.33 us: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 44.2 us: 1.10x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.40 sec: 1.14x slower                                                 |
| scimark_fft                | 342 ms                                                 | 398 ms: 1.17x slower                                                   |
| spectral_norm              | 110 ms                                                 | 129 ms: 1.17x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.1 ms: 1.17x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                   |
| generators                 | 32.2 ms                                                | 38.9 ms: 1.21x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.72 us: 1.21x slower                                                  |
| async_generators           | 384 ms                                                 | 465 ms: 1.21x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 92.8 ms: 1.21x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.20 sec: 1.21x slower                                                 |
| pylint                     | 319 ms                                                 | 394 ms: 1.24x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 98.5 ms: 1.25x slower                                                  |
| mdp                        | 2.42 sec                                               | 3.02 sec: 1.25x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 26.0 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.28x slower                                                   |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.28x slower                                                   |
| nqueens                    | 80.1 ms                                                | 104 ms: 1.29x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.74 sec: 1.30x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.73 ms: 1.30x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 66.0 ms: 1.32x slower                                                  |
| regex_compile              | 142 ms                                                 | 191 ms: 1.34x slower                                                   |
| fannkuch                   | 372 ms                                                 | 500 ms: 1.34x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.60 sec: 1.37x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.0 ms: 1.38x slower                                                  |
| telco                      | 6.53 ms                                                | 9.03 ms: 1.38x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 81.9 ms: 1.39x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 149 ms: 1.40x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 74.4 ms: 1.40x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 100 ms: 1.41x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 1.05 sec: 1.42x slower                                                 |
| 2to3                       | 264 ms                                                 | 376 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.19 sec: 1.44x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 207 ms: 1.45x slower                                                   |
| genshi_text                | 22.8 ms                                                | 33.2 ms: 1.46x slower                                                  |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| comprehensions             | 19.8 us                                                | 29.1 us: 1.47x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 30.7 ms: 1.49x slower                                                  |
| thrift                     | 791 us                                                 | 1.20 ms: 1.51x slower                                                  |
| html5lib                   | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                  |
| django_template            | 34.7 ms                                                | 55.4 ms: 1.60x slower                                                  |
| pyflate                    | 448 ms                                                 | 731 ms: 1.63x slower                                                   |
| logging_format             | 7.35 us                                                | 12.1 us: 1.64x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.65x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 193 ms: 1.69x slower                                                   |
| sympy_str                  | 292 ms                                                 | 493 ms: 1.69x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 379 us: 1.72x slower                                                   |
| hexiom                     | 6.17 ms                                                | 10.7 ms: 1.73x slower                                                  |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| float                      | 80.8 ms                                                | 143 ms: 1.77x slower                                                   |
| chaos                      | 62.8 ms                                                | 112 ms: 1.78x slower                                                   |
| mako                       | 11.0 ms                                                | 19.6 ms: 1.78x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.80x slower                                                   |
| richards                   | 45.9 ms                                                | 82.7 ms: 1.80x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 556 us: 1.81x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 3.06 ms: 1.83x slower                                                  |
| logging_silent             | 109 ns                                                 | 202 ns: 1.85x slower                                                   |
| scimark_sor                | 130 ms                                                 | 243 ms: 1.87x slower                                                   |
| richards_super             | 51.9 ms                                                | 99.1 ms: 1.91x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.65 ms: 1.95x slower                                                  |
| raytrace                   | 299 ms                                                 | 602 ms: 2.01x slower                                                   |
| go                         | 139 ms                                                 | 281 ms: 2.02x slower                                                   |
| sympy_expand               | 468 ms                                                 | 984 ms: 2.10x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.84 ms: 2.57x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                           |

Benchmark hidden because not significant (2): deepcopy, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-6c5cec5-NOGIL/bm-20241203-vultr-x86_64-dpdani-gh_117657_tsan_pymem-3.14.0a2+-6c5cec5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.253x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x