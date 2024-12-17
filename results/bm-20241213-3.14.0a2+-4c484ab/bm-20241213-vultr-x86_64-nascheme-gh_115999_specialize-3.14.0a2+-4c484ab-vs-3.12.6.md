# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 4c484ab
- commit date: 2024-12-13
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 627 ms: 1.73x faster                                                     |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.66x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 550 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 572 ms: 1.25x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                    |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                    |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                    |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 166 ms: 1.01x faster                                                     |
| regex_v8       | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 213 us: 1.03x faster                                                     |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 84.2 ms: 1.01x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 318 us: 1.03x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                    |
| django_template | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                    |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 627 ms: 1.73x faster                                                     |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.66x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                     |
| deepcopy                   | 352 us                                                 | 256 us: 1.37x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 550 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 572 ms: 1.25x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                    |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                                    |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                     |
| spectral_norm              | 110 ms                                                 | 94.8 ms: 1.16x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.15x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.2 us: 1.15x faster                                                    |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 66.7 ms: 1.15x faster                                                    |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.12x faster                                                    |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                                     |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 130 ms: 1.10x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.10x faster                                                     |
| chaos                      | 62.8 ms                                                | 57.4 ms: 1.09x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 62.7 ms: 1.09x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                    |
| async_generators           | 384 ms                                                 | 354 ms: 1.09x faster                                                     |
| thrift                     | 791 us                                                 | 729 us: 1.09x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.20 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.18 us: 1.07x faster                                                    |
| logging_format             | 7.35 us                                                | 6.85 us: 1.07x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.26 ms: 1.07x faster                                                    |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.07x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.58 ms: 1.06x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                    |
| json                       | 5.02 ms                                                | 4.76 ms: 1.06x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.05x faster                                                     |
| pyflate                    | 448 ms                                                 | 425 ms: 1.05x faster                                                     |
| float                      | 80.8 ms                                                | 76.8 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.20 ms: 1.05x faster                                                    |
| meteor_contest             | 104 ms                                                 | 98.9 ms: 1.05x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.90 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.5 ms: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 213 us: 1.03x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 721 ms: 1.03x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                   |
| genshi_text                | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                    |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| nqueens                    | 80.1 ms                                                | 77.9 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.02x faster                                                     |
| sympy_expand               | 468 ms                                                 | 458 ms: 1.02x faster                                                     |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 52.3 ms: 1.02x faster                                                    |
| json_loads                 | 26.5 us                                                | 26.1 us: 1.02x faster                                                    |
| richards                   | 45.9 ms                                                | 45.2 ms: 1.02x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 84.2 ms: 1.01x faster                                                    |
| regex_dna                  | 168 ms                                                 | 166 ms: 1.01x faster                                                     |
| scimark_sor                | 130 ms                                                 | 129 ms: 1.01x faster                                                     |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 50.6 ms: 1.01x slower                                                    |
| django_template            | 34.7 ms                                                | 35.0 ms: 1.01x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.48 sec: 1.03x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 318 us: 1.03x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.52 ms: 1.05x slower                                                    |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 78.6 ms: 1.10x slower                                                    |
| telco                      | 6.53 ms                                                | 7.27 ms: 1.11x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.5 ms: 1.14x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.04 ms: 1.17x slower                                                    |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                                     |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 89.3 ms: 8.27x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (4): richards_super, fannkuch, nbody, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-4c484ab.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x