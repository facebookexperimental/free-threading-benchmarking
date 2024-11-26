# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.039x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 332 ms: 1.40x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 407 ms: 1.36x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 568 ms: 1.27x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 860 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 570 ms: 1.26x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 889 ms: 1.25x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                    |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.7 ms: 1.01x faster                                                    |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                     |
| nbody          | 89.3 ms                                                | 94.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                                     |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 24.8 us: 1.07x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 137 ms: 1.01x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 86.0 ms: 1.01x slower                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 98.3 ms: 1.02x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 60.0 ms: 1.02x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.04x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.1 ms: 1.03x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 50.7 ms: 1.01x slower                                                    |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                    |
| mako            | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 332 ms: 1.40x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 407 ms: 1.36x faster                                                     |
| deepcopy                   | 352 us                                                 | 262 us: 1.34x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.5 us: 1.32x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 568 ms: 1.27x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 860 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 570 ms: 1.26x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 889 ms: 1.25x faster                                                     |
| pylint                     | 319 ms                                                 | 270 ms: 1.18x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                    |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.17x faster                                                    |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 67.0 ms: 1.14x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.14x faster                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                     |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.5 ms: 1.12x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| regex_compile              | 142 ms                                                 | 129 ms: 1.10x faster                                                     |
| json                       | 5.02 ms                                                | 4.56 ms: 1.10x faster                                                    |
| generators                 | 32.2 ms                                                | 29.8 ms: 1.08x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                   |
| json_loads                 | 26.5 us                                                | 24.8 us: 1.07x faster                                                    |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                     |
| chaos                      | 62.8 ms                                                | 58.9 ms: 1.07x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                    |
| deltablue                  | 3.45 ms                                                | 3.25 ms: 1.06x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.30 us: 1.05x faster                                                    |
| thrift                     | 791 us                                                 | 752 us: 1.05x faster                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.6 ms: 1.04x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 65.8 ms: 1.04x faster                                                    |
| meteor_contest             | 104 ms                                                 | 99.7 ms: 1.04x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.94 ms: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                   |
| genshi_text                | 22.8 ms                                                | 22.1 ms: 1.03x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 720 ms: 1.03x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                   |
| logging_format             | 7.35 us                                                | 7.13 us: 1.03x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                     |
| 2to3                       | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                                     |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                     |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                     |
| scimark_fft                | 342 ms                                                 | 336 ms: 1.02x faster                                                     |
| nqueens                    | 80.1 ms                                                | 78.9 ms: 1.01x faster                                                    |
| sympy_expand               | 468 ms                                                 | 461 ms: 1.01x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 137 ms: 1.01x faster                                                     |
| float                      | 80.8 ms                                                | 79.7 ms: 1.01x faster                                                    |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 107 ms: 1.00x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 53.6 ms: 1.01x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 86.0 ms: 1.01x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 50.7 ms: 1.01x slower                                                    |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 98.3 ms: 1.02x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 60.0 ms: 1.02x slower                                                    |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.50 sec: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.40 ms: 1.03x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.04x slower                                                     |
| nbody                      | 89.3 ms                                                | 94.2 ms: 1.05x slower                                                    |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.06x slower                                                    |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.06x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.69 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| telco                      | 6.53 ms                                                | 7.37 ms: 1.13x slower                                                    |
| coverage                   | 71.4 ms                                                | 82.2 ms: 1.15x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.24 ms: 1.23x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 86.2 ms: 7.98x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (5): richards, tomli_loads, richards_super, pyflate, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241125-3.14.0a2+-a515a0d/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.039x faster
# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x