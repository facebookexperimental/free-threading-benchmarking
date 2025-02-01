# Results vs. 3.12.6

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.029x slower
- HPT reliability: 99.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 295 ms: 1.12x slower                                                   |
| docutils       | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| html5lib       | 63.6 ms                                                | 69.2 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 561 ms: 1.98x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 548 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 582 ms: 1.23x faster                                                   |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.4 ms: 1.09x faster                                                  |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                                   |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 94.5 ms: 1.11x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 67.1 ms: 1.14x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                   |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                  |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                  |
| django_template | 34.7 ms                                                | 41.0 ms: 1.18x slower                                                  |
| mako            | 11.0 ms                                                | 15.3 ms: 1.39x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.73 ms: 2.00x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 561 ms: 1.98x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 548 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 582 ms: 1.23x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                  |
| deepcopy                   | 352 us                                                 | 301 us: 1.17x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 36.9 us: 1.09x faster                                                  |
| float                      | 80.8 ms                                                | 74.4 ms: 1.09x faster                                                  |
| generators                 | 32.2 ms                                                | 30.6 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| go                         | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.04x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.57 sec: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                 |
| scimark_sor                | 130 ms                                                 | 129 ms: 1.01x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.09 us: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 80.9 ms: 1.03x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.74 sec: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 783 ms: 1.05x slower                                                   |
| raytrace                   | 299 ms                                                 | 316 ms: 1.05x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.01 us: 1.06x slower                                                  |
| chaos                      | 62.8 ms                                                | 66.4 ms: 1.06x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.89 us: 1.07x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 154 ms: 1.08x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.27 sec: 1.08x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.61 sec: 1.08x slower                                                 |
| pyflate                    | 448 ms                                                 | 486 ms: 1.08x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                   |
| scimark_fft                | 342 ms                                                 | 372 ms: 1.09x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.2 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 118 ms: 1.10x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 94.5 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.87 ms: 1.12x slower                                                  |
| 2to3                       | 264 ms                                                 | 295 ms: 1.12x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 56.4 ms: 1.12x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 60.0 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 86.4 ms: 1.13x slower                                                  |
| sympy_str                  | 292 ms                                                 | 330 ms: 1.13x slower                                                   |
| thrift                     | 791 us                                                 | 897 us: 1.13x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.54 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 67.1 ms: 1.14x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.14x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.10 ms: 1.15x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                   |
| sympy_expand               | 468 ms                                                 | 542 ms: 1.16x slower                                                   |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                  |
| nqueens                    | 80.1 ms                                                | 93.2 ms: 1.16x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 80.5 ms: 1.18x slower                                                  |
| django_template            | 34.7 ms                                                | 41.0 ms: 1.18x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                   |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                  |
| richards_super             | 51.9 ms                                                | 63.9 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.45 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                  |
| fannkuch                   | 372 ms                                                 | 480 ms: 1.29x slower                                                   |
| deltablue                  | 3.45 ms                                                | 4.55 ms: 1.32x slower                                                  |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                                  |
| coverage                   | 71.4 ms                                                | 95.2 ms: 1.33x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                  |
| mako                       | 11.0 ms                                                | 15.3 ms: 1.39x slower                                                  |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 91.7 ms: 8.49x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250131-3.14.0a4+-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 99.61% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x