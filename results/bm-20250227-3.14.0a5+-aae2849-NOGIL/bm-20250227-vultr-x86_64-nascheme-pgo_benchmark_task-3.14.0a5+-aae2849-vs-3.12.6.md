# Results vs. 3.12.6

- fork: nascheme
- ref: pgo_benchmark_task
- machine: linux-x86_64
- commit hash: aae2849
- commit date: 2025-02-27
- overall geometric mean: 1.067x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 318 ms: 1.21x slower                                                   |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                 |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 600 ms: 1.19x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                  |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                  |
| regex_dna      | 168 ms                                                 | 163 ms: 1.03x faster                                                   |
| regex_compile  | 142 ms                                                 | 161 ms: 1.13x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.6 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 95.8 ms: 1.01x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 148 ms: 1.07x slower                                                   |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.50 sec: 1.19x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 278 us: 1.26x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 75.1 ms: 1.27x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 408 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.5 ms: 1.24x slower                                                  |
| django_template | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                  |
| genshi_text     | 22.8 ms                                                | 29.5 ms: 1.29x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.69 ms: 2.05x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 576 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 280 ms: 1.66x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 600 ms: 1.19x faster                                                   |
| deepcopy                   | 352 us                                                 | 321 us: 1.10x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                  |
| float                      | 80.8 ms                                                | 76.2 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.09 us: 1.05x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.05x faster                                                  |
| regex_dna                  | 168 ms                                                 | 163 ms: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 95.8 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                   |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                   |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.3 us: 1.02x slower                                                  |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                   |
| scimark_sor                | 130 ms                                                 | 137 ms: 1.06x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 148 ms: 1.07x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.26 sec: 1.08x slower                                                 |
| logging_silent             | 109 ns                                                 | 117 ns: 1.08x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.34 us: 1.08x slower                                                  |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 85.7 ms: 1.09x slower                                                  |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| json                       | 5.02 ms                                                | 5.47 ms: 1.09x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                                 |
| chaos                      | 62.8 ms                                                | 70.1 ms: 1.12x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 161 ms: 1.12x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.5 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 839 ms: 1.13x slower                                                   |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                                  |
| regex_compile              | 142 ms                                                 | 161 ms: 1.13x slower                                                   |
| scimark_fft                | 342 ms                                                 | 389 ms: 1.14x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.60 us: 1.15x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                  |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.27 ms: 1.16x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.02 ms: 1.17x slower                                                  |
| telco                      | 6.53 ms                                                | 7.63 ms: 1.17x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                                   |
| logging_format             | 7.35 us                                                | 8.64 us: 1.18x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 125 ms: 1.18x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.50 sec: 1.19x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 91.3 ms: 1.19x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.00 ms: 1.19x slower                                                  |
| pyflate                    | 448 ms                                                 | 535 ms: 1.20x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 63.7 ms: 1.20x slower                                                  |
| sympy_str                  | 292 ms                                                 | 352 ms: 1.21x slower                                                   |
| 2to3                       | 264 ms                                                 | 318 ms: 1.21x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.9 ms: 1.22x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 25.2 ms: 1.23x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 84.1 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.67 ms: 1.23x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                                   |
| thrift                     | 791 us                                                 | 980 us: 1.24x slower                                                   |
| sympy_expand               | 468 ms                                                 | 580 ms: 1.24x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 25.6 ms: 1.24x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.68 ms: 1.24x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 62.5 ms: 1.24x slower                                                  |
| fannkuch                   | 372 ms                                                 | 466 ms: 1.25x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 278 us: 1.26x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.55 ms: 1.26x slower                                                  |
| django_template            | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 75.1 ms: 1.27x slower                                                  |
| richards                   | 45.9 ms                                                | 59.2 ms: 1.29x slower                                                  |
| genshi_text                | 22.8 ms                                                | 29.5 ms: 1.29x slower                                                  |
| richards_super             | 51.9 ms                                                | 68.2 ms: 1.31x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 408 us: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| coverage                   | 71.4 ms                                                | 104 ms: 1.46x slower                                                   |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.63 ms: 3.85x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 96.6 ms: 8.94x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (3): coroutines, mdp, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250227-3.14.0a5+-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5+-aae2849.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.067x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.35x