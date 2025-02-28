# Results vs. 3.12.6

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                   |
| async_generators           | 384 ms                                                 | 322 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.1 ms: 1.13x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                  |
| nbody          | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 303 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.4 ms: 1.06x faster                                                  |
| django_template | 34.7 ms                                                | 32.9 ms: 1.05x faster                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 602 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 472 ms: 1.53x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                   |
| deepcopy                   | 352 us                                                 | 244 us: 1.44x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.2 us: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 110 ms: 1.26x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                  |
| spectral_norm              | 110 ms                                                 | 90.6 ms: 1.22x faster                                                  |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                                  |
| async_generators           | 384 ms                                                 | 322 ms: 1.20x faster                                                   |
| raytrace                   | 299 ms                                                 | 253 ms: 1.18x faster                                                   |
| pylint                     | 319 ms                                                 | 273 ms: 1.16x faster                                                   |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.2 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                   |
| chaos                      | 62.8 ms                                                | 54.5 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.02 ms: 1.14x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.1 ms: 1.13x faster                                                  |
| float                      | 80.8 ms                                                | 71.5 ms: 1.13x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.91 us: 1.12x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                  |
| pyflate                    | 448 ms                                                 | 403 ms: 1.11x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 150 ms: 1.11x faster                                                   |
| thrift                     | 791 us                                                 | 715 us: 1.11x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.38 sec: 1.10x faster                                                 |
| richards                   | 45.9 ms                                                | 41.9 ms: 1.10x faster                                                  |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 681 ms: 1.09x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.09x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.9 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.08x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.70 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.9 ms: 1.07x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                   |
| sqlglot_normalize          | 107 ms                                                 | 99.8 ms: 1.07x faster                                                  |
| meteor_contest             | 104 ms                                                 | 97.1 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 47.4 ms: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| mdp                        | 2.42 sec                                               | 2.29 sec: 1.06x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 74.7 ms: 1.06x faster                                                  |
| django_template            | 34.7 ms                                                | 32.9 ms: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 50.7 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.26 ms: 1.03x faster                                                  |
| scimark_fft                | 342 ms                                                 | 331 ms: 1.03x faster                                                   |
| xml_etree_process          | 59.0 ms                                                | 57.3 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 82.8 ms: 1.03x faster                                                  |
| fannkuch                   | 372 ms                                                 | 363 ms: 1.03x faster                                                   |
| nbody                      | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.92 ms: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 303 us: 1.01x faster                                                   |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| telco                      | 6.53 ms                                                | 7.15 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.46 ms: 1.29x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.49x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.1 ms: 8.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.11x