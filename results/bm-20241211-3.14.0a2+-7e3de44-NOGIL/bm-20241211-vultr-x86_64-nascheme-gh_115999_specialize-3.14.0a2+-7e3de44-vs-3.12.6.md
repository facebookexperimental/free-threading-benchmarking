# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 7e3de44
- commit date: 2024-12-11
- overall geometric mean: 1.217x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 367 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                   |
| html5lib       | 63.6 ms                                                | 97.3 ms: 1.53x slower                                                    |
| Geometric mean | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 781 ms: 1.42x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 795 ms: 1.36x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 425 ms: 1.32x faster                                                     |
| async_tree_none            | 464 ms                                                 | 364 ms: 1.27x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 448 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 594 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 612 ms: 1.17x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                    |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| float          | 80.8 ms                                                | 115 ms: 1.42x slower                                                     |
| nbody          | 89.3 ms                                                | 129 ms: 1.44x slower                                                     |
| Geometric mean | (ref)                                                  | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                    |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                     |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.23x slower                                                    |
| regex_compile  | 142 ms                                                 | 181 ms: 1.27x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.5 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.62 sec: 1.24x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 78.9 ms: 1.34x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 499 us: 1.62x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.22x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.7 ms: 1.27x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.5 ms: 1.38x slower                                                    |
| django_template | 34.7 ms                                                | 50.2 ms: 1.45x slower                                                    |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 781 ms: 1.42x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 795 ms: 1.36x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 337 ms: 1.32x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 425 ms: 1.32x faster                                                     |
| async_tree_none            | 464 ms                                                 | 364 ms: 1.27x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 448 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 594 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 612 ms: 1.17x faster                                                     |
| deepcopy                   | 352 us                                                 | 324 us: 1.09x faster                                                     |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.93 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 39.8 us: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.04x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.98 sec: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.08x slower                                                    |
| spectral_norm              | 110 ms                                                 | 120 ms: 1.09x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.12x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.49 us: 1.13x slower                                                    |
| regex_dna                  | 168 ms                                                 | 191 ms: 1.14x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                    |
| scimark_fft                | 342 ms                                                 | 396 ms: 1.16x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.07 sec: 1.16x slower                                                   |
| generators                 | 32.2 ms                                                | 37.7 ms: 1.17x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 93.4 ms: 1.18x slower                                                    |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                     |
| pylint                     | 319 ms                                                 | 379 ms: 1.19x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 91.2 ms: 1.19x slower                                                    |
| nqueens                    | 80.1 ms                                                | 98.0 ms: 1.22x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 25.2 ms: 1.23x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.62 sec: 1.24x slower                                                   |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.25x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 63.7 ms: 1.27x slower                                                    |
| regex_compile              | 142 ms                                                 | 181 ms: 1.27x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 955 ms: 1.29x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.66 ms: 1.29x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 68.7 ms: 1.29x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.99 sec: 1.31x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.55 sec: 1.32x slower                                                   |
| fannkuch                   | 372 ms                                                 | 495 ms: 1.33x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.1 ms: 1.34x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 78.9 ms: 1.34x slower                                                    |
| telco                      | 6.53 ms                                                | 8.89 ms: 1.36x slower                                                    |
| comprehensions             | 19.8 us                                                | 27.1 us: 1.37x slower                                                    |
| genshi_text                | 22.8 ms                                                | 31.5 ms: 1.38x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                    |
| 2to3                       | 264 ms                                                 | 367 ms: 1.39x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 202 ms: 1.41x slower                                                     |
| float                      | 80.8 ms                                                | 115 ms: 1.42x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| nbody                      | 89.3 ms                                                | 129 ms: 1.44x slower                                                     |
| django_template            | 34.7 ms                                                | 50.2 ms: 1.45x slower                                                    |
| coverage                   | 71.4 ms                                                | 105 ms: 1.47x slower                                                     |
| thrift                     | 791 us                                                 | 1.19 ms: 1.50x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                     |
| html5lib                   | 63.6 ms                                                | 97.3 ms: 1.53x slower                                                    |
| pyflate                    | 448 ms                                                 | 699 ms: 1.56x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.74 ms: 1.58x slower                                                    |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 499 us: 1.62x slower                                                     |
| sympy_str                  | 292 ms                                                 | 474 ms: 1.63x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 2.72 ms: 1.63x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 186 ms: 1.63x slower                                                     |
| logging_simple             | 6.63 us                                                | 10.8 us: 1.63x slower                                                    |
| logging_format             | 7.35 us                                                | 12.1 us: 1.65x slower                                                    |
| logging_silent             | 109 ns                                                 | 180 ns: 1.66x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                    |
| chaos                      | 62.8 ms                                                | 105 ms: 1.67x slower                                                     |
| richards_super             | 51.9 ms                                                | 88.4 ms: 1.71x slower                                                    |
| richards                   | 45.9 ms                                                | 79.0 ms: 1.72x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.35 ms: 1.74x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.75x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| scimark_sor                | 130 ms                                                 | 232 ms: 1.79x slower                                                     |
| raytrace                   | 299 ms                                                 | 562 ms: 1.88x slower                                                     |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                     |
| sympy_expand               | 468 ms                                                 | 952 ms: 2.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 349 ms: 2.10x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.09 ms: 2.35x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.41 ms: 3.63x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.10x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.32x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241211-3.14.0a2+-7e3de44-NOGIL/bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.217x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x