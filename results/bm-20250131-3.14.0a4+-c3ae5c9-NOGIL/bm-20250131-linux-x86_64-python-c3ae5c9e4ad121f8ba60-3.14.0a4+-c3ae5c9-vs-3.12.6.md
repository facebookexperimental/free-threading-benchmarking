# Results vs. 3.12.6

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.044x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 542 ms: 1.19x slower                                                   |
| docutils       | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                 |
| html5lib       | 88.9 ms                                                | 104 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 742 ms: 2.61x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 826 ms: 2.24x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 343 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 453 ms: 2.05x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 498 ms: 1.96x faster                                                   |
| async_tree_none            | 741 ms                                                 | 413 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 641 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 769 ms: 1.40x faster                                                   |
| coroutines                 | 29.5 ms                                                | 35.2 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| pidigits       | 250 ms                                                 | 235 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                 | 185 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.42 ms: 1.16x faster                                                  |
| regex_compile  | 187 ms                                                 | 205 ms: 1.10x slower                                                   |
| regex_dna      | 278 ms                                                 | 308 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 223 ms: 1.08x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 89.1 ms: 1.06x slower                                                  |
| json_loads           | 37.9 us                                                | 41.9 us: 1.11x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 3.27 sec: 1.13x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 356 us: 1.19x slower                                                   |
| xml_etree_generate   | 127 ms                                                 | 152 ms: 1.19x slower                                                   |
| json_dumps           | 14.3 ms                                                | 18.3 ms: 1.28x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 598 us: 1.37x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.2 ms: 1.21x slower                                                  |
| python_startup         | 23.7 ms                                                | 33.3 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 51.3 ms: 1.14x slower                                                  |
| genshi_text     | 30.2 ms                                                | 38.4 ms: 1.27x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 87.2 ms: 1.29x slower                                                  |
| mako            | 15.7 ms                                                | 24.2 ms: 1.54x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 742 ms: 2.61x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 826 ms: 2.24x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 343 ms: 2.05x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 453 ms: 2.05x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 498 ms: 1.96x faster                                                   |
| async_tree_none            | 741 ms                                                 | 413 ms: 1.79x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 641 ms: 1.72x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.88 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 769 ms: 1.40x faster                                                   |
| float                      | 123 ms                                                 | 103 ms: 1.20x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.42 ms: 1.16x faster                                                  |
| deepcopy                   | 468 us                                                 | 415 us: 1.13x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 223 ms: 1.08x faster                                                   |
| pathlib                    | 31.6 ms                                                | 29.7 ms: 1.07x faster                                                  |
| pidigits                   | 250 ms                                                 | 235 ms: 1.06x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.72 sec: 1.04x faster                                                 |
| docutils                   | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                 |
| go                         | 172 ms                                                 | 179 ms: 1.04x slower                                                   |
| spectral_norm              | 156 ms                                                 | 165 ms: 1.06x slower                                                   |
| logging_simple             | 9.45 us                                                | 10.0 us: 1.06x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 89.1 ms: 1.06x slower                                                  |
| pyflate                    | 727 ms                                                 | 777 ms: 1.07x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.50 ms: 1.07x slower                                                  |
| logging_silent             | 139 ns                                                 | 150 ns: 1.08x slower                                                   |
| generators                 | 41.1 ms                                                | 44.4 ms: 1.08x slower                                                  |
| regex_compile              | 187 ms                                                 | 205 ms: 1.10x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.43 us: 1.10x slower                                                  |
| sympy_str                  | 385 ms                                                 | 424 ms: 1.10x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.39 sec: 1.10x slower                                                 |
| json_loads                 | 37.9 us                                                | 41.9 us: 1.11x slower                                                  |
| regex_dna                  | 278 ms                                                 | 308 ms: 1.11x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.22 sec: 1.12x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.43 sec: 1.13x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.93 ms: 1.13x slower                                                  |
| scimark_fft                | 500 ms                                                 | 565 ms: 1.13x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.27 sec: 1.13x slower                                                 |
| json                       | 6.85 ms                                                | 7.77 ms: 1.14x slower                                                  |
| raytrace                   | 408 ms                                                 | 464 ms: 1.14x slower                                                   |
| django_template            | 44.9 ms                                                | 51.3 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 86.9 ms: 1.14x slower                                                  |
| logging_format             | 9.59 us                                                | 11.1 us: 1.15x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.12 sec: 1.16x slower                                                 |
| richards                   | 60.3 ms                                                | 70.2 ms: 1.16x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 125 ms: 1.16x slower                                                   |
| scimark_sor                | 167 ms                                                 | 194 ms: 1.16x slower                                                   |
| richards_super             | 72.8 ms                                                | 84.8 ms: 1.16x slower                                                  |
| html5lib                   | 88.9 ms                                                | 104 ms: 1.17x slower                                                   |
| sympy_expand               | 582 ms                                                 | 678 ms: 1.17x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 261 ms: 1.18x slower                                                   |
| 2to3                       | 456 ms                                                 | 542 ms: 1.19x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 356 us: 1.19x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 152 ms: 1.19x slower                                                   |
| coroutines                 | 29.5 ms                                                | 35.2 ms: 1.19x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.14 ms: 1.20x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.2 ms: 1.21x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 184 ms: 1.21x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 36.2 ms: 1.22x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 118 ms: 1.23x slower                                                   |
| fannkuch                   | 540 ms                                                 | 664 ms: 1.23x slower                                                   |
| nqueens                    | 117 ms                                                 | 145 ms: 1.24x slower                                                   |
| meteor_contest             | 146 ms                                                 | 184 ms: 1.26x slower                                                   |
| chaos                      | 84.9 ms                                                | 107 ms: 1.26x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.34 ms: 1.27x slower                                                  |
| telco                      | 9.59 ms                                                | 12.2 ms: 1.27x slower                                                  |
| genshi_text                | 30.2 ms                                                | 38.4 ms: 1.27x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.3 ms: 1.28x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 87.2 ms: 1.29x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.7 ms: 1.29x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 31.9 ms: 1.29x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 298 us: 1.33x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.10 ms: 1.36x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 598 us: 1.37x slower                                                   |
| python_startup             | 23.7 ms                                                | 33.3 ms: 1.41x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.84 ms: 1.46x slower                                                  |
| coverage                   | 95.4 ms                                                | 145 ms: 1.52x slower                                                   |
| mako                       | 15.7 ms                                                | 24.2 ms: 1.54x slower                                                  |
| deltablue                  | 4.27 ms                                                | 6.60 ms: 1.55x slower                                                  |
| nbody                      | 119 ms                                                 | 185 ms: 1.55x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 87.6 ms: 4.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (11): sqlglot_normalize, pylint, xml_etree_iterparse, async_generators, sqlite_synth, comprehensions, sqlalchemy_declarative, asyncio_websockets, dulwich_log, deepcopy_memo, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250131-3.14.0a4+-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x