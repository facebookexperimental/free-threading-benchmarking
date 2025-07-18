# Results vs. 3.12.6

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: linux-x86_64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 60.3 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.5 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 306 us: 1.00x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.81x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 316 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.6 us: 1.41x faster                                                 |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                 |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.22x faster                                                  |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.15x faster                                                  |
| float                      | 80.8 ms                                                | 70.5 ms: 1.15x faster                                                 |
| spectral_norm              | 110 ms                                                 | 96.3 ms: 1.14x faster                                                 |
| logging_silent             | 109 ns                                                 | 95.3 ns: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.70 us: 1.14x faster                                                 |
| richards                   | 45.9 ms                                                | 40.5 ms: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 396 ms: 1.13x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.05 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| generators                 | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.2 ms: 1.12x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.91 us: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.3 ms: 1.12x faster                                                 |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.58 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.9 ms: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 693 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.3 ms: 1.06x faster                                                 |
| thrift                     | 791 us                                                 | 754 us: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.0 ms: 1.05x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                 |
| nqueens                    | 80.1 ms                                                | 77.0 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| scimark_fft                | 342 ms                                                 | 334 ms: 1.02x faster                                                  |
| django_template            | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 306 us: 1.00x faster                                                  |
| json                       | 5.02 ms                                                | 5.11 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 200 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.80 ms: 1.09x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.8 ms: 1.15x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.52 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.97 ms: 1.80x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.52x slower                                                  |
| telco                      | 6.53 ms                                                | 155 ms: 23.81x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): sympy_expand, asyncio_websockets, nbody
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x