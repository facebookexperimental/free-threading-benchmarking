# Results vs. 3.12.6

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.078x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 314 ms: 1.19x slower                                                   |
| docutils       | 2.64 sec                                               | 2.86 sec: 1.08x slower                                                 |
| html5lib       | 63.6 ms                                                | 74.3 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.9 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 198 ms: 1.08x slower                                                   |
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| regex_compile  | 142 ms                                                 | 159 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.9 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.45 sec: 1.16x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 279 us: 1.26x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 393 us: 1.28x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.2 ms: 1.28x slower                                                  |
| django_template | 34.7 ms                                                | 45.2 ms: 1.30x slower                                                  |
| genshi_text     | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                  |
| mako            | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.34x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 584 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                   |
| async_tree_none            | 464 ms                                                 | 286 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.9 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| deepcopy                   | 352 us                                                 | 328 us: 1.07x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.35 ms: 1.03x faster                                                  |
| float                      | 80.8 ms                                                | 78.9 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                   |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.83 sec: 1.02x slower                                                 |
| generators                 | 32.2 ms                                                | 33.2 ms: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 144 ms: 1.04x slower                                                   |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.24 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                  |
| scimark_sor                | 130 ms                                                 | 139 ms: 1.07x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 84.8 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 198 ms: 1.08x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.86 sec: 1.08x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.62 sec: 1.08x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.36 us: 1.09x slower                                                  |
| comprehensions             | 19.8 us                                                | 21.7 us: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| regex_compile              | 142 ms                                                 | 159 ms: 1.11x slower                                                   |
| logging_silent             | 109 ns                                                 | 122 ns: 1.12x slower                                                   |
| raytrace                   | 299 ms                                                 | 336 ms: 1.12x slower                                                   |
| scimark_fft                | 342 ms                                                 | 387 ms: 1.13x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                                  |
| chaos                      | 62.8 ms                                                | 71.4 ms: 1.14x slower                                                  |
| pyflate                    | 448 ms                                                 | 511 ms: 1.14x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 850 ms: 1.14x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 191 ms: 1.15x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 98.8 ms: 1.16x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.8 ms: 1.16x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.45 sec: 1.16x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 167 ms: 1.17x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 124 ms: 1.17x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.74 us: 1.17x slower                                                  |
| html5lib                   | 63.6 ms                                                | 74.3 ms: 1.17x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.97 ms: 1.18x slower                                                  |
| sympy_str                  | 292 ms                                                 | 343 ms: 1.18x slower                                                   |
| thrift                     | 791 us                                                 | 941 us: 1.19x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 63.4 ms: 1.19x slower                                                  |
| 2to3                       | 264 ms                                                 | 314 ms: 1.19x slower                                                   |
| sympy_expand               | 468 ms                                                 | 561 ms: 1.20x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.32 ms: 1.21x slower                                                  |
| logging_format             | 7.35 us                                                | 8.88 us: 1.21x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.9 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 83.3 ms: 1.22x slower                                                  |
| richards                   | 45.9 ms                                                | 56.7 ms: 1.23x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.9 ms: 1.24x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.65 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                   |
| richards_super             | 51.9 ms                                                | 65.4 ms: 1.26x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 279 us: 1.26x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.58 ms: 1.27x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 393 us: 1.28x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 64.2 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 211 us: 1.29x slower                                                   |
| django_template            | 34.7 ms                                                | 45.2 ms: 1.30x slower                                                  |
| telco                      | 6.53 ms                                                | 8.57 ms: 1.31x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.3 ms: 1.33x slower                                                  |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.4 ms: 1.36x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.75 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                  |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.55x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.34 ms: 3.55x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.8 ms: 8.87x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (3): deepcopy_memo, asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.36x