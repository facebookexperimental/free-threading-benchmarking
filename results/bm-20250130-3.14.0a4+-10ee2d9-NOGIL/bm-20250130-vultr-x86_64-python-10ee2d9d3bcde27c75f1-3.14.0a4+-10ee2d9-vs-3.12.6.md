# Results vs. 3.12.6

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.050x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                                   |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 71.2 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.09x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 247 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 372 us: 1.21x slower                                                   |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.66 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                  |
| django_template | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                  |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.68 ms: 2.06x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 607 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 322 ms: 1.74x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 263 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 508 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                  |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.3 us: 1.05x faster                                                  |
| float                      | 80.8 ms                                                | 76.9 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.65 sec: 1.02x faster                                                 |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                   |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                 |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 81.9 ms: 1.04x slower                                                  |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                                  |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                                   |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.09x slower                                                 |
| raytrace                   | 299 ms                                                 | 327 ms: 1.09x slower                                                   |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| chaos                      | 62.8 ms                                                | 68.8 ms: 1.10x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.66 sec: 1.10x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 817 ms: 1.10x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.35 us: 1.11x slower                                                  |
| pyflate                    | 448 ms                                                 | 498 ms: 1.11x slower                                                   |
| scimark_fft                | 342 ms                                                 | 380 ms: 1.11x slower                                                   |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                                   |
| html5lib                   | 63.6 ms                                                | 71.2 ms: 1.12x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 247 us: 1.12x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                   |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 902 us: 1.14x slower                                                   |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.1 ms: 1.15x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.1 ms: 1.15x slower                                                  |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                                   |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.16x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.1 ms: 1.17x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.20x slower                                                   |
| hexiom                     | 6.17 ms                                                | 7.40 ms: 1.20x slower                                                  |
| nqueens                    | 80.1 ms                                                | 96.2 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 82.5 ms: 1.21x slower                                                  |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 372 us: 1.21x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                   |
| django_template            | 34.7 ms                                                | 42.6 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                  |
| richards                   | 45.9 ms                                                | 57.2 ms: 1.24x slower                                                  |
| richards_super             | 51.9 ms                                                | 65.2 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.41 ms: 1.29x slower                                                  |
| fannkuch                   | 372 ms                                                 | 487 ms: 1.31x slower                                                   |
| telco                      | 6.53 ms                                                | 8.57 ms: 1.31x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.66 ms: 1.35x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.67 ms: 1.35x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.3 ms: 1.36x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 92.6 ms: 8.57x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                           |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, go
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x