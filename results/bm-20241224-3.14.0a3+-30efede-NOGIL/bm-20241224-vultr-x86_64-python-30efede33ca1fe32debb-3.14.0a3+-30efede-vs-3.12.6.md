# Results vs. 3.12.6

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.168x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 349 ms: 1.33x slower                                                   |
| docutils       | 2.64 sec                                               | 3.01 sec: 1.14x slower                                                 |
| html5lib       | 63.6 ms                                                | 93.6 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 736 ms: 1.51x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 758 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 404 ms: 1.39x faster                                                   |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 432 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.01x faster                                                   |
| float          | 80.8 ms                                                | 113 ms: 1.39x slower                                                   |
| nbody          | 89.3 ms                                                | 128 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 73.5 ms: 1.25x slower                                                  |
| json_dumps           | 10.4 ms                                                | 13.8 ms: 1.33x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 329 us: 1.49x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 498 us: 1.62x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| genshi_text     | 22.8 ms                                                | 30.8 ms: 1.35x slower                                                  |
| django_template | 34.7 ms                                                | 49.4 ms: 1.42x slower                                                  |
| mako            | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 736 ms: 1.51x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 758 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 404 ms: 1.39x faster                                                   |
| async_tree_none            | 464 ms                                                 | 349 ms: 1.33x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 432 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 592 ms: 1.21x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.19 ms: 1.08x faster                                                  |
| deepcopy                   | 352 us                                                 | 327 us: 1.07x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.14 us: 1.03x faster                                                  |
| pidigits                   | 184 ms                                                 | 181 ms: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 40.8 us: 1.01x slower                                                  |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 5.02 sec: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| pylint                     | 319 ms                                                 | 347 ms: 1.09x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.45 us: 1.12x slower                                                  |
| scimark_fft                | 342 ms                                                 | 386 ms: 1.13x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.01 sec: 1.14x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 97.7 ms: 1.15x slower                                                  |
| dulwich_log                | 78.9 ms                                                | 90.7 ms: 1.15x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 194 ms: 1.17x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 90.3 ms: 1.18x slower                                                  |
| async_generators           | 384 ms                                                 | 455 ms: 1.18x slower                                                   |
| regex_compile              | 142 ms                                                 | 169 ms: 1.18x slower                                                   |
| generators                 | 32.2 ms                                                | 38.2 ms: 1.19x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.39 sec: 1.19x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.53 sec: 1.20x slower                                                 |
| sympy_str                  | 292 ms                                                 | 354 ms: 1.21x slower                                                   |
| nqueens                    | 80.1 ms                                                | 98.2 ms: 1.23x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 25.3 ms: 1.23x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 65.9 ms: 1.24x slower                                                  |
| sympy_expand               | 468 ms                                                 | 578 ms: 1.24x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 132 ms: 1.24x slower                                                   |
| thrift                     | 791 us                                                 | 984 us: 1.24x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 73.5 ms: 1.25x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.1 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.58 ms: 1.27x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 183 ms: 1.28x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 209 us: 1.28x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.9 ms: 1.28x slower                                                  |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.29x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 960 ms: 1.29x slower                                                   |
| telco                      | 6.53 ms                                                | 8.54 ms: 1.31x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.32x slower                                                 |
| 2to3                       | 264 ms                                                 | 349 ms: 1.33x slower                                                   |
| fannkuch                   | 372 ms                                                 | 496 ms: 1.33x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.8 ms: 1.33x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.8 ms: 1.35x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.3 us: 1.37x slower                                                  |
| logging_simple             | 6.63 us                                                | 9.14 us: 1.38x slower                                                  |
| logging_format             | 7.35 us                                                | 10.2 us: 1.39x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 159 ms: 1.39x slower                                                   |
| float                      | 80.8 ms                                                | 113 ms: 1.39x slower                                                   |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                                   |
| django_template            | 34.7 ms                                                | 49.4 ms: 1.42x slower                                                  |
| nbody                      | 89.3 ms                                                | 128 ms: 1.44x slower                                                   |
| pyflate                    | 448 ms                                                 | 644 ms: 1.44x slower                                                   |
| richards_super             | 51.9 ms                                                | 75.2 ms: 1.45x slower                                                  |
| richards                   | 45.9 ms                                                | 67.2 ms: 1.46x slower                                                  |
| html5lib                   | 63.6 ms                                                | 93.6 ms: 1.47x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 329 us: 1.49x slower                                                   |
| chaos                      | 62.8 ms                                                | 94.2 ms: 1.50x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.55x slower                                                   |
| mako                       | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.57 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 498 us: 1.62x slower                                                   |
| logging_silent             | 109 ns                                                 | 177 ns: 1.63x slower                                                   |
| raytrace                   | 299 ms                                                 | 487 ms: 1.63x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.73 ms: 1.63x slower                                                  |
| scimark_sor                | 130 ms                                                 | 214 ms: 1.65x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                  |
| go                         | 139 ms                                                 | 238 ms: 1.71x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.36 ms: 1.74x slower                                                  |
| deltablue                  | 3.45 ms                                                | 7.37 ms: 2.14x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.30x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                           |

Benchmark hidden because not significant (2): coroutines, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.168x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.34x