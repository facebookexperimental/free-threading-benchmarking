# Results vs. 3.12.6

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| html5lib       | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.88x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 527 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                  |
| nbody          | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                 | 220 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| regex_v8       | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.5 ms: 1.13x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.28 ms: 1.12x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 210 us: 1.05x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.5 ms: 1.03x faster                                                  |
| django_template | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                  |
| mako            | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 555 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 246 ms: 1.88x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 245 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.6 us: 1.51x faster                                                  |
| deepcopy                   | 352 us                                                 | 244 us: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 527 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 531 ms: 1.35x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.33x faster                                                   |
| comprehensions             | 19.8 us                                                | 15.8 us: 1.26x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.3 ms: 1.24x faster                                                  |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.22x faster                                                   |
| raytrace                   | 299 ms                                                 | 246 ms: 1.22x faster                                                   |
| spectral_norm              | 110 ms                                                 | 93.9 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.1 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                  |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.81 us: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 85.5 ms: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.28 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.59 us: 1.11x faster                                                  |
| logging_silent             | 109 ns                                                 | 97.9 ns: 1.11x faster                                                  |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.0 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 61.8 ms: 1.11x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| pylint                     | 319 ms                                                 | 289 ms: 1.10x faster                                                   |
| richards                   | 45.9 ms                                                | 41.8 ms: 1.10x faster                                                  |
| pyflate                    | 448 ms                                                 | 408 ms: 1.10x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.64 ms: 1.09x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.07 sec: 1.09x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.8 ms: 1.09x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.07x faster                                                 |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 210 us: 1.05x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.0 ms: 1.05x faster                                                  |
| thrift                     | 791 us                                                 | 758 us: 1.04x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.32 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 48.5 ms: 1.03x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.27 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.0 ms: 1.03x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 88.1 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                   |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.26 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                  |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                  |
| fannkuch                   | 372 ms                                                 | 387 ms: 1.04x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.7 ms: 1.10x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.08 ms: 1.15x slower                                                  |
| pidigits                   | 184 ms                                                 | 220 ms: 1.20x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 13.1 ms: 1.21x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.78 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.25x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (2): coroutines, sympy_expand
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251123-3.15.0a2+-e73fbba/bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x