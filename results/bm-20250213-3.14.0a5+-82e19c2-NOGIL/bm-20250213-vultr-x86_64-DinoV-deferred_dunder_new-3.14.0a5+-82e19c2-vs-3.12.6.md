# Results vs. 3.12.6

- fork: DinoV
- ref: deferred_dunder_new
- machine: linux-x86_64
- commit hash: 82e19c2
- commit date: 2025-02-13
- overall geometric mean: 1.047x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                 |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                               |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                  | 1.10x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                 |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                 |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                 |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                |
| regex_compile  | 142 ms                                                 | 152 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                 |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                 |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 362 us: 1.18x slower                                                 |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                |
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.98x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                 |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                                 |
| deepcopy                   | 352 us                                                 | 307 us: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                 |
| float                      | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.2 us: 1.03x faster                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.66 sec: 1.02x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.01x faster                                                 |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.00x slower                                                |
| generators                 | 32.2 ms                                                | 32.5 ms: 1.01x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                               |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                 |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.4 ms: 1.04x slower                                                |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                               |
| logging_silent             | 109 ns                                                 | 115 ns: 1.06x slower                                                 |
| regex_compile              | 142 ms                                                 | 152 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.07x slower                                               |
| logging_simple             | 6.63 us                                                | 7.12 us: 1.07x slower                                                |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 155 ms: 1.08x slower                                                 |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                |
| logging_format             | 7.35 us                                                | 8.10 us: 1.10x slower                                                |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                 |
| raytrace                   | 299 ms                                                 | 332 ms: 1.11x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 830 ms: 1.12x slower                                                 |
| chaos                      | 62.8 ms                                                | 70.3 ms: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                               |
| thrift                     | 791 us                                                 | 892 us: 1.13x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 96.2 ms: 1.13x slower                                                |
| pyflate                    | 448 ms                                                 | 512 ms: 1.14x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.94 ms: 1.14x slower                                                |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                 |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 61.3 ms: 1.15x slower                                                |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.15x slower                                                |
| scimark_fft                | 342 ms                                                 | 394 ms: 1.15x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 88.5 ms: 1.16x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.17x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 362 us: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 70.1 ms: 1.19x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                |
| hexiom                     | 6.17 ms                                                | 7.42 ms: 1.20x slower                                                |
| richards                   | 45.9 ms                                                | 55.5 ms: 1.21x slower                                                |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 83.4 ms: 1.22x slower                                                |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                                 |
| nqueens                    | 80.1 ms                                                | 98.3 ms: 1.23x slower                                                |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.6 ms: 1.25x slower                                                |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.28x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.67 ms: 1.29x slower                                                |
| telco                      | 6.53 ms                                                | 8.56 ms: 1.31x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                |
| fannkuch                   | 372 ms                                                 | 501 ms: 1.34x slower                                                 |
| coverage                   | 71.4 ms                                                | 96.8 ms: 1.36x slower                                                |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 94.6 ms: 8.76x slower                                                |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                         |

Benchmark hidden because not significant (2): pylint, spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250213-3.14.0a5+-82e19c2-NOGIL/bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x