# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.201x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 367 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                   |
| html5lib       | 63.6 ms                                                | 95.7 ms: 1.51x slower                                                    |
| Geometric mean | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 752 ms: 1.48x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 777 ms: 1.39x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 327 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 415 ms: 1.35x faster                                                     |
| async_tree_none            | 464 ms                                                 | 363 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 442 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 608 ms: 1.18x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                    |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| float          | 80.8 ms                                                | 111 ms: 1.38x slower                                                     |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                  | 1.26x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                    |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                    |
| regex_compile  | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.9 ms: 1.08x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.59 sec: 1.23x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 74.3 ms: 1.26x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.38x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 346 us: 1.57x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 533 us: 1.73x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.5 ms: 1.27x slower                                                    |
| genshi_text     | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                    |
| django_template | 34.7 ms                                                | 51.2 ms: 1.48x slower                                                    |
| mako            | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 752 ms: 1.48x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 777 ms: 1.39x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 327 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 415 ms: 1.35x faster                                                     |
| async_tree_none            | 464 ms                                                 | 363 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 442 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 608 ms: 1.18x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                    |
| gc_traversal               | 3.46 ms                                                | 3.16 ms: 1.10x faster                                                    |
| deepcopy                   | 352 us                                                 | 327 us: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 89.9 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.14 us: 1.03x faster                                                    |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                     |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.1 ms: 1.05x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.99 sec: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                    |
| scimark_fft                | 342 ms                                                 | 371 ms: 1.09x slower                                                     |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.46 us: 1.12x slower                                                    |
| pylint                     | 319 ms                                                 | 367 ms: 1.15x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 91.2 ms: 1.16x slower                                                    |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.20 ms: 1.18x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.88 sec: 1.19x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                    |
| regex_compile              | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 92.7 ms: 1.21x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.43 sec: 1.22x slower                                                   |
| nqueens                    | 80.1 ms                                                | 97.8 ms: 1.22x slower                                                    |
| generators                 | 32.2 ms                                                | 39.5 ms: 1.23x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.59 sec: 1.23x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 66.3 ms: 1.24x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 74.3 ms: 1.26x slower                                                    |
| thrift                     | 791 us                                                 | 998 us: 1.26x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 63.5 ms: 1.27x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.2 ms: 1.29x slower                                                    |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                                    |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 984 ms: 1.32x slower                                                     |
| genshi_text                | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.38x slower                                                    |
| float                      | 80.8 ms                                                | 111 ms: 1.38x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 198 ms: 1.38x slower                                                     |
| 2to3                       | 264 ms                                                 | 367 ms: 1.39x slower                                                     |
| logging_simple             | 6.63 us                                                | 9.35 us: 1.41x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.42x slower                                                    |
| logging_format             | 7.35 us                                                | 10.5 us: 1.43x slower                                                    |
| comprehensions             | 19.8 us                                                | 28.5 us: 1.44x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.44x slower                                                    |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                                     |
| coverage                   | 71.4 ms                                                | 105 ms: 1.46x slower                                                     |
| django_template            | 34.7 ms                                                | 51.2 ms: 1.48x slower                                                    |
| pyflate                    | 448 ms                                                 | 672 ms: 1.50x slower                                                     |
| html5lib                   | 63.6 ms                                                | 95.7 ms: 1.51x slower                                                    |
| mako                       | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 346 us: 1.57x slower                                                     |
| richards_super             | 51.9 ms                                                | 81.6 ms: 1.57x slower                                                    |
| chaos                      | 62.8 ms                                                | 99.0 ms: 1.58x slower                                                    |
| richards                   | 45.9 ms                                                | 73.6 ms: 1.60x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 2.71 ms: 1.62x slower                                                    |
| sympy_str                  | 292 ms                                                 | 473 ms: 1.62x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 111 ms: 1.63x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.78 ms: 1.63x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 187 ms: 1.64x slower                                                     |
| hexiom                     | 6.17 ms                                                | 10.2 ms: 1.66x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.1 ms: 1.72x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 533 us: 1.73x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.35 ms: 1.74x slower                                                    |
| raytrace                   | 299 ms                                                 | 523 ms: 1.75x slower                                                     |
| logging_silent             | 109 ns                                                 | 200 ns: 1.83x slower                                                     |
| go                         | 139 ms                                                 | 261 ms: 1.88x slower                                                     |
| scimark_sor                | 130 ms                                                 | 245 ms: 1.89x slower                                                     |
| sympy_expand               | 468 ms                                                 | 953 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.05 ms: 2.34x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 107 ms: 9.93x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.30x slower                                                             |

Benchmark hidden because not significant (2): deepcopy_memo, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.201x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x