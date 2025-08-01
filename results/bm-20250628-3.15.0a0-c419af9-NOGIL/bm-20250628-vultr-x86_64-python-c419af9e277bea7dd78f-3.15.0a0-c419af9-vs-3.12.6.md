# Results vs. 3.12.6

- fork: python
- ref: c419af9e277bea7dd78f
- machine: linux-x86_64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.023x faster
- HPT reliability: 85.54%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 462 ms: 1.57x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| nbody          | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_dna      | 168 ms                                                 | 163 ms: 1.03x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.6 ms: 1.12x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.0 ms: 1.11x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.3 ms: 1.13x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 58.2 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 519 ms: 2.14x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.92 ms: 1.80x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 462 ms: 1.57x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| deepcopy                   | 352 us                                                 | 295 us: 1.19x faster                                                  |
| float                      | 80.8 ms                                                | 69.7 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.8 us: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.4 us: 1.14x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.6 ms: 1.12x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.6 ms: 1.10x faster                                                 |
| generators                 | 32.2 ms                                                | 29.5 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.36 sec: 1.09x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                                 |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 124 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| regex_dna                  | 168 ms                                                 | 163 ms: 1.03x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.04 us: 1.01x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.1 ms: 1.00x slower                                                 |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                                  |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib                   | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.34 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 461 ms: 1.03x slower                                                  |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 778 ms: 1.05x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 21.8 ms: 1.06x slower                                                 |
| sympy_str                  | 292 ms                                                 | 310 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.35 ms: 1.06x slower                                                 |
| scimark_fft                | 342 ms                                                 | 366 ms: 1.07x slower                                                  |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.89 us: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.08x slower                                                  |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 874 us: 1.10x slower                                                  |
| sympy_expand               | 468 ms                                                 | 517 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.0 ms: 1.11x slower                                                 |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.9 ms: 1.12x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| django_template            | 34.7 ms                                                | 39.3 ms: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.0 ms: 1.16x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 58.2 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.25 ms: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                                  |
| telco                      | 6.53 ms                                                | 8.45 ms: 1.29x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.36x slower                                                 |
| nbody                      | 89.3 ms                                                | 123 ms: 1.38x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 104 ms: 9.66x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): deltablue
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 85.54% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x