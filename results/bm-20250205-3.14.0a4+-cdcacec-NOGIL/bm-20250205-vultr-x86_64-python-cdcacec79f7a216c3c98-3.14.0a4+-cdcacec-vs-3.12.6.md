# Results vs. 3.12.6

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.042x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                 |
| html5lib       | 63.6 ms                                                | 71.9 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 564 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                  |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                   |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                   |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 244 us: 1.11x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                  |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.0 ms: 1.16x slower                                                  |
| django_template | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                  |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.75 ms: 1.97x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 564 ms: 1.97x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 596 ms: 1.82x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 501 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                                   |
| deepcopy                   | 352 us                                                 | 306 us: 1.15x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 37.7 us: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.64 sec: 1.02x faster                                                 |
| generators                 | 32.2 ms                                                | 32.0 ms: 1.01x faster                                                  |
| go                         | 139 ms                                                 | 138 ms: 1.01x faster                                                   |
| comprehensions             | 19.8 us                                                | 19.7 us: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| scimark_sor                | 130 ms                                                 | 130 ms: 1.00x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.14 us: 1.02x slower                                                  |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.5 ms: 1.05x slower                                                  |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                   |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.38 ms: 1.07x slower                                                  |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                   |
| chaos                      | 62.8 ms                                                | 68.1 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 805 ms: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.19 us: 1.09x slower                                                  |
| pyflate                    | 448 ms                                                 | 489 ms: 1.09x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 244 us: 1.11x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                   |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 119 ms: 1.12x slower                                                   |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                                   |
| logging_format             | 7.35 us                                                | 8.28 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 893 us: 1.13x slower                                                   |
| html5lib                   | 63.6 ms                                                | 71.9 ms: 1.13x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 60.7 ms: 1.14x slower                                                  |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                   |
| 2to3                       | 264 ms                                                 | 302 ms: 1.15x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.0 ms: 1.16x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.3 ms: 1.16x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                  |
| sympy_expand               | 468 ms                                                 | 549 ms: 1.17x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.19x slower                                                  |
| django_template            | 34.7 ms                                                | 41.3 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 81.6 ms: 1.19x slower                                                  |
| nqueens                    | 80.1 ms                                                | 95.6 ms: 1.19x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                  |
| richards                   | 45.9 ms                                                | 55.5 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                  |
| richards_super             | 51.9 ms                                                | 64.2 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.54 ms: 1.26x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                                  |
| telco                      | 6.53 ms                                                | 8.42 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 484 ms: 1.30x slower                                                   |
| deltablue                  | 3.45 ms                                                | 4.63 ms: 1.34x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.62 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 96.5 ms: 1.35x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                  |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 94.8 ms: 8.78x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.35x