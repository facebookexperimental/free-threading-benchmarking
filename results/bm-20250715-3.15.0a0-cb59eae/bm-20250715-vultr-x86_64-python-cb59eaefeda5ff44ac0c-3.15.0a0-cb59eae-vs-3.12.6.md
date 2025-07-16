# Results vs. 3.12.6

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: linux-x86_64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.6 ms: 1.11x faster                                                 |
| nbody          | 89.3 ms                                                | 87.8 ms: 1.02x faster                                                 |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.62 ms: 1.21x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.5 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.05x slower                                                 |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                 |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| django_template | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                  |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.3 us: 1.37x faster                                                 |
| go                         | 139 ms                                                 | 103 ms: 1.35x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.28x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.62 ms: 1.21x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.4 ms: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| generators                 | 32.2 ms                                                | 28.4 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.87 us: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 342 ms: 1.13x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.06 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 40.9 ms: 1.12x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.22 sec: 1.12x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 61.0 ms: 1.12x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.3 ms: 1.12x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.6 ms: 1.11x faster                                                 |
| float                      | 80.8 ms                                                | 72.6 ms: 1.11x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.1 ms: 1.11x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.60 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 99.0 ns: 1.10x faster                                                 |
| pyflate                    | 448 ms                                                 | 407 ms: 1.10x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                  |
| logging_format             | 7.35 us                                                | 6.77 us: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| thrift                     | 791 us                                                 | 740 us: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 707 ms: 1.05x faster                                                  |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.5 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.6 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                 |
| nbody                      | 89.3 ms                                                | 87.8 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.01x faster                                                 |
| json                       | 5.02 ms                                                | 5.13 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                 |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.03x slower                                                  |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.82 ms: 1.10x slower                                                 |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.30 ms: 1.24x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.54x slower                                                  |
| telco                      | 6.53 ms                                                | 159 ms: 24.41x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): python_startup_no_site, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x