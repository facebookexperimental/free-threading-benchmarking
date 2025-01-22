# Results vs. 3.12.6

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.075x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 311 ms: 1.18x slower                                                   |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| html5lib       | 63.6 ms                                                | 74.5 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.0 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.03x slower                                                   |
| nbody          | 89.3 ms                                                | 138 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_compile  | 142 ms                                                 | 159 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.42 sec: 1.15x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 98.6 ms: 1.16x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 274 us: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 74.7 ms: 1.27x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 392 us: 1.28x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| django_template | 34.7 ms                                                | 44.8 ms: 1.29x slower                                                  |
| genshi_text     | 22.8 ms                                                | 29.7 ms: 1.30x slower                                                  |
| mako            | 11.0 ms                                                | 16.1 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 317 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.13 ms: 1.10x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| deepcopy                   | 352 us                                                 | 324 us: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 78.0 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.0 us: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.81 sec: 1.01x slower                                                 |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 191 ms: 1.03x slower                                                   |
| generators                 | 32.2 ms                                                | 33.4 ms: 1.04x slower                                                  |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.04x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.05x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 84.4 ms: 1.07x slower                                                  |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                                   |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| comprehensions             | 19.8 us                                                | 21.5 us: 1.09x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.40 us: 1.11x slower                                                  |
| logging_silent             | 109 ns                                                 | 121 ns: 1.11x slower                                                   |
| regex_compile              | 142 ms                                                 | 159 ms: 1.11x slower                                                   |
| raytrace                   | 299 ms                                                 | 337 ms: 1.12x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.6 ms: 1.13x slower                                                  |
| chaos                      | 62.8 ms                                                | 71.1 ms: 1.13x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.74 sec: 1.13x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 848 ms: 1.14x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 87.6 ms: 1.14x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.42 sec: 1.15x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 191 ms: 1.15x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                                   |
| pyflate                    | 448 ms                                                 | 517 ms: 1.15x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.6 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.16x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.72 us: 1.16x slower                                                  |
| scimark_fft                | 342 ms                                                 | 398 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 62.3 ms: 1.17x slower                                                  |
| thrift                     | 791 us                                                 | 927 us: 1.17x slower                                                   |
| html5lib                   | 63.6 ms                                                | 74.5 ms: 1.17x slower                                                  |
| sympy_str                  | 292 ms                                                 | 344 ms: 1.18x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                  |
| 2to3                       | 264 ms                                                 | 311 ms: 1.18x slower                                                   |
| logging_format             | 7.35 us                                                | 8.71 us: 1.19x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.99 ms: 1.19x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.7 ms: 1.20x slower                                                  |
| sympy_expand               | 468 ms                                                 | 567 ms: 1.21x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 83.0 ms: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 55.9 ms: 1.22x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.22x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.64 ms: 1.24x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 274 us: 1.24x slower                                                   |
| nqueens                    | 80.1 ms                                                | 99.3 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                  |
| richards_super             | 51.9 ms                                                | 65.1 ms: 1.26x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 74.7 ms: 1.27x slower                                                  |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 392 us: 1.28x slower                                                   |
| django_template            | 34.7 ms                                                | 44.8 ms: 1.29x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 212 us: 1.30x slower                                                   |
| genshi_text                | 22.8 ms                                                | 29.7 ms: 1.30x slower                                                  |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                                  |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.93 ms: 1.35x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.73 ms: 1.37x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.47x slower                                                  |
| nbody                      | 89.3 ms                                                | 138 ms: 1.54x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.35 ms: 3.56x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.7 ms: 8.87x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x