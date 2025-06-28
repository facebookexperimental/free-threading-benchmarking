# Results vs. 3.12.6

- fork: python
- ref: c419af9e277bea7dd78f
- machine: linux-x86_64
- commit hash: c419af9
- commit date: 2025-06-28
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 61.4 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 517 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 519 ms: 1.38x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.1 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 58.1 ms: 1.01x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 628 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.76x faster                                                  |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                  |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 517 ms: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 519 ms: 1.38x faster                                                  |
| go                         | 139 ms                                                 | 103 ms: 1.35x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.4 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                  |
| logging_silent             | 109 ns                                                 | 93.6 ns: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 278 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                                |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| spectral_norm              | 110 ms                                                 | 97.3 ms: 1.13x faster                                                 |
| richards                   | 45.9 ms                                                | 40.6 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.1 ms: 1.12x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.3 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.5 ms: 1.11x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.6 ms: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.65 us: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                  |
| thrift                     | 791 us                                                 | 728 us: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 691 ms: 1.08x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.06x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 92.3 ms: 1.05x faster                                                 |
| nqueens                    | 80.1 ms                                                | 76.4 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.4 ms: 1.04x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.4 ms: 1.04x faster                                                 |
| scimark_fft                | 342 ms                                                 | 332 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.1 ms: 1.01x faster                                                 |
| django_template            | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                 |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                 |
| telco                      | 6.53 ms                                                | 7.16 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.89 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.51 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 98.8 ms: 9.15x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (4): json, pickle_pure_python, asyncio_websockets, nbody
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x