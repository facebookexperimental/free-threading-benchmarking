# Results vs. 3.12.6

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.077x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 631 ms: 1.76x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.72x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.4 ms: 1.13x faster                                                  |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| nbody          | 89.3 ms                                                | 92.6 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                   |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 222 us: 1.01x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.7 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 322 us: 1.05x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.64 ms: 1.21x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.6 ms: 1.05x slower                                                  |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 631 ms: 1.76x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 324 ms: 1.72x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 265 ms: 1.69x faster                                                   |
| async_tree_none            | 464 ms                                                 | 282 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.7 us: 1.36x faster                                                  |
| deepcopy                   | 352 us                                                 | 262 us: 1.34x faster                                                   |
| go                         | 139 ms                                                 | 114 ms: 1.22x faster                                                   |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.69 us: 1.14x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.9 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 71.4 ms: 1.13x faster                                                  |
| scimark_sor                | 130 ms                                                 | 115 ms: 1.13x faster                                                   |
| spectral_norm              | 110 ms                                                 | 98.0 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.9 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 287 ms: 1.11x faster                                                   |
| generators                 | 32.2 ms                                                | 29.2 ms: 1.10x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 69.7 ms: 1.10x faster                                                  |
| regex_compile              | 142 ms                                                 | 130 ms: 1.09x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                 |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 132 ms: 1.08x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 63.8 ms: 1.07x faster                                                  |
| pyflate                    | 448 ms                                                 | 420 ms: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                   |
| scimark_fft                | 342 ms                                                 | 321 ms: 1.07x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.24 us: 1.06x faster                                                  |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.6 ms: 1.06x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.6 ms: 1.05x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 159 ms: 1.04x faster                                                   |
| sympy_str                  | 292 ms                                                 | 281 ms: 1.04x faster                                                   |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                  |
| richards                   | 45.9 ms                                                | 44.5 ms: 1.03x faster                                                  |
| richards_super             | 51.9 ms                                                | 50.3 ms: 1.03x faster                                                  |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.36 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 732 ms: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 4.96 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                  |
| hexiom                     | 6.17 ms                                                | 6.12 ms: 1.01x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 471 ms: 1.01x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 222 us: 1.01x slower                                                   |
| nqueens                    | 80.1 ms                                                | 80.8 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.03x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                   |
| nbody                      | 89.3 ms                                                | 92.6 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.05x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 322 us: 1.05x slower                                                   |
| django_template            | 34.7 ms                                                | 36.6 ms: 1.05x slower                                                  |
| fannkuch                   | 372 ms                                                 | 396 ms: 1.06x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.09x slower                                                  |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.29 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.9 ms: 1.12x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.06 ms: 1.12x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.64 ms: 1.21x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.26 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.9 ms: 8.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (5): typing_runtime_protocols, xml_etree_generate, pycparser, asyncio_websockets, scimark_sparse_mat_mult
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-f0dcb29/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.12x