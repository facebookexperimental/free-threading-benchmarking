# Results vs. 3.12.6

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: linux-x86_64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.201x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| html5lib       | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 222 ms: 2.09x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.01x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 538 ms: 2.01x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 286 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 472 ms: 1.52x faster                                                   |
| asyncio_tcp                | 519 ms                                                 | 445 ms: 1.17x faster                                                   |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 52.7 ms: 1.53x faster                                                  |
| nbody          | 89.3 ms                                                | 67.8 ms: 1.32x faster                                                  |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                  |
| regex_compile  | 142 ms                                                 | 121 ms: 1.17x faster                                                   |
| regex_dna      | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.50 sec: 1.40x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 170 us: 1.30x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 81.7 ms: 1.18x faster                                                  |
| json_dumps           | 10.4 ms                                                | 8.76 ms: 1.18x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 273 us: 1.13x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 53.0 ms: 1.11x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 79.0 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.1 us: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                                  |
| pickle_list          | 4.77 us                                                | 4.96 us: 1.04x slower                                                  |
| unpickle             | 14.1 us                                                | 14.7 us: 1.04x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.25 us: 1.12x slower                                                  |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 6.85 ms: 1.05x faster                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| mako            | 11.0 ms                                                | 10.1 ms: 1.09x faster                                                  |
| django_template | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.6 ms: 1.01x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.09x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.77x faster                                                   |
| richards_super             | 51.9 ms                                                | 21.2 ms: 2.45x faster                                                  |
| richards                   | 45.9 ms                                                | 18.9 ms: 2.43x faster                                                  |
| async_tree_none            | 464 ms                                                 | 222 ms: 2.09x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.17 sec: 2.07x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.01x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 538 ms: 2.01x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 280 ms: 2.00x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 286 ms: 1.94x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 22.3 us: 1.81x faster                                                  |
| scimark_sor                | 130 ms                                                 | 76.2 ms: 1.70x faster                                                  |
| spectral_norm              | 110 ms                                                 | 67.6 ms: 1.63x faster                                                  |
| deepcopy                   | 352 us                                                 | 225 us: 1.56x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                   |
| float                      | 80.8 ms                                                | 52.7 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 472 ms: 1.52x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 76.7 ms: 1.49x faster                                                  |
| logging_silent             | 109 ns                                                 | 75.8 ns: 1.44x faster                                                  |
| comprehensions             | 19.8 us                                                | 14.1 us: 1.41x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.50 sec: 1.40x faster                                                 |
| go                         | 139 ms                                                 | 99.9 ms: 1.39x faster                                                  |
| scimark_fft                | 342 ms                                                 | 246 ms: 1.39x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 50.4 ms: 1.36x faster                                                  |
| nbody                      | 89.3 ms                                                | 67.8 ms: 1.32x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 170 us: 1.30x faster                                                   |
| chaos                      | 62.8 ms                                                | 48.6 ms: 1.29x faster                                                  |
| deltablue                  | 3.45 ms                                                | 2.67 ms: 1.29x faster                                                  |
| pyflate                    | 448 ms                                                 | 353 ms: 1.27x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.0 ms: 1.26x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.26 us: 1.26x faster                                                  |
| logging_format             | 7.35 us                                                | 5.86 us: 1.25x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.45 us: 1.25x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.87 sec: 1.22x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.24 sec: 1.22x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 610 ms: 1.22x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 248 ms: 1.21x faster                                                   |
| nqueens                    | 80.1 ms                                                | 66.6 ms: 1.20x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 81.7 ms: 1.18x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 8.76 ms: 1.18x faster                                                  |
| genshi_text                | 22.8 ms                                                | 19.3 ms: 1.18x faster                                                  |
| regex_compile              | 142 ms                                                 | 121 ms: 1.17x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.76 ms: 1.17x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 445 ms: 1.17x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.8 ms: 1.16x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.8 ms: 1.13x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 273 us: 1.13x faster                                                   |
| fannkuch                   | 372 ms                                                 | 332 ms: 1.12x faster                                                   |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.11x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 53.0 ms: 1.11x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 148 us: 1.10x faster                                                   |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                   |
| mako                       | 11.0 ms                                                | 10.1 ms: 1.09x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.69 ms: 1.08x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 79.0 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| meteor_contest             | 104 ms                                                 | 96.6 ms: 1.07x faster                                                  |
| django_template            | 34.7 ms                                                | 32.4 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                 |
| python_startup_no_site     | 7.16 ms                                                | 6.85 ms: 1.05x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.12 us: 1.04x faster                                                  |
| json                       | 5.02 ms                                                | 4.85 ms: 1.04x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                 |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| thrift                     | 791 us                                                 | 773 us: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                                   |
| pickle_dict                | 31.8 us                                                | 31.1 us: 1.02x faster                                                  |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.02x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 49.6 ms: 1.01x faster                                                  |
| sympy_str                  | 292 ms                                                 | 289 ms: 1.01x faster                                                   |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 167 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.03x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.96 us: 1.04x slower                                                  |
| unpickle                   | 14.1 us                                                | 14.7 us: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| unpickle_list              | 4.67 us                                                | 5.25 us: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| pickle                     | 10.9 us                                                | 12.7 us: 1.16x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.33 ms: 1.25x slower                                                  |
| unpack_sequence            | 52.1 ns                                                | 65.5 ns: 1.26x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.29 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.72x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 184 ms: 17.08x slower                                                  |
| telco                      | 6.53 ms                                                | 145 ms: 22.28x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                           |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.201x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.21x