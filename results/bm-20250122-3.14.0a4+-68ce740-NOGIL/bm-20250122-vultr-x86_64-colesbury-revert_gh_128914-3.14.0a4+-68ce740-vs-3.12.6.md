# Results vs. 3.12.6

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.056x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                  |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                |
| html5lib       | 63.6 ms                                                | 71.2 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.1 ms: 1.05x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 136 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.37 sec: 1.12x slower                                                |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                 |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.21x slower                                                 |
| django_template | 34.7 ms                                                | 43.0 ms: 1.24x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 283 ms: 1.64x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 346 ms: 1.60x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.14x faster                                                 |
| deepcopy                   | 352 us                                                 | 314 us: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                 |
| float                      | 80.8 ms                                                | 77.1 ms: 1.05x faster                                                 |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.34 ms: 1.04x faster                                                 |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| go                         | 139 ms                                                 | 138 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.01x slower                                                  |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| logging_silent             | 109 ns                                                 | 113 ns: 1.03x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.6 us: 1.04x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 82.4 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.23 us: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| regex_compile              | 142 ms                                                 | 152 ms: 1.06x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                |
| raytrace                   | 299 ms                                                 | 329 ms: 1.10x slower                                                  |
| chaos                      | 62.8 ms                                                | 69.3 ms: 1.10x slower                                                 |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| pyflate                    | 448 ms                                                 | 496 ms: 1.11x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.34 us: 1.11x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 830 ms: 1.12x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.70 sec: 1.12x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.4 ms: 1.12x slower                                                 |
| html5lib                   | 63.6 ms                                                | 71.2 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.37 sec: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.72 sec: 1.13x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                                  |
| thrift                     | 791 us                                                 | 898 us: 1.13x slower                                                  |
| logging_format             | 7.35 us                                                | 8.37 us: 1.14x slower                                                 |
| scimark_fft                | 342 ms                                                 | 389 ms: 1.14x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.14x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                                 |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                  |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.2 ms: 1.16x slower                                                 |
| sympy_expand               | 468 ms                                                 | 549 ms: 1.17x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.96 ms: 1.18x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.29 ms: 1.18x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.9 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 82.0 ms: 1.20x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.21x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.1 ms: 1.21x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                  |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                  |
| django_template            | 34.7 ms                                                | 43.0 ms: 1.24x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.48 ms: 1.25x slower                                                 |
| richards_super             | 51.9 ms                                                | 64.8 ms: 1.25x slower                                                 |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| fannkuch                   | 372 ms                                                 | 481 ms: 1.29x slower                                                  |
| telco                      | 6.53 ms                                                | 8.51 ms: 1.30x slower                                                 |
| deltablue                  | 3.45 ms                                                | 4.58 ms: 1.33x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.36x slower                                                 |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| nbody                      | 89.3 ms                                                | 136 ms: 1.53x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 94.3 ms: 8.73x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): pylint, bpe_tokeniser
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250122-3.14.0a4+-68ce740-NOGIL/bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x