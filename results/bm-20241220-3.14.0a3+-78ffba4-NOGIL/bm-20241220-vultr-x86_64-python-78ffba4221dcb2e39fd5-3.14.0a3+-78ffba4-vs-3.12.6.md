# Results vs. 3.12.6

- fork: python
- ref: 78ffba4221dcb2e39fd5
- machine: linux-x86_64
- commit hash: 78ffba4
- commit date: 2024-12-20
- overall geometric mean: 1.190x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 359 ms: 1.36x slower                                                   |
| docutils       | 2.64 sec                                               | 3.02 sec: 1.14x slower                                                 |
| html5lib       | 63.6 ms                                                | 93.4 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                  | 1.32x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 729 ms: 1.52x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 753 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 311 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                   |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 428 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 600 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 631 ms: 1.13x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                  |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| float          | 80.8 ms                                                | 113 ms: 1.39x slower                                                   |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| regex_compile  | 142 ms                                                 | 168 ms: 1.18x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.54 sec: 1.21x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 328 us: 1.49x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 506 us: 1.65x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.2 ms: 1.74x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                  |
| genshi_text     | 22.8 ms                                                | 30.9 ms: 1.36x slower                                                  |
| django_template | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                  |
| mako            | 11.0 ms                                                | 17.3 ms: 1.57x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 729 ms: 1.52x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 753 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 311 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                   |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 428 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 600 ms: 1.20x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 631 ms: 1.13x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.16 ms: 1.09x faster                                                  |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.0 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.15 us: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.6 us: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                  |
| spectral_norm              | 110 ms                                                 | 117 ms: 1.06x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.06x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                   |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.43 us: 1.11x slower                                                  |
| scimark_fft                | 342 ms                                                 | 386 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.02 sec: 1.14x slower                                                 |
| pylint                     | 319 ms                                                 | 364 ms: 1.14x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 90.5 ms: 1.15x slower                                                  |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                   |
| generators                 | 32.2 ms                                                | 38.0 ms: 1.18x slower                                                  |
| regex_compile              | 142 ms                                                 | 168 ms: 1.18x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.38 sec: 1.18x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 90.7 ms: 1.18x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.88 sec: 1.19x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.54 sec: 1.21x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 65.9 ms: 1.24x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                   |
| nqueens                    | 80.1 ms                                                | 99.7 ms: 1.25x slower                                                  |
| thrift                     | 791 us                                                 | 986 us: 1.25x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.25x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.6 ms: 1.27x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.8 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.64 ms: 1.28x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 961 ms: 1.29x slower                                                   |
| fannkuch                   | 372 ms                                                 | 488 ms: 1.31x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.74 ms: 1.34x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.9 ms: 1.36x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| 2to3                       | 264 ms                                                 | 359 ms: 1.36x slower                                                   |
| logging_simple             | 6.63 us                                                | 9.11 us: 1.37x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 197 ms: 1.38x slower                                                   |
| logging_format             | 7.35 us                                                | 10.1 us: 1.38x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.4 ms: 1.39x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.6 us: 1.39x slower                                                  |
| float                      | 80.8 ms                                                | 113 ms: 1.39x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 160 ms: 1.40x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.43x slower                                                  |
| pyflate                    | 448 ms                                                 | 648 ms: 1.45x slower                                                   |
| django_template            | 34.7 ms                                                | 50.7 ms: 1.46x slower                                                  |
| html5lib                   | 63.6 ms                                                | 93.4 ms: 1.47x slower                                                  |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| richards                   | 45.9 ms                                                | 67.6 ms: 1.47x slower                                                  |
| richards_super             | 51.9 ms                                                | 76.5 ms: 1.47x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 328 us: 1.49x slower                                                   |
| chaos                      | 62.8 ms                                                | 94.9 ms: 1.51x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.56x slower                                                   |
| hexiom                     | 6.17 ms                                                | 9.69 ms: 1.57x slower                                                  |
| mako                       | 11.0 ms                                                | 17.3 ms: 1.57x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.69 ms: 1.61x slower                                                  |
| sympy_str                  | 292 ms                                                 | 475 ms: 1.63x slower                                                   |
| raytrace                   | 299 ms                                                 | 490 ms: 1.64x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 506 us: 1.65x slower                                                   |
| scimark_sor                | 130 ms                                                 | 216 ms: 1.66x slower                                                   |
| logging_silent             | 109 ns                                                 | 184 ns: 1.69x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.33 ms: 1.72x slower                                                  |
| go                         | 139 ms                                                 | 241 ms: 1.73x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.2 ms: 1.74x slower                                                  |
| sympy_expand               | 468 ms                                                 | 952 ms: 2.04x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                   |
| deltablue                  | 3.45 ms                                                | 7.53 ms: 2.18x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.00x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.28x slower                                                           |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-78ffba4-NOGIL/bm-20241220-vultr-x86_64-python-78ffba4221dcb2e39fd5-3.14.0a3+-78ffba4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.190x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x