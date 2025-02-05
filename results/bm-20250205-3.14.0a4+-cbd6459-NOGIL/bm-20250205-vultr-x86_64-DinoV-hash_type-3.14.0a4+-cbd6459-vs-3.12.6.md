# Results vs. 3.12.6

- fork: DinoV
- ref: hash_type
- machine: linux-x86_64
- commit hash: cbd6459
- commit date: 2025-02-05
- overall geometric mean: 1.050x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                       |
| docutils       | 2.64 sec                                               | 2.85 sec: 1.08x slower                                     |
| html5lib       | 63.6 ms                                                | 70.2 ms: 1.10x slower                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 575 ms: 1.93x faster                                       |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.79x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                       |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.63x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                       |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                       |
| Geometric mean             | (ref)                                                  | 1.44x faster                                               |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.6 ms: 1.06x faster                                      |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                       |
| nbody          | 89.3 ms                                                | 135 ms: 1.52x slower                                       |
| Geometric mean | (ref)                                                  | 1.15x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                      |
| regex_compile  | 142 ms                                                 | 149 ms: 1.05x slower                                       |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                       |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                      |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| tomli_loads          | 2.11 sec                                               | 2.32 sec: 1.10x slower                                     |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                      |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.14x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                      |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                      |
| pickle_pure_python   | 308 us                                                 | 368 us: 1.20x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                      |
| Geometric mean       | (ref)                                                  | 1.10x slower                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.63 ms: 1.34x slower                                      |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.55x slower                                      |
| Geometric mean         | (ref)                                                  | 1.44x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.2 ms: 1.20x slower                                      |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                      |
| django_template | 34.7 ms                                                | 42.7 ms: 1.23x slower                                      |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                      |
| Geometric mean  | (ref)                                                  | 1.27x slower                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.76 ms: 1.97x faster                                      |
| async_tree_io_tg           | 1.11 sec                                               | 575 ms: 1.93x faster                                       |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.79x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.76x faster                                       |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.63x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 537 ms: 1.33x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.15x faster                                      |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                      |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                       |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                      |
| float                      | 80.8 ms                                                | 76.6 ms: 1.06x faster                                      |
| deepcopy_memo              | 40.3 us                                                | 38.3 us: 1.05x faster                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.62 sec: 1.03x faster                                     |
| async_generators           | 384 ms                                                 | 375 ms: 1.02x faster                                       |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                       |
| comprehensions             | 19.8 us                                                | 19.9 us: 1.01x slower                                      |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                       |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                     |
| dulwich_log                | 78.9 ms                                                | 81.7 ms: 1.04x slower                                      |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                      |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                       |
| generators                 | 32.2 ms                                                | 33.6 ms: 1.04x slower                                      |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                       |
| regex_compile              | 142 ms                                                 | 149 ms: 1.05x slower                                       |
| json                       | 5.02 ms                                                | 5.40 ms: 1.07x slower                                      |
| docutils                   | 2.64 sec                                               | 2.85 sec: 1.08x slower                                     |
| mdp                        | 2.42 sec                                               | 2.64 sec: 1.09x slower                                     |
| logging_simple             | 6.63 us                                                | 7.24 us: 1.09x slower                                      |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                       |
| raytrace                   | 299 ms                                                 | 329 ms: 1.10x slower                                       |
| tomli_loads                | 2.11 sec                                               | 2.32 sec: 1.10x slower                                     |
| html5lib                   | 63.6 ms                                                | 70.2 ms: 1.10x slower                                      |
| pprint_safe_repr           | 743 ms                                                 | 822 ms: 1.11x slower                                       |
| logging_format             | 7.35 us                                                | 8.17 us: 1.11x slower                                      |
| pprint_pformat             | 1.52 sec                                               | 1.69 sec: 1.11x slower                                     |
| chaos                      | 62.8 ms                                                | 70.2 ms: 1.12x slower                                      |
| sqlalchemy_declarative     | 143 ms                                                 | 160 ms: 1.12x slower                                       |
| scimark_fft                | 342 ms                                                 | 383 ms: 1.12x slower                                       |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                      |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                      |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.14x slower                                       |
| pyflate                    | 448 ms                                                 | 511 ms: 1.14x slower                                       |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                       |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                      |
| thrift                     | 791 us                                                 | 908 us: 1.15x slower                                       |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                       |
| crypto_pyaes               | 76.6 ms                                                | 88.1 ms: 1.15x slower                                      |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                      |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.16x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                      |
| sqlglot_optimize           | 53.3 ms                                                | 61.9 ms: 1.16x slower                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                      |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                      |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                      |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                       |
| pickle_pure_python         | 308 us                                                 | 368 us: 1.20x slower                                       |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                      |
| nqueens                    | 80.1 ms                                                | 96.0 ms: 1.20x slower                                      |
| genshi_xml                 | 50.2 ms                                                | 60.2 ms: 1.20x slower                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 82.6 ms: 1.21x slower                                      |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.23x slower                                       |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                      |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                      |
| django_template            | 34.7 ms                                                | 42.7 ms: 1.23x slower                                      |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                      |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                       |
| richards_super             | 51.9 ms                                                | 65.0 ms: 1.25x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.60 ms: 1.27x slower                                      |
| fannkuch                   | 372 ms                                                 | 486 ms: 1.31x slower                                       |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.63 ms: 1.34x slower                                      |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.37x slower                                      |
| deltablue                  | 3.45 ms                                                | 4.75 ms: 1.38x slower                                      |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                      |
| nbody                      | 89.3 ms                                                | 135 ms: 1.52x slower                                       |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.55x slower                                      |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 94.6 ms: 8.76x slower                                      |
| Geometric mean             | (ref)                                                  | 1.09x slower                                               |

Benchmark hidden because not significant (4): coroutines, go, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4+-cbd6459.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x