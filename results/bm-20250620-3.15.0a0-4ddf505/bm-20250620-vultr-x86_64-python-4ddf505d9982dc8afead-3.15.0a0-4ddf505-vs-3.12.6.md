# Results vs. 3.12.6

- fork: python
- ref: 4ddf505d9982dc8afead
- machine: linux-x86_64
- commit hash: 4ddf505
- commit date: 2025-06-20
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                 |
| nbody          | 89.3 ms                                                | 88.5 ms: 1.01x faster                                                 |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 175 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| mako           | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 609 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 509 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                 |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                  |
| go                         | 139 ms                                                 | 103 ms: 1.36x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 250 ms: 1.20x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.9 ms: 1.18x faster                                                 |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                                 |
| async_generators           | 384 ms                                                 | 332 ms: 1.16x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| pyflate                    | 448 ms                                                 | 391 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.4 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.15 sec: 1.14x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 67.2 ms: 1.14x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 60.2 ms: 1.14x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.4 ms: 1.13x faster                                                 |
| float                      | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                 |
| richards                   | 45.9 ms                                                | 40.8 ms: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.5 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.6 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                 |
| sympy_str                  | 292 ms                                                 | 267 ms: 1.09x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.65 ms: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.20 ms: 1.08x faster                                                 |
| thrift                     | 791 us                                                 | 736 us: 1.08x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| sympy_expand               | 468 ms                                                 | 445 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.8 ms: 1.05x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.2 ms: 1.04x faster                                                 |
| scimark_fft                | 342 ms                                                 | 330 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.48 us: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                 |
| logging_format             | 7.35 us                                                | 7.27 us: 1.01x faster                                                 |
| nbody                      | 89.3 ms                                                | 88.5 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 374 ms: 1.00x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.15 ms: 1.02x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 764 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.56 sec: 1.03x slower                                                |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.70 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| telco                      | 6.53 ms                                                | 7.19 ms: 1.10x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.38 ms: 1.27x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.91 ms: 1.75x slower                                                 |
| logging_silent             | 109 ns                                                 | 464 ns: 4.26x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 99.4 ms: 9.21x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (3): django_template, asyncio_websockets, pickle_pure_python
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x