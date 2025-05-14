# Results vs. 3.12.6

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 522 ms: 1.37x faster                                                  |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 303 us: 1.02x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.08x faster                                                |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 512 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 522 ms: 1.37x faster                                                  |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                                  |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.9 ms: 1.18x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                 |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.17x faster                                                 |
| spectral_norm              | 110 ms                                                 | 94.8 ms: 1.16x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.66 us: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.15x faster                                                  |
| richards                   | 45.9 ms                                                | 39.8 ms: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| chaos                      | 62.8 ms                                                | 54.9 ms: 1.14x faster                                                 |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                  |
| richards_super             | 51.9 ms                                                | 45.6 ms: 1.14x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.2 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 397 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.6 ms: 1.12x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.57 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.4 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.10x faster                                                 |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                                 |
| thrift                     | 791 us                                                 | 731 us: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.6 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 708 ms: 1.05x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                                 |
| scimark_fft                | 342 ms                                                 | 330 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| sympy_expand               | 468 ms                                                 | 453 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.03x faster                                                 |
| django_template            | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 303 us: 1.02x faster                                                  |
| logging_format             | 7.35 us                                                | 7.24 us: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.58 us: 1.01x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json                       | 5.02 ms                                                | 5.28 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 197 ms: 1.07x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.3 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.78 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.35 ms: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.7 ms: 1.14x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.72 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.90 ms: 1.74x slower                                                 |
| logging_silent             | 109 ns                                                 | 467 ns: 4.29x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 99.0 ms: 9.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (3): nbody, fannkuch, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x