# Results vs. 3.12.6

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 7e3de44
- commit date: 2024-12-11
- overall geometric mean: 1.059x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                     |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 624 ms: 1.78x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 631 ms: 1.72x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                     |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 589 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.5 ms: 1.12x faster                                                    |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.7 ms: 1.07x faster                                                    |
| nbody          | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                    |
| pidigits       | 184 ms                                                 | 222 ms: 1.20x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                    |
| regex_compile  | 142 ms                                                 | 133 ms: 1.07x faster                                                     |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.05 sec: 1.03x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                                    |
| pickle_pure_python   | 308 us                                                 | 311 us: 1.01x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 61.1 ms: 1.04x slower                                                    |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.48x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                    |
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                    |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 314 ms: 1.78x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 624 ms: 1.78x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 631 ms: 1.72x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                     |
| async_tree_none            | 464 ms                                                 | 281 ms: 1.65x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                     |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 29.4 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 589 ms: 1.23x faster                                                     |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                                    |
| comprehensions             | 19.8 us                                                | 16.7 us: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 606 ms: 1.18x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                                    |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.66 us: 1.16x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 66.7 ms: 1.15x faster                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                    |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.5 ms: 1.12x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.25 sec: 1.11x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.26 ms: 1.08x faster                                                    |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.1 ms: 1.07x faster                                                    |
| regex_compile              | 142 ms                                                 | 133 ms: 1.07x faster                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.56 ms: 1.07x faster                                                    |
| float                      | 80.8 ms                                                | 75.7 ms: 1.07x faster                                                    |
| genshi_text                | 22.8 ms                                                | 21.4 ms: 1.06x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 700 ms: 1.06x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                   |
| json                       | 5.02 ms                                                | 4.74 ms: 1.06x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.84 ms: 1.06x faster                                                    |
| go                         | 139 ms                                                 | 132 ms: 1.06x faster                                                     |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                                     |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.04x faster                                                     |
| scimark_fft                | 342 ms                                                 | 330 ms: 1.03x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                     |
| mdp                        | 2.42 sec                                               | 2.34 sec: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 76.5 ms: 1.03x faster                                                    |
| nqueens                    | 80.1 ms                                                | 77.7 ms: 1.03x faster                                                    |
| raytrace                   | 299 ms                                                 | 291 ms: 1.03x faster                                                     |
| chaos                      | 62.8 ms                                                | 61.1 ms: 1.03x faster                                                    |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.03x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.46 us: 1.03x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 2.05 sec: 1.03x faster                                                   |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.02x faster                                                     |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                                     |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 52.1 ms: 1.02x faster                                                    |
| logging_format             | 7.35 us                                                | 7.21 us: 1.02x faster                                                    |
| json_loads                 | 26.5 us                                                | 26.1 us: 1.02x faster                                                    |
| pyflate                    | 448 ms                                                 | 450 ms: 1.01x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                    |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 311 us: 1.01x slower                                                     |
| nbody                      | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                    |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                     |
| django_template            | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 70.5 ms: 1.03x slower                                                    |
| thrift                     | 791 us                                                 | 816 us: 1.03x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 61.1 ms: 1.04x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.58 ms: 1.04x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.60 ms: 1.05x slower                                                    |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                    |
| telco                      | 6.53 ms                                                | 7.29 ms: 1.12x slower                                                    |
| richards_super             | 51.9 ms                                                | 58.4 ms: 1.13x slower                                                    |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                    |
| pidigits                   | 184 ms                                                 | 222 ms: 1.20x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.27 ms: 1.24x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.48x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 88.8 ms: 8.22x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                             |

Benchmark hidden because not significant (1): fannkuch
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241211-3.14.0a2+-7e3de44/bm-20241211-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-7e3de44.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.11x