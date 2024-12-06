# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.066x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 340 ms: 1.63x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                 |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| nbody          | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.8 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 24.8 us: 1.07x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 91.7 ms: 1.05x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.00x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 86.0 ms: 1.01x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 314 us: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 50.8 ms: 1.01x slower                                                 |
| django_template | 34.7 ms                                                | 35.9 ms: 1.04x slower                                                 |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 313 ms: 1.79x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 629 ms: 1.77x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 629 ms: 1.72x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 340 ms: 1.63x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 487 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.3 us: 1.33x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                 |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.15x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.3 ms: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                  |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                 |
| json                       | 5.02 ms                                                | 4.55 ms: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.32 sec: 1.10x faster                                                |
| regex_compile              | 142 ms                                                 | 130 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.6 ms: 1.07x faster                                                 |
| json_loads                 | 26.5 us                                                | 24.8 us: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.23 ms: 1.07x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.22 us: 1.07x faster                                                 |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.7 ms: 1.05x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.87 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 65.1 ms: 1.05x faster                                                 |
| thrift                     | 791 us                                                 | 755 us: 1.05x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.9 ms: 1.04x faster                                                 |
| float                      | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.8 ms: 1.04x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.04x faster                                                |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 719 ms: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 20.0 ms: 1.03x faster                                                 |
| mdp                        | 2.42 sec                                               | 2.36 sec: 1.03x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| 2to3                       | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.4 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 374 ms: 1.00x slower                                                  |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.00x slower                                                |
| xml_etree_process          | 59.0 ms                                                | 59.4 ms: 1.01x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 86.0 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 108 ms: 1.01x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 50.8 ms: 1.01x slower                                                 |
| scimark_fft                | 342 ms                                                 | 346 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 314 us: 1.02x slower                                                  |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 35.9 ms: 1.04x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.66 ms: 1.06x slower                                                 |
| nbody                      | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                 |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.3 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.41 ms: 1.13x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.8 ms: 1.21x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.61 ms: 1.33x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.9 ms: 8.23x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): sympy_expand, richards, pyflate, richards_super
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-eb8ce39/bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x