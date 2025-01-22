# Results vs. 3.12.6

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 313 ms: 1.19x slower                                                   |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| html5lib       | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 569 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                   |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.2 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                                   |
| nbody          | 89.3 ms                                                | 137 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| regex_compile  | 142 ms                                                 | 159 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.43 sec: 1.15x slower                                                 |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.9 ms: 1.16x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 280 us: 1.27x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 75.3 ms: 1.28x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 395 us: 1.28x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                  |
| django_template | 34.7 ms                                                | 44.8 ms: 1.29x slower                                                  |
| genshi_text     | 22.8 ms                                                | 29.8 ms: 1.30x slower                                                  |
| mako            | 11.0 ms                                                | 16.3 ms: 1.48x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 569 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                                  |
| deepcopy                   | 352 us                                                 | 323 us: 1.09x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                  |
| float                      | 80.8 ms                                                | 77.2 ms: 1.05x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.37 ms: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 39.9 us: 1.01x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.80 sec: 1.01x slower                                                 |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                   |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 84.5 ms: 1.07x slower                                                  |
| comprehensions             | 19.8 us                                                | 21.4 us: 1.08x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                                 |
| scimark_sor                | 130 ms                                                 | 140 ms: 1.08x slower                                                   |
| logging_silent             | 109 ns                                                 | 118 ns: 1.08x slower                                                   |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.38 us: 1.10x slower                                                  |
| raytrace                   | 299 ms                                                 | 334 ms: 1.12x slower                                                   |
| regex_compile              | 142 ms                                                 | 159 ms: 1.12x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| pyflate                    | 448 ms                                                 | 504 ms: 1.13x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.7 ms: 1.13x slower                                                  |
| chaos                      | 62.8 ms                                                | 71.6 ms: 1.14x slower                                                  |
| html5lib                   | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 191 ms: 1.15x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.43 sec: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.79 sec: 1.15x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 123 ms: 1.16x slower                                                   |
| scimark_fft                | 342 ms                                                 | 395 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 861 ms: 1.16x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 166 ms: 1.16x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.9 ms: 1.16x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.95 ms: 1.17x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.78 sec: 1.17x slower                                                 |
| sympy_str                  | 292 ms                                                 | 343 ms: 1.18x slower                                                   |
| pidigits                   | 184 ms                                                 | 217 ms: 1.18x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 63.1 ms: 1.18x slower                                                  |
| thrift                     | 791 us                                                 | 939 us: 1.19x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.87 us: 1.19x slower                                                  |
| 2to3                       | 264 ms                                                 | 313 ms: 1.19x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.62 ms: 1.19x slower                                                  |
| sympy_expand               | 468 ms                                                 | 565 ms: 1.21x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.8 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 83.2 ms: 1.22x slower                                                  |
| logging_format             | 7.35 us                                                | 8.99 us: 1.22x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.60 ms: 1.23x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.8 ms: 1.23x slower                                                  |
| richards                   | 45.9 ms                                                | 56.9 ms: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 63.0 ms: 1.26x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                  |
| richards_super             | 51.9 ms                                                | 65.7 ms: 1.27x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 280 us: 1.27x slower                                                   |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 75.3 ms: 1.28x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 395 us: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.64 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 210 us: 1.29x slower                                                   |
| django_template            | 34.7 ms                                                | 44.8 ms: 1.29x slower                                                  |
| genshi_text                | 22.8 ms                                                | 29.8 ms: 1.30x slower                                                  |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                   |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.77 ms: 1.38x slower                                                  |
| coverage                   | 71.4 ms                                                | 98.9 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 16.3 ms: 1.48x slower                                                  |
| nbody                      | 89.3 ms                                                | 137 ms: 1.54x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.35 ms: 3.56x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.7 ms: 8.87x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.36x