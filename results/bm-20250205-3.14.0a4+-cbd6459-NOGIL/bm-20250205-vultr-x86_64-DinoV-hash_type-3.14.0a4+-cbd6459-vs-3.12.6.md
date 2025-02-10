# Results vs. 3.12.6

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.048x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                       |
| docutils       | 2.64 sec                                               | 2.85 sec: 1.08x slower                                     |
| html5lib       | 63.6 ms                                                | 70.7 ms: 1.11x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                       |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 323 ms: 1.73x faster                                       |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.59x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 361 ms: 1.54x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 552 ms: 1.30x faster                                       |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                       |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                      |
| Geometric mean             | (ref)                                                  | 1.42x faster                                               |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.6 ms: 1.07x faster                                      |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                       |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                       |
| Geometric mean | (ref)                                                  | 1.14x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                      |
| regex_compile  | 142 ms                                                 | 149 ms: 1.04x slower                                       |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                       |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                      |
| Geometric mean | (ref)                                                  | 1.03x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.5 ms: 1.10x faster                                      |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.08x slower                                     |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                       |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                      |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                      |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                      |
| pickle_pure_python   | 308 us                                                 | 376 us: 1.22x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                      |
| Geometric mean       | (ref)                                                  | 1.10x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.63 ms: 1.34x slower                                      |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                      |
| Geometric mean         | (ref)                                                  | 1.44x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.9 ms: 1.19x slower                                      |
| genshi_text     | 22.8 ms                                                | 27.4 ms: 1.20x slower                                      |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                      |
| mako            | 11.0 ms                                                | 16.0 ms: 1.46x slower                                      |
| Geometric mean  | (ref)                                                  | 1.27x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.97x faster                                      |
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                       |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 323 ms: 1.73x faster                                       |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.59x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 361 ms: 1.54x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 552 ms: 1.30x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                      |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 87.5 ms: 1.10x faster                                      |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| float                      | 80.8 ms                                                | 75.6 ms: 1.07x faster                                      |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                      |
| deepcopy_memo              | 40.3 us                                                | 38.2 us: 1.05x faster                                      |
| go                         | 139 ms                                                 | 135 ms: 1.03x faster                                       |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                       |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                      |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.66 sec: 1.02x faster                                     |
| comprehensions             | 19.8 us                                                | 19.8 us: 1.00x faster                                      |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                     |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                       |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                      |
| dulwich_log                | 78.9 ms                                                | 82.0 ms: 1.04x slower                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.21 us: 1.04x slower                                      |
| regex_compile              | 142 ms                                                 | 149 ms: 1.04x slower                                       |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                       |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                       |
| mdp                        | 2.42 sec                                               | 2.58 sec: 1.07x slower                                     |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                      |
| docutils                   | 2.64 sec                                               | 2.85 sec: 1.08x slower                                     |
| raytrace                   | 299 ms                                                 | 323 ms: 1.08x slower                                       |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.08x slower                                     |
| pprint_safe_repr           | 743 ms                                                 | 808 ms: 1.09x slower                                       |
| chaos                      | 62.8 ms                                                | 68.7 ms: 1.09x slower                                      |
| logging_simple             | 6.63 us                                                | 7.27 us: 1.10x slower                                      |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                     |
| pyflate                    | 448 ms                                                 | 497 ms: 1.11x slower                                       |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                       |
| html5lib                   | 63.6 ms                                                | 70.7 ms: 1.11x slower                                      |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 160 ms: 1.12x slower                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                      |
| logging_format             | 7.35 us                                                | 8.25 us: 1.12x slower                                      |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                       |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                      |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                       |
| thrift                     | 791 us                                                 | 909 us: 1.15x slower                                       |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                      |
| crypto_pyaes               | 76.6 ms                                                | 88.3 ms: 1.15x slower                                      |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                       |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.16x slower                                       |
| sqlglot_optimize           | 53.3 ms                                                | 61.9 ms: 1.16x slower                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                      |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                      |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                      |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                       |
| hexiom                     | 6.17 ms                                                | 7.31 ms: 1.18x slower                                      |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.19x slower                                      |
| genshi_xml                 | 50.2 ms                                                | 59.9 ms: 1.19x slower                                      |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 82.1 ms: 1.20x slower                                      |
| genshi_text                | 22.8 ms                                                | 27.4 ms: 1.20x slower                                      |
| nqueens                    | 80.1 ms                                                | 96.5 ms: 1.20x slower                                      |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                       |
| pickle_pure_python         | 308 us                                                 | 376 us: 1.22x slower                                       |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                      |
| richards                   | 45.9 ms                                                | 57.0 ms: 1.24x slower                                      |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                      |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                       |
| richards_super             | 51.9 ms                                                | 65.8 ms: 1.27x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.74 ms: 1.31x slower                                      |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                       |
| telco                      | 6.53 ms                                                | 8.55 ms: 1.31x slower                                      |
| deltablue                  | 3.45 ms                                                | 4.63 ms: 1.34x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.63 ms: 1.34x slower                                      |
| coverage                   | 71.4 ms                                                | 96.9 ms: 1.36x slower                                      |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.46x slower                                      |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                       |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                      |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 94.8 ms: 8.78x slower                                      |
| Geometric mean             | (ref)                                                  | 1.09x slower                                               |

Benchmark hidden because not significant (3): logging_silent, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x