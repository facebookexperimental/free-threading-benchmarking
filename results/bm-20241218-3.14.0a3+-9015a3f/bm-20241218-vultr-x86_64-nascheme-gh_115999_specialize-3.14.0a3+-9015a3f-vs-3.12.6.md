# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 9015a3f
- commit date: 2024-12-18
- overall geometric mean: 1.082x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                     |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.67x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 581 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 602 ms: 1.19x faster                                                     |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.42x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                    |
| pidigits       | 184 ms                                                 | 222 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                    |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 169 ms: 1.00x slower                                                     |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                    |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                    |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                                     |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.67x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 335 ms: 1.66x faster                                                     |
| deepcopy                   | 352 us                                                 | 254 us: 1.38x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 29.3 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 581 ms: 1.24x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                    |
| generators                 | 32.2 ms                                                | 26.8 ms: 1.20x faster                                                    |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 602 ms: 1.19x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                    |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                     |
| comprehensions             | 19.8 us                                                | 17.1 us: 1.16x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 66.4 ms: 1.15x faster                                                    |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.4 ms: 1.13x faster                                                    |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.25 sec: 1.12x faster                                                   |
| spectral_norm              | 110 ms                                                 | 99.0 ms: 1.11x faster                                                    |
| deltablue                  | 3.45 ms                                                | 3.13 ms: 1.10x faster                                                    |
| chaos                      | 62.8 ms                                                | 57.2 ms: 1.10x faster                                                    |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 62.5 ms: 1.09x faster                                                    |
| async_generators           | 384 ms                                                 | 352 ms: 1.09x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.2 ms: 1.08x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.26 ms: 1.07x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.77 ms: 1.07x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.20 us: 1.07x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.07x faster                                                    |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                     |
| pyflate                    | 448 ms                                                 | 420 ms: 1.07x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                     |
| logging_format             | 7.35 us                                                | 6.90 us: 1.06x faster                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.57 ms: 1.06x faster                                                    |
| thrift                     | 791 us                                                 | 746 us: 1.06x faster                                                     |
| json                       | 5.02 ms                                                | 4.75 ms: 1.06x faster                                                    |
| richards                   | 45.9 ms                                                | 43.5 ms: 1.06x faster                                                    |
| float                      | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                    |
| meteor_contest             | 104 ms                                                 | 98.2 ms: 1.05x faster                                                    |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 75.2 ms: 1.05x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 710 ms: 1.05x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.22 ms: 1.04x faster                                                    |
| richards_super             | 51.9 ms                                                | 49.9 ms: 1.04x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.03x faster                                                     |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.03x faster                                                     |
| nqueens                    | 80.1 ms                                                | 77.7 ms: 1.03x faster                                                    |
| 2to3                       | 264 ms                                                 | 256 ms: 1.03x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                    |
| sympy_expand               | 468 ms                                                 | 457 ms: 1.02x faster                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 52.1 ms: 1.02x faster                                                    |
| json_loads                 | 26.5 us                                                | 26.0 us: 1.02x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 49.3 ms: 1.02x faster                                                    |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.02x faster                                                     |
| fannkuch                   | 372 ms                                                 | 371 ms: 1.00x faster                                                     |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.00x slower                                                     |
| django_template            | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.44 sec: 1.01x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                     |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| telco                      | 6.53 ms                                                | 7.16 ms: 1.10x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 79.4 ms: 1.11x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                    |
| pidigits                   | 184 ms                                                 | 222 ms: 1.21x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.48x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 88.5 ms: 8.20x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                             |

Benchmark hidden because not significant (2): nbody, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241218-3.14.0a3+-9015a3f/bm-20241218-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a3+-9015a3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.11x