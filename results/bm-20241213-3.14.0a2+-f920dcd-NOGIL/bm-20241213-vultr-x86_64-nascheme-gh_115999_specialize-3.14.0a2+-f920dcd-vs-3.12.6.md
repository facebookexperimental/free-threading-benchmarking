# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: f920dcd
- commit date: 2024-12-13
- overall geometric mean: 1.202x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                   |
| html5lib       | 63.6 ms                                                | 95.5 ms: 1.50x slower                                                    |
| Geometric mean | (ref)                                                  | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 763 ms: 1.46x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 788 ms: 1.37x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 328 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 416 ms: 1.35x faster                                                     |
| async_tree_none            | 464 ms                                                 | 363 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 444 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 612 ms: 1.17x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                    |
| async_generators           | 384 ms                                                 | 449 ms: 1.17x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| float          | 80.8 ms                                                | 115 ms: 1.42x slower                                                     |
| nbody          | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| Geometric mean | (ref)                                                  | 1.27x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                    |
| regex_compile  | 142 ms                                                 | 173 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.61 sec: 1.24x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.7 ms: 1.25x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 329 us: 1.49x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 503 us: 1.64x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.9 ms: 1.27x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                    |
| django_template | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                    |
| mako            | 11.0 ms                                                | 17.5 ms: 1.59x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.42x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 763 ms: 1.46x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 788 ms: 1.37x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 328 ms: 1.36x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 416 ms: 1.35x faster                                                     |
| async_tree_none            | 464 ms                                                 | 363 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 444 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 612 ms: 1.17x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| pathlib                    | 21.5 ms                                                | 20.0 ms: 1.08x faster                                                    |
| deepcopy                   | 352 us                                                 | 327 us: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 39.4 us: 1.02x faster                                                    |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                                     |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.51 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.97 sec: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| spectral_norm              | 110 ms                                                 | 123 ms: 1.12x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.47 us: 1.13x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 97.2 ms: 1.14x slower                                                    |
| docutils                   | 2.64 sec                                               | 3.08 sec: 1.17x slower                                                   |
| async_generators           | 384 ms                                                 | 449 ms: 1.17x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 92.5 ms: 1.17x slower                                                    |
| scimark_fft                | 342 ms                                                 | 401 ms: 1.17x slower                                                     |
| pylint                     | 319 ms                                                 | 376 ms: 1.18x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                    |
| generators                 | 32.2 ms                                                | 38.3 ms: 1.19x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.90 sec: 1.20x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 91.9 ms: 1.20x slower                                                    |
| regex_compile              | 142 ms                                                 | 173 ms: 1.21x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.42 sec: 1.21x slower                                                   |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.61 sec: 1.24x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 73.7 ms: 1.25x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.26x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 63.9 ms: 1.27x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 955 ms: 1.28x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 68.6 ms: 1.29x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.3 ms: 1.30x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.98 sec: 1.30x slower                                                   |
| telco                      | 6.53 ms                                                | 8.69 ms: 1.33x slower                                                    |
| thrift                     | 791 us                                                 | 1.06 ms: 1.34x slower                                                    |
| fannkuch                   | 372 ms                                                 | 498 ms: 1.34x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.95 ms: 1.35x slower                                                    |
| comprehensions             | 19.8 us                                                | 27.2 us: 1.37x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.2 ms: 1.37x slower                                                    |
| genshi_text                | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                    |
| 2to3                       | 264 ms                                                 | 366 ms: 1.39x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 199 ms: 1.40x slower                                                     |
| float                      | 80.8 ms                                                | 115 ms: 1.42x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.43x slower                                                    |
| coverage                   | 71.4 ms                                                | 103 ms: 1.44x slower                                                     |
| nbody                      | 89.3 ms                                                | 130 ms: 1.46x slower                                                     |
| django_template            | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                    |
| richards_super             | 51.9 ms                                                | 76.2 ms: 1.47x slower                                                    |
| richards                   | 45.9 ms                                                | 67.8 ms: 1.47x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 329 us: 1.49x slower                                                     |
| html5lib                   | 63.6 ms                                                | 95.5 ms: 1.50x slower                                                    |
| pyflate                    | 448 ms                                                 | 676 ms: 1.51x slower                                                     |
| logging_simple             | 6.63 us                                                | 10.1 us: 1.52x slower                                                    |
| logging_format             | 7.35 us                                                | 11.3 us: 1.53x slower                                                    |
| chaos                      | 62.8 ms                                                | 97.2 ms: 1.55x slower                                                    |
| hexiom                     | 6.17 ms                                                | 9.72 ms: 1.58x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 108 ms: 1.58x slower                                                     |
| mako                       | 11.0 ms                                                | 17.5 ms: 1.59x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 183 ms: 1.60x slower                                                     |
| sympy_str                  | 292 ms                                                 | 474 ms: 1.63x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 503 us: 1.64x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 2.74 ms: 1.64x slower                                                    |
| raytrace                   | 299 ms                                                 | 498 ms: 1.67x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                    |
| logging_silent             | 109 ns                                                 | 185 ns: 1.70x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 2.37 ms: 1.75x slower                                                    |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.75x slower                                                    |
| go                         | 139 ms                                                 | 245 ms: 1.76x slower                                                     |
| scimark_sor                | 130 ms                                                 | 235 ms: 1.81x slower                                                     |
| sympy_expand               | 468 ms                                                 | 950 ms: 2.03x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.10x slower                                                     |
| deltablue                  | 3.45 ms                                                | 7.49 ms: 2.17x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.43 ms: 3.65x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.02x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.30x slower                                                             |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-f920dcd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.202x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.20x
- 95% likely to have a slowdown of 1.19x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.33x