# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 0c173c9
- commit date: 2025-01-13
- overall geometric mean: 1.160x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 341 ms: 1.30x slower                                                    |
| docutils       | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                  |
| html5lib       | 63.6 ms                                                | 88.8 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 731 ms: 1.52x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 312 ms: 1.43x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 761 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 431 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 599 ms: 1.19x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                    |
| async_generators           | 384 ms                                                 | 448 ms: 1.17x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                    |
| float          | 80.8 ms                                                | 106 ms: 1.31x slower                                                    |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                  | 1.28x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                   |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                    |
| regex_compile  | 142 ms                                                 | 165 ms: 1.16x slower                                                    |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.9 ms: 1.09x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.37 sec: 1.13x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.3 ms: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.7 ms: 1.33x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 321 us: 1.46x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 487 us: 1.58x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                   |
| genshi_text     | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                   |
| django_template | 34.7 ms                                                | 49.9 ms: 1.44x slower                                                   |
| mako            | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 731 ms: 1.52x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 312 ms: 1.43x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 761 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 431 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 599 ms: 1.19x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.9 ms: 1.09x faster                                                   |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.12 us: 1.04x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                    |
| json                       | 5.02 ms                                                | 5.20 ms: 1.03x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.94 sec: 1.04x slower                                                  |
| pylint                     | 319 ms                                                 | 335 ms: 1.05x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.65 ms: 1.06x slower                                                   |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.43 us: 1.11x slower                                                   |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                    |
| scimark_fft                | 342 ms                                                 | 384 ms: 1.12x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.37 sec: 1.13x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 89.6 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.16x slower                                                  |
| regex_compile              | 142 ms                                                 | 165 ms: 1.16x slower                                                    |
| async_generators           | 384 ms                                                 | 448 ms: 1.17x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 90.2 ms: 1.18x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                   |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.4 ms: 1.22x slower                                                   |
| sympy_str                  | 292 ms                                                 | 356 ms: 1.22x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 25.2 ms: 1.22x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 73.3 ms: 1.24x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 66.3 ms: 1.24x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.24x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.25x slower                                                   |
| sympy_expand               | 468 ms                                                 | 584 ms: 1.25x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.57 ms: 1.27x slower                                                   |
| thrift                     | 791 us                                                 | 1.00 ms: 1.27x slower                                                   |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 946 ms: 1.27x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.27x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.8 ms: 1.28x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.96 sec: 1.29x slower                                                  |
| 2to3                       | 264 ms                                                 | 341 ms: 1.30x slower                                                    |
| fannkuch                   | 372 ms                                                 | 485 ms: 1.30x slower                                                    |
| float                      | 80.8 ms                                                | 106 ms: 1.31x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 13.7 ms: 1.33x slower                                                   |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                                   |
| genshi_text                | 22.8 ms                                                | 30.4 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                   |
| comprehensions             | 19.8 us                                                | 26.7 us: 1.35x slower                                                   |
| logging_simple             | 6.63 us                                                | 8.98 us: 1.35x slower                                                   |
| logging_format             | 7.35 us                                                | 10.1 us: 1.37x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 156 ms: 1.37x slower                                                    |
| coverage                   | 71.4 ms                                                | 99.0 ms: 1.39x slower                                                   |
| html5lib                   | 63.6 ms                                                | 88.8 ms: 1.40x slower                                                   |
| richards                   | 45.9 ms                                                | 65.0 ms: 1.42x slower                                                   |
| django_template            | 34.7 ms                                                | 49.9 ms: 1.44x slower                                                   |
| pyflate                    | 448 ms                                                 | 646 ms: 1.44x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 321 us: 1.46x slower                                                    |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                    |
| richards_super             | 51.9 ms                                                | 76.0 ms: 1.47x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 102 ms: 1.49x slower                                                    |
| hexiom                     | 6.17 ms                                                | 9.24 ms: 1.50x slower                                                   |
| chaos                      | 62.8 ms                                                | 94.7 ms: 1.51x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                   |
| mako                       | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                   |
| scimark_sor                | 130 ms                                                 | 203 ms: 1.57x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 2.63 ms: 1.58x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 487 us: 1.58x slower                                                    |
| logging_silent             | 109 ns                                                 | 177 ns: 1.62x slower                                                    |
| raytrace                   | 299 ms                                                 | 489 ms: 1.63x slower                                                    |
| go                         | 139 ms                                                 | 229 ms: 1.65x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.28 ms: 1.68x slower                                                   |
| deltablue                  | 3.45 ms                                                | 7.17 ms: 2.08x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.37 ms: 3.58x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 97.3 ms: 9.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.24x slower                                                            |

Benchmark hidden because not significant (2): deepcopy_memo, spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250113-3.14.0a3+-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.160x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.33x