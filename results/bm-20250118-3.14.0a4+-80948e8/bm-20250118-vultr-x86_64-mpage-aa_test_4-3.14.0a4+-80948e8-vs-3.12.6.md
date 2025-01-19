# Results vs. 3.12.6

- fork: mpage
- ref: aa_test_4
- machine: linux-x86_64
- commit hash: 80948e8
- commit date: 2025-01-18
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.04x faster                                       |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                       |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                       |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 326 ms: 1.70x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 492 ms: 1.45x faster                                       |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                       |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.50x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.1 ms: 1.14x faster                                      |
| nbody          | 89.3 ms                                                | 87.4 ms: 1.02x faster                                      |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                  | 1.04x faster                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                      |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                       |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                       |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.11x faster                                     |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                      |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                       |
| xml_etree_generate   | 85.2 ms                                                | 84.3 ms: 1.01x faster                                      |
| pickle_pure_python   | 308 us                                                 | 310 us: 1.01x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 59.5 ms: 1.01x slower                                      |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                      |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                      |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                      |
| Geometric mean         | (ref)                                                  | 1.23x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.1 ms: 1.08x faster                                      |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                      |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                      |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                      |
| Geometric mean  | (ref)                                                  | 1.01x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                       |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                       |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 326 ms: 1.70x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 492 ms: 1.45x faster                                       |
| deepcopy                   | 352 us                                                 | 260 us: 1.35x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 30.1 us: 1.34x faster                                      |
| spectral_norm              | 110 ms                                                 | 88.1 ms: 1.25x faster                                      |
| go                         | 139 ms                                                 | 113 ms: 1.23x faster                                       |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                      |
| crypto_pyaes               | 76.6 ms                                                | 65.1 ms: 1.18x faster                                      |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.17x faster                                      |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                       |
| chaos                      | 62.8 ms                                                | 54.3 ms: 1.16x faster                                      |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                       |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                      |
| float                      | 80.8 ms                                                | 71.1 ms: 1.14x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                      |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                       |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                       |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.11x faster                                     |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                       |
| deltablue                  | 3.45 ms                                                | 3.11 ms: 1.11x faster                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                      |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                       |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                      |
| richards                   | 45.9 ms                                                | 42.3 ms: 1.09x faster                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                      |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                       |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 63.3 ms: 1.08x faster                                      |
| hexiom                     | 6.17 ms                                                | 5.74 ms: 1.07x faster                                      |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                       |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                      |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                     |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                       |
| richards_super             | 51.9 ms                                                | 48.8 ms: 1.06x faster                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                      |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                       |
| thrift                     | 791 us                                                 | 748 us: 1.06x faster                                       |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                       |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                     |
| logging_format             | 7.35 us                                                | 6.99 us: 1.05x faster                                      |
| meteor_contest             | 104 ms                                                 | 98.6 ms: 1.05x faster                                      |
| dulwich_log                | 78.9 ms                                                | 75.4 ms: 1.05x faster                                      |
| 2to3                       | 264 ms                                                 | 252 ms: 1.04x faster                                       |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                      |
| mdp                        | 2.42 sec                                               | 2.33 sec: 1.04x faster                                     |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                      |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                       |
| nqueens                    | 80.1 ms                                                | 77.9 ms: 1.03x faster                                      |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                     |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.02x faster                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.29 ms: 1.02x faster                                      |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                       |
| nbody                      | 89.3 ms                                                | 87.4 ms: 1.02x faster                                      |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                       |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                      |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                       |
| sqlglot_optimize           | 53.3 ms                                                | 52.6 ms: 1.01x faster                                      |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                       |
| xml_etree_generate         | 85.2 ms                                                | 84.3 ms: 1.01x faster                                      |
| pickle_pure_python         | 308 us                                                 | 310 us: 1.01x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 59.5 ms: 1.01x slower                                      |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                       |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.42 ms: 1.04x slower                                      |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                      |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                       |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                      |
| telco                      | 6.53 ms                                                | 7.13 ms: 1.09x slower                                      |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                      |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                      |
| coverage                   | 71.4 ms                                                | 80.7 ms: 1.13x slower                                      |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.17x slower                                      |
| gc_traversal               | 3.46 ms                                                | 4.28 ms: 1.24x slower                                      |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 88.1 ms: 8.16x slower                                      |
| Geometric mean             | (ref)                                                  | 1.07x faster                                               |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250118-3.14.0a4+-80948e8/bm-20250118-vultr-x86_64-mpage-aa_test_4-3.14.0a4+-80948e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x