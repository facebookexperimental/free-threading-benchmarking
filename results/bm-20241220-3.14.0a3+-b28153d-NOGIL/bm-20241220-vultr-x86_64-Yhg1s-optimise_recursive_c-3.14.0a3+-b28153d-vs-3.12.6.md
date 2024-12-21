# Results vs. 3.12.6

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: b28153d
- commit date: 2024-12-20
- overall geometric mean: 1.171x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 352 ms: 1.34x slower                                                  |
| docutils       | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                |
| html5lib       | 63.6 ms                                                | 90.8 ms: 1.43x slower                                                 |
| Geometric mean | (ref)                                                  | 1.29x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 742 ms: 1.50x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 317 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 405 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 433 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 573 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| float          | 80.8 ms                                                | 113 ms: 1.40x slower                                                  |
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                  | 1.29x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.09x faster                                                 |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 90.7 ms: 1.07x faster                                                 |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 73.4 ms: 1.24x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 501 us: 1.63x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.82 ms: 1.37x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.5 ms: 1.34x slower                                                 |
| django_template | 34.7 ms                                                | 49.4 ms: 1.42x slower                                                 |
| mako            | 11.0 ms                                                | 17.1 ms: 1.56x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 742 ms: 1.50x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 760 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 317 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 405 ms: 1.38x faster                                                  |
| async_tree_none            | 464 ms                                                 | 352 ms: 1.32x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 433 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 573 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.09x faster                                                 |
| deepcopy                   | 352 us                                                 | 324 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.7 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.12 us: 1.04x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                 |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.04 sec: 1.06x slower                                                |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                 |
| pylint                     | 319 ms                                                 | 348 ms: 1.09x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.39 us: 1.10x slower                                                 |
| scimark_fft                | 342 ms                                                 | 382 ms: 1.12x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 90.8 ms: 1.15x slower                                                 |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 89.9 ms: 1.17x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.18x slower                                                  |
| generators                 | 32.2 ms                                                | 38.0 ms: 1.18x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.87 sec: 1.19x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.39 sec: 1.19x slower                                                |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| sympy_str                  | 292 ms                                                 | 357 ms: 1.22x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.5 ms: 1.23x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 25.3 ms: 1.23x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                |
| sqlglot_optimize           | 53.3 ms                                                | 66.1 ms: 1.24x slower                                                 |
| thrift                     | 791 us                                                 | 984 us: 1.24x slower                                                  |
| sympy_expand               | 468 ms                                                 | 582 ms: 1.24x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 73.4 ms: 1.24x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.4 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                 |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 183 ms: 1.28x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 964 ms: 1.30x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                                |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                                 |
| 2to3                       | 264 ms                                                 | 352 ms: 1.34x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.5 ms: 1.34x slower                                                 |
| fannkuch                   | 372 ms                                                 | 500 ms: 1.34x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| logging_simple             | 6.63 us                                                | 9.06 us: 1.37x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.82 ms: 1.37x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                 |
| coverage                   | 71.4 ms                                                | 99.0 ms: 1.39x slower                                                 |
| logging_format             | 7.35 us                                                | 10.2 us: 1.39x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 160 ms: 1.40x slower                                                  |
| float                      | 80.8 ms                                                | 113 ms: 1.40x slower                                                  |
| django_template            | 34.7 ms                                                | 49.4 ms: 1.42x slower                                                 |
| pyflate                    | 448 ms                                                 | 639 ms: 1.43x slower                                                  |
| html5lib                   | 63.6 ms                                                | 90.8 ms: 1.43x slower                                                 |
| richards                   | 45.9 ms                                                | 67.2 ms: 1.46x slower                                                 |
| richards_super             | 51.9 ms                                                | 76.9 ms: 1.48x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                  |
| chaos                      | 62.8 ms                                                | 95.6 ms: 1.52x slower                                                 |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.54x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.57 ms: 1.55x slower                                                 |
| mako                       | 11.0 ms                                                | 17.1 ms: 1.56x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                 |
| logging_silent             | 109 ns                                                 | 177 ns: 1.62x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.72 ms: 1.63x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 501 us: 1.63x slower                                                  |
| raytrace                   | 299 ms                                                 | 489 ms: 1.63x slower                                                  |
| scimark_sor                | 130 ms                                                 | 215 ms: 1.65x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                 |
| go                         | 139 ms                                                 | 238 ms: 1.71x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.37 ms: 1.75x slower                                                 |
| deltablue                  | 3.45 ms                                                | 7.39 ms: 2.14x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 101 ms: 9.34x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                          |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-b28153d-NOGIL/bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.171x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.34x