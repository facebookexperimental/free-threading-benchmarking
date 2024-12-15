# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.129x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 422 ms: 1.08x faster                                                 |
| docutils       | 4.00 sec                                               | 3.56 sec: 1.12x faster                                               |
| html5lib       | 88.9 ms                                                | 84.4 ms: 1.05x faster                                                |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 888 ms: 2.18x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 449 ms: 2.07x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 910 ms: 2.03x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 494 ms: 1.98x faster                                                 |
| async_tree_none            | 741 ms                                                 | 378 ms: 1.96x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 692 ms: 1.56x faster                                                 |
| async_generators           | 589 ms                                                 | 538 ms: 1.09x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                 |
| coroutines                 | 29.5 ms                                                | 30.7 ms: 1.04x slower                                                |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 107 ms: 1.15x faster                                                 |
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                 |
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                |
| regex_compile  | 187 ms                                                 | 167 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 136 ms: 1.24x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 195 ms: 1.23x faster                                                 |
| tomli_loads          | 2.88 sec                                               | 2.51 sec: 1.15x faster                                               |
| xml_etree_generate   | 127 ms                                                 | 112 ms: 1.14x faster                                                 |
| json_loads           | 37.9 us                                                | 33.7 us: 1.13x faster                                                |
| unpickle_pure_python | 300 us                                                 | 287 us: 1.04x faster                                                 |
| json_dumps           | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                         |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                |
| python_startup         | 23.7 ms                                                | 24.7 ms: 1.04x slower                                                |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 28.8 ms: 1.05x faster                                                |
| mako           | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x faster                                                         |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 888 ms: 2.18x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 449 ms: 2.07x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 910 ms: 2.03x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 494 ms: 1.98x faster                                                 |
| async_tree_none            | 741 ms                                                 | 378 ms: 1.96x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 673 ms: 1.64x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 692 ms: 1.56x faster                                                 |
| deepcopy                   | 468 us                                                 | 338 us: 1.38x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 38.6 us: 1.36x faster                                                |
| sqlalchemy_declarative     | 218 ms                                                 | 174 ms: 1.25x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 136 ms: 1.24x faster                                                 |
| comprehensions             | 27.1 us                                                | 21.9 us: 1.24x faster                                                |
| xml_etree_parse            | 241 ms                                                 | 195 ms: 1.23x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                |
| regex_effbot               | 5.13 ms                                                | 4.24 ms: 1.21x faster                                                |
| raytrace                   | 408 ms                                                 | 338 ms: 1.21x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 89.1 ms: 1.20x faster                                                |
| nqueens                    | 117 ms                                                 | 98.1 ms: 1.19x faster                                                |
| pylint                     | 465 ms                                                 | 392 ms: 1.18x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                               |
| deepcopy_reduce            | 4.04 us                                                | 3.51 us: 1.15x faster                                                |
| bench_thread_pool          | 3.48 ms                                                | 3.03 ms: 1.15x faster                                                |
| tomli_loads                | 2.88 sec                                               | 2.51 sec: 1.15x faster                                               |
| float                      | 123 ms                                                 | 107 ms: 1.15x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.77 sec: 1.14x faster                                               |
| xml_etree_generate         | 127 ms                                                 | 112 ms: 1.14x faster                                                 |
| sqlglot_normalize          | 157 ms                                                 | 139 ms: 1.13x faster                                                 |
| json_loads                 | 37.9 us                                                | 33.7 us: 1.13x faster                                                |
| sympy_integrate            | 29.8 ms                                                | 26.5 ms: 1.12x faster                                                |
| go                         | 172 ms                                                 | 153 ms: 1.12x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.56 sec: 1.12x faster                                               |
| scimark_sor                | 167 ms                                                 | 149 ms: 1.12x faster                                                 |
| regex_compile              | 187 ms                                                 | 167 ms: 1.12x faster                                                 |
| logging_simple             | 9.45 us                                                | 8.47 us: 1.12x faster                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 86.7 ms: 1.11x faster                                                |
| pathlib                    | 31.6 ms                                                | 28.5 ms: 1.11x faster                                                |
| scimark_fft                | 500 ms                                                 | 453 ms: 1.10x faster                                                 |
| pyflate                    | 727 ms                                                 | 662 ms: 1.10x faster                                                 |
| async_generators           | 589 ms                                                 | 538 ms: 1.09x faster                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.14 ms: 1.09x faster                                                |
| spectral_norm              | 156 ms                                                 | 142 ms: 1.09x faster                                                 |
| sympy_sum                  | 222 ms                                                 | 204 ms: 1.09x faster                                                 |
| json                       | 6.85 ms                                                | 6.32 ms: 1.08x faster                                                |
| 2to3                       | 456 ms                                                 | 422 ms: 1.08x faster                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.9 ms: 1.08x faster                                                |
| chaos                      | 84.9 ms                                                | 79.0 ms: 1.07x faster                                                |
| richards_super             | 72.8 ms                                                | 67.8 ms: 1.07x faster                                                |
| fannkuch                   | 540 ms                                                 | 504 ms: 1.07x faster                                                 |
| meteor_contest             | 146 ms                                                 | 137 ms: 1.07x faster                                                 |
| dulwich_log                | 100 ms                                                 | 93.8 ms: 1.07x faster                                                |
| typing_runtime_protocols   | 224 us                                                 | 210 us: 1.07x faster                                                 |
| logging_format             | 9.59 us                                                | 9.00 us: 1.07x faster                                                |
| sqlglot_parse              | 1.79 ms                                                | 1.68 ms: 1.06x faster                                                |
| sqlglot_optimize           | 76.0 ms                                                | 71.4 ms: 1.06x faster                                                |
| thrift                     | 1.06 ms                                                | 1.00 ms: 1.06x faster                                                |
| html5lib                   | 88.9 ms                                                | 84.4 ms: 1.05x faster                                                |
| pprint_pformat             | 1.98 sec                                               | 1.88 sec: 1.05x faster                                               |
| mdp                        | 3.97 sec                                               | 3.78 sec: 1.05x faster                                               |
| genshi_text                | 30.2 ms                                                | 28.8 ms: 1.05x faster                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.40 ms: 1.05x faster                                                |
| sympy_str                  | 385 ms                                                 | 369 ms: 1.04x faster                                                 |
| generators                 | 41.1 ms                                                | 39.4 ms: 1.04x faster                                                |
| unpickle_pure_python       | 300 us                                                 | 287 us: 1.04x faster                                                 |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 929 ms: 1.04x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                 |
| scimark_lu                 | 152 ms                                                 | 148 ms: 1.03x faster                                                 |
| richards                   | 60.3 ms                                                | 62.7 ms: 1.04x slower                                                |
| json_dumps                 | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                |
| coroutines                 | 29.5 ms                                                | 30.7 ms: 1.04x slower                                                |
| python_startup             | 23.7 ms                                                | 24.7 ms: 1.04x slower                                                |
| mako                       | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                 |
| coverage                   | 95.4 ms                                                | 105 ms: 1.10x slower                                                 |
| gc_traversal               | 5.86 ms                                                | 7.01 ms: 1.20x slower                                                |
| create_gc_cycles           | 1.94 ms                                                | 3.36 ms: 1.73x slower                                                |
| bench_mp_pool              | 20.7 ms                                                | 90.9 ms: 4.39x slower                                                |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                         |

Benchmark hidden because not significant (12): hexiom, sqlite_synth, genshi_xml, logging_silent, regex_v8, regex_dna, django_template, xml_etree_process, deltablue, sympy_expand, pickle_pure_python, telco
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.129x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.13x