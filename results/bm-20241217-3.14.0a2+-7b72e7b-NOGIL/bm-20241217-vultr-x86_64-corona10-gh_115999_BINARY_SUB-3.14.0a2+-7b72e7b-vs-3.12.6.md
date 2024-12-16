# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.224x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 368 ms: 1.40x slower                                                     |
| docutils       | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| html5lib       | 63.6 ms                                                | 96.9 ms: 1.52x slower                                                    |
| Geometric mean | (ref)                                                  | 1.36x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 833 ms: 1.33x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 855 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 450 ms: 1.24x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                     |
| async_tree_none            | 464 ms                                                 | 390 ms: 1.19x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 625 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 649 ms: 1.10x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                    |
| async_generators           | 384 ms                                                 | 454 ms: 1.18x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| nbody          | 89.3 ms                                                | 131 ms: 1.46x slower                                                     |
| float          | 80.8 ms                                                | 139 ms: 1.72x slower                                                     |
| Geometric mean | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                    |
| regex_dna      | 168 ms                                                 | 185 ms: 1.11x slower                                                     |
| regex_v8       | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                    |
| regex_compile  | 142 ms                                                 | 178 ms: 1.25x slower                                                     |
| Geometric mean | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                    |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 97.5 ms: 1.14x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 335 us: 1.52x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 519 us: 1.69x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 65.1 ms: 1.30x slower                                                    |
| genshi_text     | 22.8 ms                                                | 32.0 ms: 1.40x slower                                                    |
| django_template | 34.7 ms                                                | 51.6 ms: 1.49x slower                                                    |
| mako            | 11.0 ms                                                | 17.9 ms: 1.62x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 833 ms: 1.33x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 855 ms: 1.27x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 450 ms: 1.24x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 363 ms: 1.23x faster                                                     |
| async_tree_none            | 464 ms                                                 | 390 ms: 1.19x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 625 ms: 1.16x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 649 ms: 1.10x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.21 ms: 1.08x faster                                                    |
| deepcopy                   | 352 us                                                 | 330 us: 1.06x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                    |
| pathlib                    | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                    |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                                     |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.28 us: 1.04x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.00 sec: 1.06x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.11x slower                                                     |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.11x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 97.5 ms: 1.14x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.55 us: 1.15x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.10 sec: 1.17x slower                                                   |
| scimark_fft                | 342 ms                                                 | 403 ms: 1.18x slower                                                     |
| async_generators           | 384 ms                                                 | 454 ms: 1.18x slower                                                     |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 95.1 ms: 1.21x slower                                                    |
| generators                 | 32.2 ms                                                | 39.0 ms: 1.21x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 92.9 ms: 1.21x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                    |
| nqueens                    | 80.1 ms                                                | 97.8 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                                     |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                     |
| regex_compile              | 142 ms                                                 | 178 ms: 1.25x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 137 ms: 1.29x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 65.1 ms: 1.30x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 69.3 ms: 1.30x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 974 ms: 1.31x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.80 ms: 1.32x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.01 sec: 1.32x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.55 sec: 1.32x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 78.2 ms: 1.33x slower                                                    |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.33x slower                                                     |
| telco                      | 6.53 ms                                                | 8.71 ms: 1.34x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.5 ms: 1.35x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 156 ms: 1.37x slower                                                     |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.3 ms: 1.38x slower                                                    |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                    |
| 2to3                       | 264 ms                                                 | 368 ms: 1.40x slower                                                     |
| genshi_text                | 22.8 ms                                                | 32.0 ms: 1.40x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.4 ms: 1.43x slower                                                    |
| nbody                      | 89.3 ms                                                | 131 ms: 1.46x slower                                                     |
| thrift                     | 791 us                                                 | 1.16 ms: 1.46x slower                                                    |
| django_template            | 34.7 ms                                                | 51.6 ms: 1.49x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 335 us: 1.52x slower                                                     |
| html5lib                   | 63.6 ms                                                | 96.9 ms: 1.52x slower                                                    |
| pyflate                    | 448 ms                                                 | 699 ms: 1.56x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.81 ms: 1.59x slower                                                    |
| mako                       | 11.0 ms                                                | 17.9 ms: 1.62x slower                                                    |
| logging_format             | 7.35 us                                                | 12.0 us: 1.64x slower                                                    |
| sympy_str                  | 292 ms                                                 | 478 ms: 1.64x slower                                                     |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.65x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.80 ms: 1.65x slower                                                    |
| chaos                      | 62.8 ms                                                | 105 ms: 1.68x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 519 us: 1.69x slower                                                     |
| richards                   | 45.9 ms                                                | 78.4 ms: 1.71x slower                                                    |
| float                      | 80.8 ms                                                | 139 ms: 1.72x slower                                                     |
| logging_silent             | 109 ns                                                 | 188 ns: 1.73x slower                                                     |
| richards_super             | 51.9 ms                                                | 89.9 ms: 1.73x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.74x slower                                                     |
| scimark_sor                | 130 ms                                                 | 225 ms: 1.74x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 3.00 ms: 1.79x slower                                                    |
| raytrace                   | 299 ms                                                 | 555 ms: 1.85x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.59 ms: 1.91x slower                                                    |
| go                         | 139 ms                                                 | 274 ms: 1.97x slower                                                     |
| sympy_expand               | 468 ms                                                 | 958 ms: 2.05x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 350 ms: 2.11x slower                                                     |
| deltablue                  | 3.45 ms                                                | 8.08 ms: 2.34x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.42 ms: 3.63x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.09x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                             |

Benchmark hidden because not significant (1): deepcopy_memo
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.224x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x