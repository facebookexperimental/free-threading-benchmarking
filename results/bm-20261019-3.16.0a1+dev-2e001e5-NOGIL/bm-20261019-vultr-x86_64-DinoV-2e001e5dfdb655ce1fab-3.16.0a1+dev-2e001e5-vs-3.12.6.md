# Results vs. 3.12.6

- fork: DinoV
- ref: 2e001e5dfdb655ce1fab
- machine: linux-x86_64
- commit hash: 2e001e5
- commit date: 2026-10-19
- overall geometric mean: 1.046x slower
- HPT reliability: 84.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.45x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                                     |
| docutils       | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                   |
| html5lib       | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 723 ms: 1.50x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                                     |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 580 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 596 ms: 1.20x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 499 ms: 1.04x faster                                                     |
| async_generators           | 384 ms                                                 | 421 ms: 1.09x slower                                                     |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.10x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.00x faster                                                     |
| float          | 80.8 ms                                                | 86.3 ms: 1.07x slower                                                    |
| nbody          | 89.3 ms                                                | 122 ms: 1.36x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| regex_compile  | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 97.2 ms: 1.01x slower                                                    |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.10x slower                                                     |
| json_loads           | 26.5 us                                                | 30.3 us: 1.14x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 104 ms: 1.22x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 77.6 ms: 1.32x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                    |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                    |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.34x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 135 ms: 2.36x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.89x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.41 sec: 1.71x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 705 ms: 1.57x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 723 ms: 1.50x faster                                                     |
| bench_mp_pool              | 10.8 ms                                                | 7.34 ms: 1.47x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 395 ms: 1.42x faster                                                     |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.34x faster                                                     |
| deepcopy                   | 352 us                                                 | 273 us: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 580 ms: 1.25x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 33.2 us: 1.21x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 596 ms: 1.20x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                    |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                    |
| spectral_norm              | 110 ms                                                 | 101 ms: 1.09x faster                                                     |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                   |
| comprehensions             | 19.8 us                                                | 18.4 us: 1.08x faster                                                    |
| scimark_fft                | 342 ms                                                 | 320 ms: 1.07x faster                                                     |
| chaos                      | 62.8 ms                                                | 59.9 ms: 1.05x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 499 ms: 1.04x faster                                                     |
| pyflate                    | 448 ms                                                 | 436 ms: 1.03x faster                                                     |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                                     |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.03 us: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                 | 183 ms: 1.00x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 97.2 ms: 1.01x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                    |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                     |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| generators                 | 32.2 ms                                                | 34.3 ms: 1.06x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.06 us: 1.06x slower                                                    |
| float                      | 80.8 ms                                                | 86.3 ms: 1.07x slower                                                    |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                    |
| html5lib                   | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.65 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.76 ms: 1.08x slower                                                    |
| logging_format             | 7.35 us                                                | 7.96 us: 1.08x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.76 ms: 1.09x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                     |
| async_generators           | 384 ms                                                 | 421 ms: 1.09x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.10x slower                                                     |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.10x slower                                                    |
| nqueens                    | 80.1 ms                                                | 88.2 ms: 1.10x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 820 ms: 1.10x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.8 ms: 1.11x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 76.2 ms: 1.11x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.98 sec: 1.13x slower                                                   |
| json_loads                 | 26.5 us                                                | 30.3 us: 1.14x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 87.6 ms: 1.14x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 191 ms: 1.15x slower                                                     |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                     |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 53.0 ms: 1.15x slower                                                    |
| richards_super             | 51.9 ms                                                | 60.5 ms: 1.17x slower                                                    |
| thrift                     | 791 us                                                 | 947 us: 1.20x slower                                                     |
| regex_compile              | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| sympy_expand               | 468 ms                                                 | 564 ms: 1.21x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.21x slower                                                    |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.21x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 104 ms: 1.22x slower                                                     |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                    |
| fannkuch                   | 372 ms                                                 | 465 ms: 1.25x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 77.6 ms: 1.32x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                    |
| nbody                      | 89.3 ms                                                | 122 ms: 1.36x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.37 ms: 1.45x slower                                                    |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                                    |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                    |
| coverage                   | 71.4 ms                                                | 120 ms: 1.68x slower                                                     |
| telco                      | 6.53 ms                                                | 178 ms: 27.26x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                             |

Benchmark hidden because not significant (1): json_dumps
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261019-3.16.0a1+dev-2e001e5-NOGIL/bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1+dev-2e001e5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 84.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.45x