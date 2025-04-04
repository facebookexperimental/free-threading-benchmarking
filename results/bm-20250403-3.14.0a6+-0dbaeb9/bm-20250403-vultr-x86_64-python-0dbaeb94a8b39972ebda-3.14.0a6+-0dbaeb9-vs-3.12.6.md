# Results vs. 3.12.6

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.070x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 332 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 271 ms: 1.65x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 516 ms: 1.39x faster                                                   |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| nbody          | 89.3 ms                                                | 92.5 ms: 1.04x slower                                                  |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 94.3 ms: 1.03x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 223 us: 1.01x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                  |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 61.4 ms: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.04x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.72 ms: 1.22x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.7 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.8 ms: 1.06x slower                                                  |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 630 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 332 ms: 1.69x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 271 ms: 1.65x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 516 ms: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                  |
| deepcopy                   | 352 us                                                 | 262 us: 1.34x faster                                                   |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| raytrace                   | 299 ms                                                 | 257 ms: 1.17x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.2 us: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.6 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 336 ms: 1.14x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.70 us: 1.14x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                  |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| spectral_norm              | 110 ms                                                 | 98.5 ms: 1.12x faster                                                  |
| chaos                      | 62.8 ms                                                | 56.2 ms: 1.12x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| pylint                     | 319 ms                                                 | 289 ms: 1.10x faster                                                   |
| regex_compile              | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 70.9 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                 |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| pyflate                    | 448 ms                                                 | 419 ms: 1.07x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.21 us: 1.07x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 134 ms: 1.06x faster                                                   |
| logging_format             | 7.35 us                                                | 6.94 us: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| scimark_fft                | 342 ms                                                 | 325 ms: 1.05x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.01 sec: 1.05x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.8 ms: 1.05x faster                                                  |
| richards                   | 45.9 ms                                                | 44.1 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                  |
| generators                 | 32.2 ms                                                | 31.1 ms: 1.04x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 160 ms: 1.04x faster                                                   |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                   |
| sympy_str                  | 292 ms                                                 | 283 ms: 1.03x faster                                                   |
| genshi_text                | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                  |
| richards_super             | 51.9 ms                                                | 50.5 ms: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.90 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.3 ms: 1.03x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.36 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                 |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 162 us: 1.01x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.52 sec: 1.00x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 50.7 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 223 us: 1.01x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                  |
| nqueens                    | 80.1 ms                                                | 81.7 ms: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 118 ms: 1.03x slower                                                   |
| nbody                      | 89.3 ms                                                | 92.5 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 61.4 ms: 1.04x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                   |
| fannkuch                   | 372 ms                                                 | 395 ms: 1.06x slower                                                   |
| django_template            | 34.7 ms                                                | 36.8 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.69 ms: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 80.3 ms: 1.12x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.06 ms: 1.13x slower                                                  |
| telco                      | 6.53 ms                                                | 7.45 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 8.72 ms: 1.22x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.64 ms: 1.34x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 89.7 ms: 8.30x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (5): sqlite_synth, pprint_safe_repr, asyncio_websockets, hexiom, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x