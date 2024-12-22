# Results vs. 3.12.6

- fork: Yhg1s
- ref: optimise_recursive_c
- machine: linux-x86_64
- commit hash: b28153d
- commit date: 2024-12-20
- overall geometric mean: 1.168x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 350 ms: 1.33x slower                                                  |
| docutils       | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                |
| html5lib       | 63.6 ms                                                | 90.2 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                  | 1.29x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 756 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 318 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 575 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| float          | 80.8 ms                                                | 112 ms: 1.38x slower                                                  |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                  | 1.26x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                 |
| regex_dna      | 168 ms                                                 | 179 ms: 1.06x slower                                                  |
| regex_compile  | 142 ms                                                 | 169 ms: 1.18x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.52 sec: 1.19x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                 |
| json_dumps           | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 330 us: 1.49x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 499 us: 1.62x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.6 ms: 1.27x slower                                                 |
| genshi_text     | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                 |
| django_template | 34.7 ms                                                | 48.6 ms: 1.40x slower                                                 |
| mako            | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 756 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 318 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 403 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 575 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                 |
| deepcopy                   | 352 us                                                 | 323 us: 1.09x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.12 us: 1.04x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 40.6 us: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.2 ms: 1.01x slower                                                 |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 5.02 sec: 1.06x slower                                                |
| json_loads                 | 26.5 us                                                | 28.1 us: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.06x slower                                                  |
| pylint                     | 319 ms                                                 | 349 ms: 1.09x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.38 us: 1.10x slower                                                 |
| scimark_fft                | 342 ms                                                 | 379 ms: 1.11x slower                                                  |
| docutils                   | 2.64 sec                                               | 3.00 sec: 1.14x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.0 ms: 1.14x slower                                                 |
| dulwich_log                | 78.9 ms                                                | 90.7 ms: 1.15x slower                                                 |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.81 sec: 1.16x slower                                                |
| generators                 | 32.2 ms                                                | 37.7 ms: 1.17x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.7 ms: 1.17x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.18x slower                                                  |
| regex_compile              | 142 ms                                                 | 169 ms: 1.18x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.39 sec: 1.19x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.52 sec: 1.19x slower                                                |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                 |
| sympy_str                  | 292 ms                                                 | 359 ms: 1.23x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 25.3 ms: 1.23x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 65.9 ms: 1.24x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 73.0 ms: 1.24x slower                                                 |
| nqueens                    | 80.1 ms                                                | 99.1 ms: 1.24x slower                                                 |
| thrift                     | 791 us                                                 | 990 us: 1.25x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                                 |
| sympy_expand               | 468 ms                                                 | 591 ms: 1.26x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 63.6 ms: 1.27x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.6 ms: 1.27x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 207 us: 1.27x slower                                                  |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.27x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 963 ms: 1.30x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.32x slower                                                |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                                  |
| 2to3                       | 264 ms                                                 | 350 ms: 1.33x slower                                                  |
| genshi_text                | 22.8 ms                                                | 30.6 ms: 1.34x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 14.0 ms: 1.35x slower                                                 |
| telco                      | 6.53 ms                                                | 8.82 ms: 1.35x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 155 ms: 1.36x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                                 |
| logging_simple             | 6.63 us                                                | 9.10 us: 1.37x slower                                                 |
| comprehensions             | 19.8 us                                                | 27.3 us: 1.38x slower                                                 |
| float                      | 80.8 ms                                                | 112 ms: 1.38x slower                                                  |
| logging_format             | 7.35 us                                                | 10.2 us: 1.39x slower                                                 |
| coverage                   | 71.4 ms                                                | 99.3 ms: 1.39x slower                                                 |
| django_template            | 34.7 ms                                                | 48.6 ms: 1.40x slower                                                 |
| html5lib                   | 63.6 ms                                                | 90.2 ms: 1.42x slower                                                 |
| richards_super             | 51.9 ms                                                | 74.7 ms: 1.44x slower                                                 |
| pyflate                    | 448 ms                                                 | 648 ms: 1.45x slower                                                  |
| richards                   | 45.9 ms                                                | 66.6 ms: 1.45x slower                                                 |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                                  |
| chaos                      | 62.8 ms                                                | 93.9 ms: 1.49x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 330 us: 1.49x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 105 ms: 1.54x slower                                                  |
| hexiom                     | 6.17 ms                                                | 9.52 ms: 1.54x slower                                                 |
| mako                       | 11.0 ms                                                | 17.0 ms: 1.55x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 2.69 ms: 1.61x slower                                                 |
| raytrace                   | 299 ms                                                 | 483 ms: 1.61x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 499 us: 1.62x slower                                                  |
| scimark_sor                | 130 ms                                                 | 214 ms: 1.65x slower                                                  |
| logging_silent             | 109 ns                                                 | 180 ns: 1.66x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                 |
| go                         | 139 ms                                                 | 236 ms: 1.69x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 2.34 ms: 1.73x slower                                                 |
| deltablue                  | 3.45 ms                                                | 7.31 ms: 2.12x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.61x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.27x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241220-3.14.0a3+-b28153d-NOGIL/bm-20241220-vultr-x86_64-Yhg1s-optimise_recursive_c-3.14.0a3+-b28153d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.168x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.33x