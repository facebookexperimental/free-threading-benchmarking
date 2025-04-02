# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.082x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 312 ms: 1.18x slower                                                   |
| docutils       | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                 |
| html5lib       | 63.6 ms                                                | 76.0 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                                   |
| async_generators           | 384 ms                                                 | 392 ms: 1.02x slower                                                   |
| coroutines                 | 23.9 ms                                                | 26.9 ms: 1.12x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.6 ms: 1.04x faster                                                  |
| pidigits       | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| nbody          | 89.3 ms                                                | 139 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                   |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 94.1 ms: 1.03x faster                                                  |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.57 sec: 1.22x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 272 us: 1.23x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 387 us: 1.26x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.3 ms: 1.29x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.61x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 45.5 ms: 1.31x slower                                                  |
| genshi_xml      | 50.2 ms                                                | 67.5 ms: 1.34x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                  |
| mako            | 11.0 ms                                                | 16.7 ms: 1.51x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.47 sec: 1.65x faster                                                 |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 344 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 498 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 530 ms: 1.35x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                  |
| deepcopy                   | 352 us                                                 | 324 us: 1.09x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.0 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.09 us: 1.06x faster                                                  |
| float                      | 80.8 ms                                                | 77.6 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.1 ms: 1.03x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 78.5 ms: 1.00x faster                                                  |
| async_generators           | 384 ms                                                 | 392 ms: 1.02x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.91 sec: 1.04x slower                                                 |
| pylint                     | 319 ms                                                 | 332 ms: 1.04x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.27 us: 1.06x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                   |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.26 sec: 1.07x slower                                                 |
| spectral_norm              | 110 ms                                                 | 119 ms: 1.08x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.90 sec: 1.10x slower                                                 |
| go                         | 139 ms                                                 | 154 ms: 1.10x slower                                                   |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                                   |
| comprehensions             | 19.8 us                                                | 22.2 us: 1.12x slower                                                  |
| coroutines                 | 23.9 ms                                                | 26.9 ms: 1.12x slower                                                  |
| logging_silent             | 109 ns                                                 | 124 ns: 1.14x slower                                                   |
| raytrace                   | 299 ms                                                 | 340 ms: 1.14x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 166 ms: 1.16x slower                                                   |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 25.4 ms: 1.17x slower                                                  |
| pidigits                   | 184 ms                                                 | 215 ms: 1.17x slower                                                   |
| chaos                      | 62.8 ms                                                | 73.5 ms: 1.17x slower                                                  |
| scimark_sor                | 130 ms                                                 | 153 ms: 1.18x slower                                                   |
| 2to3                       | 264 ms                                                 | 312 ms: 1.18x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 880 ms: 1.18x slower                                                   |
| pyflate                    | 448 ms                                                 | 531 ms: 1.19x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.5 ms: 1.19x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 198 ms: 1.19x slower                                                   |
| html5lib                   | 63.6 ms                                                | 76.0 ms: 1.20x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 91.6 ms: 1.20x slower                                                  |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.83 sec: 1.21x slower                                                 |
| sympy_str                  | 292 ms                                                 | 354 ms: 1.22x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.57 sec: 1.22x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 84.2 ms: 1.23x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 272 us: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.44 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 387 us: 1.26x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                   |
| sympy_expand               | 468 ms                                                 | 593 ms: 1.27x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 75.0 ms: 1.27x slower                                                  |
| nqueens                    | 80.1 ms                                                | 102 ms: 1.27x slower                                                   |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.29x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.3 ms: 1.29x slower                                                  |
| logging_simple             | 6.63 us                                                | 8.58 us: 1.29x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.50 ms: 1.31x slower                                                  |
| hexiom                     | 6.17 ms                                                | 8.09 ms: 1.31x slower                                                  |
| django_template            | 34.7 ms                                                | 45.5 ms: 1.31x slower                                                  |
| richards                   | 45.9 ms                                                | 60.9 ms: 1.33x slower                                                  |
| logging_format             | 7.35 us                                                | 9.75 us: 1.33x slower                                                  |
| richards_super             | 51.9 ms                                                | 69.1 ms: 1.33x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 67.5 ms: 1.34x slower                                                  |
| telco                      | 6.53 ms                                                | 8.84 ms: 1.35x slower                                                  |
| generators                 | 32.2 ms                                                | 44.3 ms: 1.38x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.7 ms: 1.39x slower                                                  |
| fannkuch                   | 372 ms                                                 | 519 ms: 1.39x slower                                                   |
| mako                       | 11.0 ms                                                | 16.7 ms: 1.51x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                   |
| nbody                      | 89.3 ms                                                | 139 ms: 1.56x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.61x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.20 ms: 3.40x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.7 ms: 9.14x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, deepcopy_memo
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.38x