# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.197x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 365 ms: 1.39x slower                                                     |
| docutils       | 2.64 sec                                               | 3.07 sec: 1.17x slower                                                   |
| html5lib       | 63.6 ms                                                | 95.0 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                  | 1.34x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 765 ms: 1.45x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 793 ms: 1.37x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 329 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 420 ms: 1.33x faster                                                     |
| async_tree_none            | 464 ms                                                 | 362 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 446 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 593 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 620 ms: 1.15x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                    |
| async_generators           | 384 ms                                                 | 438 ms: 1.14x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| float          | 80.8 ms                                                | 113 ms: 1.40x slower                                                     |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                                     |
| Geometric mean | (ref)                                                  | 1.25x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                    |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                    |
| regex_compile  | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                    |
| tomli_loads          | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                    |
| json_dumps           | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 326 us: 1.48x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 492 us: 1.60x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| python_startup         | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.2 ms: 1.37x slower                                                    |
| django_template | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                    |
| mako            | 11.0 ms                                                | 17.6 ms: 1.60x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 765 ms: 1.45x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 793 ms: 1.37x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 329 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 420 ms: 1.33x faster                                                     |
| async_tree_none            | 464 ms                                                 | 362 ms: 1.28x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 446 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 593 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 620 ms: 1.15x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                    |
| deepcopy                   | 352 us                                                 | 323 us: 1.09x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                    |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 38.8 us: 1.04x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.1 ms: 1.01x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.52 ms: 1.02x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.93 sec: 1.04x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                    |
| spectral_norm              | 110 ms                                                 | 120 ms: 1.09x slower                                                     |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.45 us: 1.12x slower                                                    |
| scimark_fft                | 342 ms                                                 | 384 ms: 1.12x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 96.5 ms: 1.13x slower                                                    |
| async_generators           | 384 ms                                                 | 438 ms: 1.14x slower                                                     |
| docutils                   | 2.64 sec                                               | 3.07 sec: 1.17x slower                                                   |
| generators                 | 32.2 ms                                                | 37.6 ms: 1.17x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 90.0 ms: 1.17x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 92.9 ms: 1.18x slower                                                    |
| pylint                     | 319 ms                                                 | 376 ms: 1.18x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.89 sec: 1.20x slower                                                   |
| regex_compile              | 142 ms                                                 | 172 ms: 1.21x slower                                                     |
| nqueens                    | 80.1 ms                                                | 96.8 ms: 1.21x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.43 sec: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.39 ms: 1.23x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.60 sec: 1.23x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 73.1 ms: 1.24x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 62.9 ms: 1.25x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 68.3 ms: 1.28x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 962 ms: 1.30x slower                                                     |
| thrift                     | 791 us                                                 | 1.03 ms: 1.30x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 28.5 ms: 1.31x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 2.00 sec: 1.32x slower                                                   |
| fannkuch                   | 372 ms                                                 | 492 ms: 1.32x slower                                                     |
| telco                      | 6.53 ms                                                | 8.70 ms: 1.33x slower                                                    |
| comprehensions             | 19.8 us                                                | 26.8 us: 1.35x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 14.1 ms: 1.36x slower                                                    |
| genshi_text                | 22.8 ms                                                | 31.2 ms: 1.37x slower                                                    |
| 2to3                       | 264 ms                                                 | 365 ms: 1.39x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 199 ms: 1.39x slower                                                     |
| float                      | 80.8 ms                                                | 113 ms: 1.40x slower                                                     |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 29.5 ms: 1.43x slower                                                    |
| richards                   | 45.9 ms                                                | 66.8 ms: 1.45x slower                                                    |
| richards_super             | 51.9 ms                                                | 75.4 ms: 1.45x slower                                                    |
| coverage                   | 71.4 ms                                                | 104 ms: 1.46x slower                                                     |
| django_template            | 34.7 ms                                                | 50.5 ms: 1.46x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 326 us: 1.48x slower                                                     |
| html5lib                   | 63.6 ms                                                | 95.0 ms: 1.49x slower                                                    |
| pyflate                    | 448 ms                                                 | 673 ms: 1.50x slower                                                     |
| logging_simple             | 6.63 us                                                | 9.97 us: 1.50x slower                                                    |
| logging_format             | 7.35 us                                                | 11.1 us: 1.51x slower                                                    |
| chaos                      | 62.8 ms                                                | 95.0 ms: 1.51x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 105 ms: 1.53x slower                                                     |
| hexiom                     | 6.17 ms                                                | 9.63 ms: 1.56x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 180 ms: 1.58x slower                                                     |
| mako                       | 11.0 ms                                                | 17.6 ms: 1.60x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 492 us: 1.60x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 2.69 ms: 1.61x slower                                                    |
| sympy_str                  | 292 ms                                                 | 474 ms: 1.62x slower                                                     |
| raytrace                   | 299 ms                                                 | 489 ms: 1.63x slower                                                     |
| logging_silent             | 109 ns                                                 | 180 ns: 1.65x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.33 ms: 1.72x slower                                                    |
| go                         | 139 ms                                                 | 241 ms: 1.73x slower                                                     |
| python_startup             | 9.93 ms                                                | 17.4 ms: 1.76x slower                                                    |
| scimark_sor                | 130 ms                                                 | 230 ms: 1.77x slower                                                     |
| sympy_expand               | 468 ms                                                 | 952 ms: 2.03x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 348 ms: 2.09x slower                                                     |
| deltablue                  | 3.45 ms                                                | 7.35 ms: 2.13x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.41 ms: 3.63x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.01x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.29x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.197x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.16x

# Memory
- memory change: 1.33x