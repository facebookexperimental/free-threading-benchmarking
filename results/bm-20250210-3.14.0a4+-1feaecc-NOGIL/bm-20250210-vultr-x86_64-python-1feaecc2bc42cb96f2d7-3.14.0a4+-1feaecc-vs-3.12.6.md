# Results vs. 3.12.6

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.050x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| html5lib       | 63.6 ms                                                | 72.4 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.6 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                   |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 248 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                  |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 369 us: 1.20x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                  |
| django_template | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.72 ms: 2.01x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 612 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                   |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 533 ms: 1.34x faster                                                   |
| deepcopy                   | 352 us                                                 | 309 us: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.7 ms: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 76.6 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                   |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.67 sec: 1.01x faster                                                 |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                                  |
| go                         | 139 ms                                                 | 140 ms: 1.01x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                 |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 82.7 ms: 1.05x slower                                                  |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                                   |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.22 us: 1.09x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                   |
| chaos                      | 62.8 ms                                                | 69.2 ms: 1.10x slower                                                  |
| raytrace                   | 299 ms                                                 | 330 ms: 1.10x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 825 ms: 1.11x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 248 us: 1.12x slower                                                   |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.6 ms: 1.13x slower                                                  |
| logging_format             | 7.35 us                                                | 8.32 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.14x slower                                                  |
| pyflate                    | 448 ms                                                 | 509 ms: 1.14x slower                                                   |
| html5lib                   | 63.6 ms                                                | 72.4 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.3 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                  |
| thrift                     | 791 us                                                 | 908 us: 1.15x slower                                                   |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| sympy_str                  | 292 ms                                                 | 338 ms: 1.16x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                  |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                                   |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                  |
| nqueens                    | 80.1 ms                                                | 95.4 ms: 1.19x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 369 us: 1.20x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 82.3 ms: 1.20x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.44 ms: 1.21x slower                                                  |
| django_template            | 34.7 ms                                                | 42.3 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                  |
| richards                   | 45.9 ms                                                | 56.6 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                  |
| richards_super             | 51.9 ms                                                | 65.7 ms: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.65 ms: 1.29x slower                                                  |
| telco                      | 6.53 ms                                                | 8.63 ms: 1.32x slower                                                  |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 96.8 ms: 1.36x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.74 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.1 ms: 8.81x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x