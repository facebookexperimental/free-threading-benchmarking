# Results vs. 3.12.6

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.228x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 369 ms: 1.40x slower                                                   |
| docutils       | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                 |
| html5lib       | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                  | 1.37x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 822 ms: 1.35x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 447 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                                   |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 468 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 614 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 636 ms: 1.12x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                  |
| async_generators           | 384 ms                                                 | 466 ms: 1.21x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| float          | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                  |
| regex_compile  | 142 ms                                                 | 181 ms: 1.27x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.5 ms: 1.08x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 78.6 ms: 1.33x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 339 us: 1.54x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 509 us: 1.66x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.6 ms: 1.27x slower                                                  |
| genshi_text     | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                  |
| django_template | 34.7 ms                                                | 51.0 ms: 1.47x slower                                                  |
| mako            | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.43x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 822 ms: 1.35x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 850 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 447 ms: 1.25x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 357 ms: 1.25x faster                                                   |
| async_tree_none            | 464 ms                                                 | 387 ms: 1.20x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 468 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 614 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 636 ms: 1.12x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 3.17 ms: 1.09x faster                                                  |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 89.5 ms: 1.08x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 39.9 us: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.27 us: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.2 ms: 1.05x slower                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.98 sec: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.49 us: 1.14x slower                                                  |
| spectral_norm              | 110 ms                                                 | 126 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                  |
| scimark_fft                | 342 ms                                                 | 403 ms: 1.18x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.11 sec: 1.18x slower                                                 |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                  |
| pylint                     | 319 ms                                                 | 383 ms: 1.20x slower                                                   |
| async_generators           | 384 ms                                                 | 466 ms: 1.21x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 96.0 ms: 1.22x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 93.5 ms: 1.22x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.97 sec: 1.23x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 25.3 ms: 1.23x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.4 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 204 us: 1.25x slower                                                   |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.25x slower                                                   |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 63.6 ms: 1.27x slower                                                  |
| regex_compile              | 142 ms                                                 | 181 ms: 1.27x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.69 sec: 1.28x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 68.1 ms: 1.28x slower                                                  |
| telco                      | 6.53 ms                                                | 8.62 ms: 1.32x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 78.6 ms: 1.33x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 991 ms: 1.33x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.56 sec: 1.34x slower                                                 |
| fannkuch                   | 372 ms                                                 | 499 ms: 1.34x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 2.05 sec: 1.35x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.95 ms: 1.36x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.6 ms: 1.36x slower                                                  |
| genshi_text                | 22.8 ms                                                | 31.4 ms: 1.38x slower                                                  |
| comprehensions             | 19.8 us                                                | 27.6 us: 1.39x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 14.4 ms: 1.39x slower                                                  |
| coverage                   | 71.4 ms                                                | 99.7 ms: 1.40x slower                                                  |
| 2to3                       | 264 ms                                                 | 369 ms: 1.40x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 204 ms: 1.43x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 29.7 ms: 1.45x slower                                                  |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                   |
| django_template            | 34.7 ms                                                | 51.0 ms: 1.47x slower                                                  |
| thrift                     | 791 us                                                 | 1.17 ms: 1.47x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 339 us: 1.54x slower                                                   |
| pyflate                    | 448 ms                                                 | 692 ms: 1.54x slower                                                   |
| html5lib                   | 63.6 ms                                                | 99.2 ms: 1.56x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 185 ms: 1.62x slower                                                   |
| mako                       | 11.0 ms                                                | 17.8 ms: 1.62x slower                                                  |
| hexiom                     | 6.17 ms                                                | 10.0 ms: 1.62x slower                                                  |
| sympy_str                  | 292 ms                                                 | 479 ms: 1.64x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.79 ms: 1.64x slower                                                  |
| logging_simple             | 6.63 us                                                | 10.9 us: 1.65x slower                                                  |
| logging_format             | 7.35 us                                                | 12.1 us: 1.65x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 509 us: 1.66x slower                                                   |
| richards_super             | 51.9 ms                                                | 87.4 ms: 1.69x slower                                                  |
| chaos                      | 62.8 ms                                                | 106 ms: 1.69x slower                                                   |
| richards                   | 45.9 ms                                                | 78.2 ms: 1.70x slower                                                  |
| logging_silent             | 109 ns                                                 | 188 ns: 1.73x slower                                                   |
| float                      | 80.8 ms                                                | 140 ms: 1.73x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 120 ms: 1.75x slower                                                   |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 2.98 ms: 1.79x slower                                                  |
| scimark_sor                | 130 ms                                                 | 239 ms: 1.84x slower                                                   |
| raytrace                   | 299 ms                                                 | 566 ms: 1.89x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 2.61 ms: 1.92x slower                                                  |
| go                         | 139 ms                                                 | 276 ms: 1.98x slower                                                   |
| sympy_expand               | 468 ms                                                 | 959 ms: 2.05x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 352 ms: 2.12x slower                                                   |
| deltablue                  | 3.45 ms                                                | 8.33 ms: 2.42x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.65x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 109 ms: 10.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.34x slower                                                           |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.228x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.33x