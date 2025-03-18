# Results vs. 3.12.6

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 258 ms: 1.02x faster                                                   |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 636 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                   |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 104 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| regex_compile  | 142 ms                                                 | 130 ms: 1.10x faster                                                   |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 59.8 ms: 1.01x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 225 us: 1.02x slower                                                   |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 326 us: 1.06x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.51x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 51.8 ms: 1.03x slower                                                  |
| django_template | 34.7 ms                                                | 36.5 ms: 1.05x slower                                                  |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 636 ms: 1.70x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 512 ms: 1.40x faster                                                   |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.7 us: 1.31x faster                                                  |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 67.8 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 97.1 ms: 1.13x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.71 us: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                  |
| scimark_sor                | 130 ms                                                 | 117 ms: 1.11x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.8 ms: 1.10x faster                                                  |
| regex_compile              | 142 ms                                                 | 130 ms: 1.10x faster                                                   |
| raytrace                   | 299 ms                                                 | 273 ms: 1.10x faster                                                   |
| generators                 | 32.2 ms                                                | 29.5 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 131 ms: 1.09x faster                                                   |
| logging_format             | 7.35 us                                                | 6.77 us: 1.08x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.13 us: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| chaos                      | 62.8 ms                                                | 58.9 ms: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 72.7 ms: 1.05x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 755 us: 1.05x faster                                                   |
| pyflate                    | 448 ms                                                 | 428 ms: 1.05x faster                                                   |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                  |
| richards                   | 45.9 ms                                                | 44.3 ms: 1.04x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.62 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.89 ms: 1.03x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.36 sec: 1.03x faster                                                 |
| genshi_text                | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 258 ms: 1.02x faster                                                   |
| scimark_fft                | 342 ms                                                 | 336 ms: 1.02x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 67.3 ms: 1.02x faster                                                  |
| richards_super             | 51.9 ms                                                | 51.0 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                                   |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 737 ms: 1.01x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.51 sec: 1.01x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                 |
| hexiom                     | 6.17 ms                                                | 6.14 ms: 1.00x faster                                                  |
| sympy_expand               | 468 ms                                                 | 472 ms: 1.01x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 59.8 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 225 us: 1.02x slower                                                   |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.02x slower                                                   |
| nqueens                    | 80.1 ms                                                | 82.6 ms: 1.03x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 51.8 ms: 1.03x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.55 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| django_template            | 34.7 ms                                                | 36.5 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 326 us: 1.06x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| fannkuch                   | 372 ms                                                 | 408 ms: 1.10x slower                                                   |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 80.4 ms: 1.13x slower                                                  |
| nbody                      | 89.3 ms                                                | 104 ms: 1.16x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| telco                      | 6.53 ms                                                | 7.80 ms: 1.20x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.61 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.16 ms: 1.20x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.51x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.3 ms: 8.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): sqlglot_optimize, asyncio_websockets, xml_etree_generate, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.12x