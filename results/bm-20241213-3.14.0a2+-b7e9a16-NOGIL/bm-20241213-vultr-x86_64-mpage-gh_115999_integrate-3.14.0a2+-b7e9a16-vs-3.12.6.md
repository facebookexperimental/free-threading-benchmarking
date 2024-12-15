# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.084x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 318 ms: 1.21x slower                                                 |
| docutils       | 2.64 sec                                               | 2.84 sec: 1.08x slower                                               |
| html5lib       | 63.6 ms                                                | 75.3 ms: 1.18x slower                                                |
| Geometric mean | (ref)                                                  | 1.15x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                 |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| async_generators           | 384 ms                                                 | 422 ms: 1.10x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                 |
| float          | 80.8 ms                                                | 83.0 ms: 1.03x slower                                                |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                  | 1.14x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                 |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                 |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                |
| Geometric mean | (ref)                                                  | 1.04x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 27.8 us: 1.05x slower                                                |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                               |
| unpickle_pure_python | 221 us                                                 | 248 us: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                |
| pickle_pure_python   | 308 us                                                 | 365 us: 1.19x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                |
| python_startup         | 9.93 ms                                                | 17.0 ms: 1.72x slower                                                |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                |
| django_template | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 591 ms: 1.88x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 239 ms: 1.86x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 309 ms: 1.81x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 604 ms: 1.79x faster                                                 |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                                |
| deepcopy                   | 352 us                                                 | 315 us: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                 |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                |
| deepcopy_memo              | 40.3 us                                                | 39.0 us: 1.03x faster                                                |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                                |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                 |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                 |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                 |
| float                      | 80.8 ms                                                | 83.0 ms: 1.03x slower                                                |
| dulwich_log                | 78.9 ms                                                | 82.2 ms: 1.04x slower                                                |
| json_loads                 | 26.5 us                                                | 27.8 us: 1.05x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.22 sec: 1.05x slower                                               |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                 |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.28 us: 1.07x slower                                                |
| logging_silent             | 109 ns                                                 | 117 ns: 1.07x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.84 sec: 1.08x slower                                               |
| pylint                     | 319 ms                                                 | 343 ms: 1.08x slower                                                 |
| comprehensions             | 19.8 us                                                | 21.5 us: 1.08x slower                                                |
| scimark_fft                | 342 ms                                                 | 371 ms: 1.09x slower                                                 |
| async_generators           | 384 ms                                                 | 422 ms: 1.10x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.29 us: 1.10x slower                                                |
| raytrace                   | 299 ms                                                 | 331 ms: 1.11x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                               |
| pyflate                    | 448 ms                                                 | 498 ms: 1.11x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.3 ms: 1.12x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 248 us: 1.12x slower                                                 |
| logging_format             | 7.35 us                                                | 8.27 us: 1.13x slower                                                |
| crypto_pyaes               | 76.6 ms                                                | 86.4 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 96.4 ms: 1.13x slower                                                |
| chaos                      | 62.8 ms                                                | 71.2 ms: 1.13x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.14x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.76 sec: 1.14x slower                                               |
| scimark_sor                | 130 ms                                                 | 149 ms: 1.14x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 854 ms: 1.15x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 61.2 ms: 1.15x slower                                                |
| thrift                     | 791 us                                                 | 915 us: 1.16x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.76 sec: 1.16x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.94 ms: 1.16x slower                                                |
| html5lib                   | 63.6 ms                                                | 75.3 ms: 1.18x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 81.2 ms: 1.19x slower                                                |
| pickle_pure_python         | 308 us                                                 | 365 us: 1.19x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.62 ms: 1.19x slower                                                |
| nqueens                    | 80.1 ms                                                | 96.5 ms: 1.21x slower                                                |
| 2to3                       | 264 ms                                                 | 318 ms: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.31 ms: 1.21x slower                                                |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                |
| richards                   | 45.9 ms                                                | 56.8 ms: 1.24x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 177 ms: 1.24x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.65 ms: 1.24x slower                                                |
| django_template            | 34.7 ms                                                | 43.4 ms: 1.25x slower                                                |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                 |
| richards_super             | 51.9 ms                                                | 66.1 ms: 1.27x slower                                                |
| json_dumps                 | 10.4 ms                                                | 13.2 ms: 1.28x slower                                                |
| fannkuch                   | 372 ms                                                 | 480 ms: 1.29x slower                                                 |
| telco                      | 6.53 ms                                                | 8.46 ms: 1.30x slower                                                |
| deltablue                  | 3.45 ms                                                | 4.72 ms: 1.37x slower                                                |
| coverage                   | 71.4 ms                                                | 98.7 ms: 1.38x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 28.4 ms: 1.38x slower                                                |
| scimark_lu                 | 114 ms                                                 | 161 ms: 1.41x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                 |
| sympy_str                  | 292 ms                                                 | 458 ms: 1.57x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                |
| python_startup             | 9.93 ms                                                | 17.0 ms: 1.72x slower                                                |
| sympy_expand               | 468 ms                                                 | 927 ms: 1.98x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 340 ms: 2.05x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                                |
| bench_mp_pool              | 10.8 ms                                                | 105 ms: 9.75x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.13x slower                                                         |

Benchmark hidden because not significant (1): bpe_tokeniser
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.084x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.34x