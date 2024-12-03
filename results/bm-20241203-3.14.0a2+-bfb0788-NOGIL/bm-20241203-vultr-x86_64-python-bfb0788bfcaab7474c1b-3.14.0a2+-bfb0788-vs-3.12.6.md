# Results vs. 3.12.6

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.259x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 377 ms: 1.43x slower                                                   |
| docutils       | 2.64 sec                                               | 3.22 sec: 1.22x slower                                                 |
| html5lib       | 63.6 ms                                                | 102 ms: 1.61x slower                                                   |
| Geometric mean | (ref)                                                  | 1.41x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 862 ms: 1.29x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 890 ms: 1.22x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 368 ms: 1.21x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 462 ms: 1.21x faster                                                   |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 493 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 654 ms: 1.09x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.7 ms: 1.20x slower                                                  |
| async_generators           | 384 ms                                                 | 471 ms: 1.22x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| float          | 80.8 ms                                                | 142 ms: 1.76x slower                                                   |
| Geometric mean | (ref)                                                  | 1.38x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| regex_v8       | 20.6 ms                                                | 26.1 ms: 1.27x slower                                                  |
| regex_compile  | 142 ms                                                 | 194 ms: 1.36x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.77 sec: 1.32x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 386 us: 1.75x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 562 us: 1.83x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 67.6 ms: 1.35x slower                                                  |
| genshi_text     | 22.8 ms                                                | 33.6 ms: 1.47x slower                                                  |
| django_template | 34.7 ms                                                | 55.6 ms: 1.60x slower                                                  |
| mako            | 11.0 ms                                                | 20.0 ms: 1.82x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 862 ms: 1.29x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 890 ms: 1.22x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 368 ms: 1.21x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 462 ms: 1.21x faster                                                   |
| async_tree_none            | 464 ms                                                 | 400 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 624 ms: 1.16x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 493 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 654 ms: 1.09x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.19 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                   |
| pathlib                    | 21.5 ms                                                | 20.6 ms: 1.05x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                  |
| deepcopy                   | 352 us                                                 | 354 us: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 45.8 us: 1.14x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.51 sec: 1.16x slower                                                 |
| scimark_fft                | 342 ms                                                 | 408 ms: 1.19x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                   |
| coroutines                 | 23.9 ms                                                | 28.7 ms: 1.20x slower                                                  |
| spectral_norm              | 110 ms                                                 | 132 ms: 1.20x slower                                                   |
| generators                 | 32.2 ms                                                | 39.1 ms: 1.21x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.74 us: 1.21x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.22 sec: 1.22x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 93.8 ms: 1.22x slower                                                  |
| async_generators           | 384 ms                                                 | 471 ms: 1.22x slower                                                   |
| pylint                     | 319 ms                                                 | 395 ms: 1.24x slower                                                   |
| mdp                        | 2.42 sec                                               | 3.03 sec: 1.25x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 98.7 ms: 1.25x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 26.1 ms: 1.27x slower                                                  |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.29x slower                                                   |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.30x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 213 us: 1.30x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.77 sec: 1.32x slower                                                 |
| telco                      | 6.53 ms                                                | 8.73 ms: 1.34x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.90 ms: 1.34x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 67.6 ms: 1.35x slower                                                  |
| regex_compile              | 142 ms                                                 | 194 ms: 1.36x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.61 sec: 1.38x slower                                                 |
| fannkuch                   | 372 ms                                                 | 517 ms: 1.39x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 30.3 ms: 1.39x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 82.2 ms: 1.39x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 74.7 ms: 1.40x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 150 ms: 1.40x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 14.5 ms: 1.40x slower                                                  |
| coverage                   | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| 2to3                       | 264 ms                                                 | 377 ms: 1.43x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 1.08 sec: 1.46x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 208 ms: 1.46x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.24 sec: 1.47x slower                                                 |
| comprehensions             | 19.8 us                                                | 29.2 us: 1.47x slower                                                  |
| genshi_text                | 22.8 ms                                                | 33.6 ms: 1.47x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 30.7 ms: 1.50x slower                                                  |
| nbody                      | 89.3 ms                                                | 134 ms: 1.50x slower                                                   |
| thrift                     | 791 us                                                 | 1.21 ms: 1.53x slower                                                  |
| django_template            | 34.7 ms                                                | 55.6 ms: 1.60x slower                                                  |
| html5lib                   | 63.6 ms                                                | 102 ms: 1.61x slower                                                   |
| pyflate                    | 448 ms                                                 | 737 ms: 1.65x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                  |
| sympy_str                  | 292 ms                                                 | 492 ms: 1.69x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 193 ms: 1.69x slower                                                   |
| logging_simple             | 6.63 us                                                | 11.2 us: 1.69x slower                                                  |
| logging_format             | 7.35 us                                                | 12.5 us: 1.70x slower                                                  |
| hexiom                     | 6.17 ms                                                | 10.8 ms: 1.74x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 386 us: 1.75x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                  |
| float                      | 80.8 ms                                                | 142 ms: 1.76x slower                                                   |
| chaos                      | 62.8 ms                                                | 112 ms: 1.78x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.80x slower                                                   |
| mako                       | 11.0 ms                                                | 20.0 ms: 1.82x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 562 us: 1.83x slower                                                   |
| richards                   | 45.9 ms                                                | 84.0 ms: 1.83x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.06 ms: 1.83x slower                                                  |
| logging_silent             | 109 ns                                                 | 201 ns: 1.85x slower                                                   |
| scimark_sor                | 130 ms                                                 | 243 ms: 1.87x slower                                                   |
| richards_super             | 51.9 ms                                                | 101 ms: 1.95x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.64 ms: 1.95x slower                                                  |
| go                         | 139 ms                                                 | 283 ms: 2.03x slower                                                   |
| raytrace                   | 299 ms                                                 | 611 ms: 2.04x slower                                                   |
| sympy_expand               | 468 ms                                                 | 986 ms: 2.11x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.78 ms: 2.55x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.40x slower                                                           |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.259x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.33x