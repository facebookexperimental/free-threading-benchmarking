# Results vs. 3.12.6

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.058x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                 |
| html5lib       | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                   |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.3 ms: 1.05x faster                                                  |
| pidigits       | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| nbody          | 89.3 ms                                                | 128 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 250 us: 1.13x slower                                                   |
| json_loads           | 26.5 us                                                | 30.2 us: 1.14x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.7 ms: 1.21x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                  |
| django_template | 34.7 ms                                                | 43.5 ms: 1.25x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 351 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                  |
| deepcopy                   | 352 us                                                 | 311 us: 1.13x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.5 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                   |
| spectral_norm              | 110 ms                                                 | 105 ms: 1.05x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 38.5 us: 1.05x faster                                                  |
| float                      | 80.8 ms                                                | 77.3 ms: 1.05x faster                                                  |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.66 sec: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                   |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.0 ms: 1.04x slower                                                  |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                   |
| json                       | 5.02 ms                                                | 5.29 ms: 1.05x slower                                                  |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.69 ms: 1.07x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.32 us: 1.08x slower                                                  |
| logging_silent             | 109 ns                                                 | 119 ns: 1.09x slower                                                   |
| pyflate                    | 448 ms                                                 | 492 ms: 1.10x slower                                                   |
| chaos                      | 62.8 ms                                                | 69.0 ms: 1.10x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 205 ms: 1.11x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.39 us: 1.12x slower                                                  |
| raytrace                   | 299 ms                                                 | 335 ms: 1.12x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 831 ms: 1.12x slower                                                   |
| scimark_fft                | 342 ms                                                 | 382 ms: 1.12x slower                                                   |
| html5lib                   | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                  |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 95.8 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.71 sec: 1.13x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 250 us: 1.13x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 86.8 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                   |
| json_loads                 | 26.5 us                                                | 30.2 us: 1.14x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                                 |
| logging_format             | 7.35 us                                                | 8.45 us: 1.15x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                                   |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 61.6 ms: 1.16x slower                                                  |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.94 ms: 1.16x slower                                                  |
| thrift                     | 791 us                                                 | 920 us: 1.16x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                  |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                                   |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.61 ms: 1.19x slower                                                  |
| nqueens                    | 80.1 ms                                                | 95.0 ms: 1.19x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.36 ms: 1.19x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 60.7 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 82.8 ms: 1.21x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 198 us: 1.21x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.22x slower                                                  |
| richards                   | 45.9 ms                                                | 56.7 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.47 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.25x slower                                                   |
| django_template            | 34.7 ms                                                | 43.5 ms: 1.25x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                  |
| fannkuch                   | 372 ms                                                 | 472 ms: 1.27x slower                                                   |
| richards_super             | 51.9 ms                                                | 66.0 ms: 1.27x slower                                                  |
| telco                      | 6.53 ms                                                | 8.36 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.37x slower                                                  |
| deltablue                  | 3.45 ms                                                | 4.73 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| nbody                      | 89.3 ms                                                | 128 ms: 1.43x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.51x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 94.7 ms: 8.77x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (2): pylint, coroutines
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x