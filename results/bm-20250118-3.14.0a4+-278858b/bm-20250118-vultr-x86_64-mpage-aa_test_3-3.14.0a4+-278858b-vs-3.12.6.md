# Results vs. 3.12.6

- fork: mpage
- ref: aa_test_3
- machine: linux-x86_64
- commit hash: 278858b
- commit date: 2025-01-18
- overall geometric mean: 1.083x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                       |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.02x faster                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                       |
| async_tree_io              | 1.08 sec                                               | 615 ms: 1.76x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                       |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                       |
| async_generators           | 384 ms                                                 | 329 ms: 1.17x faster                                       |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                      |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| Geometric mean             | (ref)                                                  | 1.49x faster                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.2 ms: 1.10x faster                                      |
| nbody          | 89.3 ms                                                | 87.8 ms: 1.02x faster                                      |
| pidigits       | 184 ms                                                 | 214 ms: 1.16x slower                                       |
| Geometric mean | (ref)                                                  | 1.01x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                      |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                     |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                      |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.02x faster                                       |
| xml_etree_generate   | 85.2 ms                                                | 84.6 ms: 1.01x faster                                      |
| xml_etree_process    | 59.0 ms                                                | 59.7 ms: 1.01x slower                                      |
| pickle_pure_python   | 308 us                                                 | 316 us: 1.03x slower                                       |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                      |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                      |
| Geometric mean       | (ref)                                                  | 1.01x faster                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                      |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| Geometric mean         | (ref)                                                  | 1.24x slower                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.5 ms: 1.06x faster                                      |
| genshi_xml      | 50.2 ms                                                | 49.0 ms: 1.02x faster                                      |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                      |
| mako            | 11.0 ms                                                | 11.7 ms: 1.07x slower                                      |
| Geometric mean  | (ref)                                                  | 1.00x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                       |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                       |
| async_tree_io              | 1.08 sec                                               | 615 ms: 1.76x faster                                       |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                       |
| async_tree_none            | 464 ms                                                 | 273 ms: 1.70x faster                                       |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                       |
| deepcopy                   | 352 us                                                 | 259 us: 1.36x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 30.7 us: 1.31x faster                                      |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                       |
| comprehensions             | 19.8 us                                                | 16.9 us: 1.18x faster                                      |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                      |
| async_generators           | 384 ms                                                 | 329 ms: 1.17x faster                                       |
| spectral_norm              | 110 ms                                                 | 95.1 ms: 1.16x faster                                      |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                      |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                      |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                       |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                       |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                       |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                      |
| raytrace                   | 299 ms                                                 | 268 ms: 1.12x faster                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                     |
| chaos                      | 62.8 ms                                                | 56.8 ms: 1.11x faster                                      |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                       |
| coroutines                 | 23.9 ms                                                | 21.7 ms: 1.10x faster                                      |
| float                      | 80.8 ms                                                | 73.2 ms: 1.10x faster                                      |
| deltablue                  | 3.45 ms                                                | 3.16 ms: 1.09x faster                                      |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                       |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                       |
| richards                   | 45.9 ms                                                | 42.5 ms: 1.08x faster                                      |
| logging_format             | 7.35 us                                                | 6.81 us: 1.08x faster                                      |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                       |
| logging_simple             | 6.63 us                                                | 6.19 us: 1.07x faster                                      |
| scimark_fft                | 342 ms                                                 | 320 ms: 1.07x faster                                       |
| hexiom                     | 6.17 ms                                                | 5.79 ms: 1.06x faster                                      |
| genshi_text                | 22.8 ms                                                | 21.5 ms: 1.06x faster                                      |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.06x faster                                      |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                       |
| thrift                     | 791 us                                                 | 745 us: 1.06x faster                                       |
| richards_super             | 51.9 ms                                                | 48.8 ms: 1.06x faster                                      |
| pyflate                    | 448 ms                                                 | 422 ms: 1.06x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.58 ms: 1.05x faster                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 65.1 ms: 1.05x faster                                      |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                     |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                     |
| dulwich_log                | 78.9 ms                                                | 75.6 ms: 1.04x faster                                      |
| pprint_safe_repr           | 743 ms                                                 | 715 ms: 1.04x faster                                       |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                       |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                       |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                      |
| mdp                        | 2.42 sec                                               | 2.35 sec: 1.03x faster                                     |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.02x faster                                     |
| genshi_xml                 | 50.2 ms                                                | 49.0 ms: 1.02x faster                                      |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.02x faster                                       |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                       |
| nbody                      | 89.3 ms                                                | 87.8 ms: 1.02x faster                                      |
| nqueens                    | 80.1 ms                                                | 78.8 ms: 1.02x faster                                      |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.01x faster                                      |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                       |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                       |
| xml_etree_generate         | 85.2 ms                                                | 84.6 ms: 1.01x faster                                      |
| sqlglot_optimize           | 53.3 ms                                                | 52.9 ms: 1.01x faster                                      |
| sqlglot_normalize          | 107 ms                                                 | 106 ms: 1.01x faster                                       |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                      |
| django_template            | 34.7 ms                                                | 35.4 ms: 1.02x slower                                      |
| pickle_pure_python         | 308 us                                                 | 316 us: 1.03x slower                                       |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                      |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.07x slower                                      |
| telco                      | 6.53 ms                                                | 7.19 ms: 1.10x slower                                      |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                      |
| json_dumps                 | 10.4 ms                                                | 11.6 ms: 1.12x slower                                      |
| coverage                   | 71.4 ms                                                | 80.4 ms: 1.13x slower                                      |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                      |
| pidigits                   | 184 ms                                                 | 214 ms: 1.16x slower                                       |
| gc_traversal               | 3.46 ms                                                | 4.28 ms: 1.24x slower                                      |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                      |
| bench_mp_pool              | 10.8 ms                                                | 88.7 ms: 8.21x slower                                      |
| Geometric mean             | (ref)                                                  | 1.05x faster                                               |

Benchmark hidden because not significant (4): scimark_sparse_mat_mult, json, regex_dna, fannkuch
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250118-3.14.0a4+-278858b/bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4+-278858b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x