# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 956e5d1
- commit date: 2025-04-16
- overall geometric mean: 1.031x faster
- HPT reliability: 55.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                     |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                   |
| html5lib       | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 516 ms: 2.15x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 539 ms: 2.01x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                     |
| async_tree_none            | 464 ms                                                 | 253 ms: 1.83x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.32x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                    |
| async_generators           | 384 ms                                                 | 361 ms: 1.07x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.3 ms: 1.20x faster                                                    |
| nbody          | 89.3 ms                                                | 109 ms: 1.22x slower                                                     |
| pidigits       | 184 ms                                                 | 235 ms: 1.27x slower                                                     |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                    |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                    |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 227 us: 1.03x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 325 us: 1.06x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 92.2 ms: 1.08x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 66.0 ms: 1.12x slower                                                    |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                                    |
| json_dumps           | 10.4 ms                                                | 12.5 ms: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.3 ms: 1.08x slower                                                    |
| genshi_text     | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                    |
| django_template | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                    |
| mako            | 11.0 ms                                                | 15.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 516 ms: 2.15x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 539 ms: 2.01x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 223 ms: 2.00x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.99x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                   |
| async_tree_none            | 464 ms                                                 | 253 ms: 1.83x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 516 ms: 1.40x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.32x faster                                                     |
| deepcopy                   | 352 us                                                 | 290 us: 1.22x faster                                                     |
| float                      | 80.8 ms                                                | 67.3 ms: 1.20x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 34.5 us: 1.17x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                    |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 1.98 us: 1.11x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 87.4 ms: 1.11x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                    |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.07x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                   |
| async_generators           | 384 ms                                                 | 361 ms: 1.07x faster                                                     |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                     |
| chaos                      | 62.8 ms                                                | 59.8 ms: 1.05x faster                                                    |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                                     |
| raytrace                   | 299 ms                                                 | 287 ms: 1.04x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                   |
| generators                 | 32.2 ms                                                | 31.1 ms: 1.04x faster                                                    |
| scimark_fft                | 342 ms                                                 | 334 ms: 1.02x faster                                                     |
| comprehensions             | 19.8 us                                                | 19.4 us: 1.02x faster                                                    |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.01x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 2.08 sec: 1.01x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.50 ms: 1.01x slower                                                    |
| pyflate                    | 448 ms                                                 | 455 ms: 1.02x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 763 ms: 1.03x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 227 us: 1.03x slower                                                     |
| logging_simple             | 6.63 us                                                | 6.84 us: 1.03x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.57 sec: 1.03x slower                                                   |
| logging_format             | 7.35 us                                                | 7.68 us: 1.05x slower                                                    |
| html5lib                   | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                    |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 325 us: 1.06x slower                                                     |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.06x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 73.1 ms: 1.07x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 152 ms: 1.07x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 81.9 ms: 1.07x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.60 ms: 1.07x slower                                                    |
| sympy_str                  | 292 ms                                                 | 312 ms: 1.07x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.4 ms: 1.07x slower                                                    |
| nqueens                    | 80.1 ms                                                | 86.0 ms: 1.07x slower                                                    |
| richards                   | 45.9 ms                                                | 49.7 ms: 1.08x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 54.3 ms: 1.08x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 92.2 ms: 1.08x slower                                                    |
| sympy_expand               | 468 ms                                                 | 516 ms: 1.10x slower                                                     |
| richards_super             | 51.9 ms                                                | 57.4 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.90 ms: 1.11x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 66.0 ms: 1.12x slower                                                    |
| genshi_text                | 22.8 ms                                                | 25.6 ms: 1.12x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.8 us: 1.12x slower                                                    |
| django_template            | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.15x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.5 ms: 1.21x slower                                                    |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                     |
| nbody                      | 89.3 ms                                                | 109 ms: 1.22x slower                                                     |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                     |
| telco                      | 6.53 ms                                                | 8.18 ms: 1.25x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                    |
| pidigits                   | 184 ms                                                 | 235 ms: 1.27x slower                                                     |
| mako                       | 11.0 ms                                                | 15.0 ms: 1.36x slower                                                    |
| coverage                   | 71.4 ms                                                | 108 ms: 1.52x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 95.2 ms: 8.81x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (3): asyncio_websockets, json, regex_compile
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250416-3.14.0a7+-956e5d1-NOGIL/bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 55.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x