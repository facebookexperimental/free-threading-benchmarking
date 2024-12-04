# Results vs. 3.12.6

- fork: python
- ref: dabcecfd6dadb9430733
- machine: linux-x86_64
- commit hash: dabcecf
- commit date: 2024-12-03
- overall geometric mean: 1.231x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 370 ms: 1.40x slower                                                   |
| docutils       | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                 |
| html5lib       | 63.6 ms                                                | 101 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                  | 1.38x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 831 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 860 ms: 1.26x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 452 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 361 ms: 1.24x faster                                                   |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.19x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 622 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 644 ms: 1.11x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                                  |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                                   |
| float          | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                  | 1.39x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.09x faster                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| regex_compile  | 142 ms                                                 | 180 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                  |
| json_loads           | 26.5 us                                                | 28.5 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 79.2 ms: 1.34x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 335 us: 1.52x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 523 us: 1.70x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 65.3 ms: 1.30x slower                                                  |
| genshi_text     | 22.8 ms                                                | 32.3 ms: 1.41x slower                                                  |
| django_template | 34.7 ms                                                | 52.4 ms: 1.51x slower                                                  |
| mako            | 11.0 ms                                                | 17.5 ms: 1.59x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 831 ms: 1.34x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 860 ms: 1.26x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 452 ms: 1.24x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 361 ms: 1.24x faster                                                   |
| async_tree_none            | 464 ms                                                 | 389 ms: 1.19x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 473 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 622 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 644 ms: 1.11x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.09x faster                                                  |
| deepcopy                   | 352 us                                                 | 329 us: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                  |
| deepcopy_memo              | 40.3 us                                                | 41.0 us: 1.02x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.53 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.31 us: 1.05x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.01 sec: 1.06x slower                                                 |
| coroutines                 | 23.9 ms                                                | 25.4 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.08x slower                                                  |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.12x slower                                                   |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.1 ms: 1.15x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.58 us: 1.16x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.85 sec: 1.18x slower                                                 |
| scimark_fft                | 342 ms                                                 | 402 ms: 1.18x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                 |
| async_generators           | 384 ms                                                 | 457 ms: 1.19x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 91.7 ms: 1.20x slower                                                  |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                   |
| generators                 | 32.2 ms                                                | 38.8 ms: 1.20x slower                                                  |
| nqueens                    | 80.1 ms                                                | 97.5 ms: 1.22x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 96.4 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.67 sec: 1.27x slower                                                 |
| regex_compile              | 142 ms                                                 | 180 ms: 1.27x slower                                                   |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.63 ms: 1.28x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 65.3 ms: 1.30x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 139 ms: 1.30x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 69.7 ms: 1.31x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.54 sec: 1.32x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 983 ms: 1.32x slower                                                   |
| fannkuch                   | 372 ms                                                 | 496 ms: 1.33x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.04 sec: 1.34x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 79.2 ms: 1.34x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.4 ms: 1.35x slower                                                  |
| telco                      | 6.53 ms                                                | 8.80 ms: 1.35x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.5 us: 1.39x slower                                                  |
| 2to3                       | 264 ms                                                 | 370 ms: 1.40x slower                                                   |
| genshi_text                | 22.8 ms                                                | 32.3 ms: 1.41x slower                                                  |
| coverage                   | 71.4 ms                                                | 102 ms: 1.42x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.7 ms: 1.45x slower                                                  |
| thrift                     | 791 us                                                 | 1.17 ms: 1.48x slower                                                  |
| django_template            | 34.7 ms                                                | 52.4 ms: 1.51x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 335 us: 1.52x slower                                                   |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                                   |
| pyflate                    | 448 ms                                                 | 693 ms: 1.55x slower                                                   |
| html5lib                   | 63.6 ms                                                | 101 ms: 1.58x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 181 ms: 1.58x slower                                                   |
| mako                       | 11.0 ms                                                | 17.5 ms: 1.59x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.90 ms: 1.61x slower                                                  |
| sympy_str                  | 292 ms                                                 | 480 ms: 1.65x slower                                                   |
| chaos                      | 62.8 ms                                                | 104 ms: 1.65x slower                                                   |
| logging_format             | 7.35 us                                                | 12.2 us: 1.66x slower                                                  |
| logging_simple             | 6.63 us                                                | 11.1 us: 1.67x slower                                                  |
| richards                   | 45.9 ms                                                | 77.7 ms: 1.69x slower                                                  |
| richards_super             | 51.9 ms                                                | 87.7 ms: 1.69x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 523 us: 1.70x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                  |
| logging_silent             | 109 ns                                                 | 187 ns: 1.72x slower                                                   |
| float                      | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 119 ms: 1.74x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 3.00 ms: 1.80x slower                                                  |
| scimark_sor                | 130 ms                                                 | 236 ms: 1.82x slower                                                   |
| raytrace                   | 299 ms                                                 | 558 ms: 1.86x slower                                                   |
| go                         | 139 ms                                                 | 269 ms: 1.93x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.62 ms: 1.93x slower                                                  |
| sympy_expand               | 468 ms                                                 | 963 ms: 2.06x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 353 ms: 2.12x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.15 ms: 2.36x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.12x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                           |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-dabcecf-NOGIL/bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2+-dabcecf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.231x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x