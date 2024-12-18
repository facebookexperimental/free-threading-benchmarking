# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.81x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.72x faster                                                     |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 547 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 569 ms: 1.26x faster                                                     |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                    |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                    |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 165 ms: 1.01x faster                                                     |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 26.2 us: 1.01x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 320 us: 1.04x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                    |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                    |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.81x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.81x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 628 ms: 1.72x faster                                                     |
| async_tree_none            | 464 ms                                                 | 278 ms: 1.67x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                     |
| deepcopy                   | 352 us                                                 | 254 us: 1.38x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 547 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 569 ms: 1.26x faster                                                     |
| generators                 | 32.2 ms                                                | 26.9 ms: 1.20x faster                                                    |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                    |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 66.2 ms: 1.16x faster                                                    |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                     |
| spectral_norm              | 110 ms                                                 | 97.2 ms: 1.13x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                    |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.12x faster                                                    |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.27 sec: 1.11x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.10 us: 1.09x faster                                                    |
| scimark_fft                | 342 ms                                                 | 315 ms: 1.09x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.17 ms: 1.09x faster                                                    |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                    |
| thrift                     | 791 us                                                 | 733 us: 1.08x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                    |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                     |
| chaos                      | 62.8 ms                                                | 58.4 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                   |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 91.2 ms: 1.06x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.28 ms: 1.06x faster                                                    |
| float                      | 80.8 ms                                                | 76.4 ms: 1.06x faster                                                    |
| pyflate                    | 448 ms                                                 | 425 ms: 1.05x faster                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.59 ms: 1.05x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 706 ms: 1.05x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.05x faster                                                     |
| json                       | 5.02 ms                                                | 4.78 ms: 1.05x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.45 sec: 1.05x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                   |
| richards                   | 45.9 ms                                                | 43.9 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.5 ms: 1.04x faster                                                    |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.9 ms: 1.04x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.95 ms: 1.04x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                     |
| richards_super             | 51.9 ms                                                | 50.1 ms: 1.04x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                     |
| logging_silent             | 109 ns                                                 | 105 ns: 1.03x faster                                                     |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.03x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| sympy_expand               | 468 ms                                                 | 454 ms: 1.03x faster                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.29 ms: 1.02x faster                                                    |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 52.3 ms: 1.02x faster                                                    |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.02x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                    |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.01x faster                                                     |
| json_loads                 | 26.5 us                                                | 26.2 us: 1.01x faster                                                    |
| nqueens                    | 80.1 ms                                                | 79.0 ms: 1.01x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 58.2 ms: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                     |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                    |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 320 us: 1.04x slower                                                     |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| coverage                   | 71.4 ms                                                | 78.3 ms: 1.10x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                    |
| telco                      | 6.53 ms                                                | 7.21 ms: 1.11x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                    |
| pidigits                   | 184 ms                                                 | 217 ms: 1.18x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.42 ms: 1.28x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 88.5 ms: 8.20x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (3): genshi_xml, sqlite_synth, nbody
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-699f4e9/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x