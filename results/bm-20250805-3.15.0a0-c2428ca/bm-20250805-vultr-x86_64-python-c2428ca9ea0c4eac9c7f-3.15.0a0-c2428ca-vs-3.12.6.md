# Results vs. 3.12.6

- fork: python
- ref: c2428ca9ea0c4eac9c7f
- machine: linux-x86_64
- commit hash: c2428ca
- commit date: 2025-08-05
- overall geometric mean: 1.065x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.1 ms: 1.14x faster                                                 |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.3 ms: 1.01x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.8 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                 |
| mako           | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 610 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                                  |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.8 us: 1.31x faster                                                 |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                                 |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                  |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.4 ms: 1.19x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| async_generators           | 384 ms                                                 | 335 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                                 |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.83 us: 1.14x faster                                                 |
| float                      | 80.8 ms                                                | 71.1 ms: 1.14x faster                                                 |
| logging_format             | 7.35 us                                                | 6.46 us: 1.14x faster                                                 |
| logging_silent             | 109 ns                                                 | 95.9 ns: 1.14x faster                                                 |
| spectral_norm              | 110 ms                                                 | 97.2 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.7 ms: 1.12x faster                                                 |
| pyflate                    | 448 ms                                                 | 402 ms: 1.11x faster                                                  |
| richards                   | 45.9 ms                                                | 41.4 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| richards_super             | 51.9 ms                                                | 47.2 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.9 ms: 1.09x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 704 ms: 1.05x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.30 ms: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 759 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.0 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.9 ms: 1.04x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| scimark_fft                | 342 ms                                                 | 333 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.7 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.3 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.25 ms: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 380 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json                       | 5.02 ms                                                | 5.24 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.79 ms: 1.09x slower                                                 |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 82.0 ms: 1.15x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.35 ms: 1.26x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.94 ms: 1.78x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.54x slower                                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.46x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): nbody, asyncio_websockets, django_template
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x