# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: f920dcd
- commit date: 2024-12-13
- overall geometric mean: 1.228x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                   |
| html5lib       | 67.0 ms                                                      | 95.5 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                        | 1.33x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                     |
| async_tree_io              | 876 ms                                                       | 788 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 612 ms: 1.09x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 444 ms: 1.04x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 328 ms: 1.03x faster                                                     |
| async_tree_none            | 354 ms                                                       | 363 ms: 1.03x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                    |
| async_generators           | 377 ms                                                       | 449 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| float          | 77.5 ms                                                      | 115 ms: 1.48x slower                                                     |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| Geometric mean | (ref)                                                        | 1.24x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| regex_dna      | 180 ms                                                       | 181 ms: 1.01x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                    |
| regex_compile  | 132 ms                                                       | 173 ms: 1.31x slower                                                     |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.0 ms: 1.05x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 73.7 ms: 1.24x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.61 sec: 1.30x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 329 us: 1.57x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 503 us: 1.71x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.23x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.9 ms: 1.31x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 31.6 ms: 1.47x slower                                                    |
| django_template | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                    |
| mako            | 11.3 ms                                                      | 17.5 ms: 1.54x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                     |
| pidigits                   | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| async_tree_io              | 876 ms                                                       | 788 ms: 1.11x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 612 ms: 1.09x faster                                                     |
| deepcopy                   | 355 us                                                       | 327 us: 1.09x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.0 ms: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 444 ms: 1.04x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 328 ms: 1.03x faster                                                     |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.01x slower                                                     |
| deepcopy_memo              | 39.1 us                                                      | 39.4 us: 1.01x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                    |
| async_tree_none            | 354 ms                                                       | 363 ms: 1.03x slower                                                     |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 20.0 ms: 1.04x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.07x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.69 ms: 1.11x slower                                                    |
| spectral_norm              | 111 ms                                                       | 123 ms: 1.11x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.47 us: 1.11x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.51 ms: 1.12x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 97.2 ms: 1.14x slower                                                    |
| scimark_fft                | 349 ms                                                       | 401 ms: 1.15x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                   |
| pylint                     | 317 ms                                                       | 376 ms: 1.19x slower                                                     |
| async_generators           | 377 ms                                                       | 449 ms: 1.19x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.90 sec: 1.23x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 92.5 ms: 1.24x slower                                                    |
| coverage                   | 83.0 ms                                                      | 103 ms: 1.24x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 73.7 ms: 1.24x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 98.1 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.95 ms: 1.26x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 134 ms: 1.27x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.42 sec: 1.27x slower                                                   |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 955 ms: 1.29x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.61 sec: 1.30x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 68.6 ms: 1.30x slower                                                    |
| regex_compile              | 132 ms                                                       | 173 ms: 1.31x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 63.9 ms: 1.31x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.98 sec: 1.32x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.3 ms: 1.33x slower                                                    |
| fannkuch                   | 370 ms                                                       | 498 ms: 1.35x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 91.9 ms: 1.35x slower                                                    |
| thrift                     | 778 us                                                       | 1.06 ms: 1.36x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                    |
| 2to3                       | 260 ms                                                       | 366 ms: 1.41x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 95.5 ms: 1.42x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 31.6 ms: 1.47x slower                                                    |
| richards_super             | 51.6 ms                                                      | 76.2 ms: 1.48x slower                                                    |
| float                      | 77.5 ms                                                      | 115 ms: 1.48x slower                                                     |
| django_template            | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                    |
| richards                   | 45.2 ms                                                      | 67.8 ms: 1.50x slower                                                    |
| pyflate                    | 449 ms                                                       | 676 ms: 1.51x slower                                                     |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                     |
| mako                       | 11.3 ms                                                      | 17.5 ms: 1.54x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 329 us: 1.57x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 183 ms: 1.62x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 9.72 ms: 1.62x slower                                                    |
| logging_simple             | 6.16 us                                                      | 10.1 us: 1.64x slower                                                    |
| logging_format             | 6.84 us                                                      | 11.3 us: 1.65x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.2 us: 1.65x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 108 ms: 1.65x slower                                                     |
| chaos                      | 57.3 ms                                                      | 97.2 ms: 1.70x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 503 us: 1.71x slower                                                     |
| sympy_str                  | 275 ms                                                       | 474 ms: 1.73x slower                                                     |
| go                         | 141 ms                                                       | 245 ms: 1.74x slower                                                     |
| scimark_sor                | 134 ms                                                       | 235 ms: 1.75x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 2.74 ms: 1.76x slower                                                    |
| logging_silent             | 103 ns                                                       | 185 ns: 1.81x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.37 ms: 1.90x slower                                                    |
| raytrace                   | 253 ms                                                       | 498 ms: 1.97x slower                                                     |
| sympy_expand               | 457 ms                                                       | 950 ms: 2.08x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 7.49 ms: 2.40x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.43 ms: 3.74x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.84x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.34x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.228x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.32x