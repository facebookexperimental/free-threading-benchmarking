# Results vs. 3.12.6

- fork: python
- ref: 56eabea056ae1da49b55
- machine: linux-x86_64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| html5lib       | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 336 ms: 1.15x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.0 ms: 1.14x faster                                                 |
| nbody          | 89.3 ms                                                | 88.0 ms: 1.01x faster                                                 |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.27 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 47.2 ms: 1.06x faster                                                 |
| django_template | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 250 us: 1.41x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.9 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 249 ms: 1.20x faster                                                  |
| generators                 | 32.2 ms                                                | 27.3 ms: 1.18x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.7 ms: 1.18x faster                                                 |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.13 sec: 1.15x faster                                                |
| async_generators           | 384 ms                                                 | 336 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                 |
| float                      | 80.8 ms                                                | 71.0 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                 |
| spectral_norm              | 110 ms                                                 | 97.4 ms: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 398 ms: 1.13x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.3 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 41.2 ms: 1.12x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.54 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.8 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| sympy_str                  | 292 ms                                                 | 265 ms: 1.10x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| thrift                     | 791 us                                                 | 729 us: 1.09x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.9 ms: 1.07x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.2 ms: 1.06x faster                                                 |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.24 ms: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| sympy_expand               | 468 ms                                                 | 444 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.1 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.7 ms: 1.05x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                |
| scimark_fft                | 342 ms                                                 | 328 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                  |
| html5lib                   | 63.6 ms                                                | 61.3 ms: 1.04x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.6 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| nbody                      | 89.3 ms                                                | 88.0 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| django_template            | 34.7 ms                                                | 34.3 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                 |
| logging_format             | 7.35 us                                                | 7.44 us: 1.01x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.71 us: 1.01x slower                                                 |
| json                       | 5.02 ms                                                | 5.10 ms: 1.01x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.27 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.56 sec: 1.03x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 764 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                 |
| telco                      | 6.53 ms                                                | 7.23 ms: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 81.2 ms: 1.14x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.40 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.89 ms: 1.74x slower                                                 |
| logging_silent             | 109 ns                                                 | 469 ns: 4.30x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 98.3 ms: 9.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.15x