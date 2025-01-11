# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.157x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 341 ms: 1.30x slower                                                    |
| docutils       | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                  |
| html5lib       | 63.6 ms                                                | 87.9 ms: 1.38x slower                                                   |
| Geometric mean | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 727 ms: 1.53x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 754 ms: 1.44x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 313 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 425 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 594 ms: 1.20x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                   |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| float          | 80.8 ms                                                | 106 ms: 1.32x slower                                                    |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                  | 1.25x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                   |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                   |
| regex_compile  | 142 ms                                                 | 166 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.35x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 323 us: 1.46x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 492 us: 1.60x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.5 ms: 1.24x slower                                                   |
| genshi_text     | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                   |
| django_template | 34.7 ms                                                | 48.9 ms: 1.41x slower                                                   |
| mako            | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 727 ms: 1.53x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 754 ms: 1.44x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 313 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                    |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 425 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 594 ms: 1.20x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.7 ms: 1.09x faster                                                   |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.10 us: 1.05x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.33 ms: 1.04x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.7 us: 1.01x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                    |
| json                       | 5.02 ms                                                | 5.24 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.99 sec: 1.05x slower                                                  |
| pylint                     | 319 ms                                                 | 337 ms: 1.06x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.43 us: 1.12x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                  |
| scimark_fft                | 342 ms                                                 | 383 ms: 1.12x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 89.8 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 97.1 ms: 1.14x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.16x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                   |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                    |
| regex_compile              | 142 ms                                                 | 166 ms: 1.16x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 89.5 ms: 1.17x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.88 sec: 1.19x slower                                                  |
| generators                 | 32.2 ms                                                | 38.5 ms: 1.19x slower                                                   |
| sympy_str                  | 292 ms                                                 | 352 ms: 1.21x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 24.9 ms: 1.21x slower                                                   |
| nqueens                    | 80.1 ms                                                | 98.0 ms: 1.22x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 65.4 ms: 1.23x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 132 ms: 1.24x slower                                                    |
| sympy_expand               | 468 ms                                                 | 578 ms: 1.24x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 62.5 ms: 1.24x slower                                                   |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 939 ms: 1.26x slower                                                    |
| thrift                     | 791 us                                                 | 1.00 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.59 ms: 1.27x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.7 ms: 1.27x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.27x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.96 sec: 1.29x slower                                                  |
| 2to3                       | 264 ms                                                 | 341 ms: 1.30x slower                                                    |
| fannkuch                   | 372 ms                                                 | 484 ms: 1.30x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.43 ms: 1.31x slower                                                   |
| float                      | 80.8 ms                                                | 106 ms: 1.32x slower                                                    |
| telco                      | 6.53 ms                                                | 8.65 ms: 1.32x slower                                                   |
| logging_format             | 7.35 us                                                | 9.84 us: 1.34x slower                                                   |
| genshi_text                | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                   |
| logging_simple             | 6.63 us                                                | 8.90 us: 1.34x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.35x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.67 ms: 1.35x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.36x slower                                                    |
| comprehensions             | 19.8 us                                                | 27.4 us: 1.38x slower                                                   |
| html5lib                   | 63.6 ms                                                | 87.9 ms: 1.38x slower                                                   |
| coverage                   | 71.4 ms                                                | 98.8 ms: 1.38x slower                                                   |
| django_template            | 34.7 ms                                                | 48.9 ms: 1.41x slower                                                   |
| pyflate                    | 448 ms                                                 | 635 ms: 1.42x slower                                                    |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                    |
| richards                   | 45.9 ms                                                | 66.0 ms: 1.44x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 323 us: 1.46x slower                                                    |
| richards_super             | 51.9 ms                                                | 77.0 ms: 1.48x slower                                                   |
| hexiom                     | 6.17 ms                                                | 9.18 ms: 1.49x slower                                                   |
| chaos                      | 62.8 ms                                                | 93.5 ms: 1.49x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 103 ms: 1.50x slower                                                    |
| scimark_sor                | 130 ms                                                 | 202 ms: 1.56x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                   |
| mako                       | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.62 ms: 1.57x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 492 us: 1.60x slower                                                    |
| raytrace                   | 299 ms                                                 | 489 ms: 1.63x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.24 ms: 1.65x slower                                                   |
| go                         | 139 ms                                                 | 230 ms: 1.65x slower                                                    |
| logging_silent             | 109 ns                                                 | 183 ns: 1.68x slower                                                    |
| deltablue                  | 3.45 ms                                                | 7.31 ms: 2.12x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 94.3 ms: 8.74x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.23x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250109-3.14.0a3+-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.157x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.34x