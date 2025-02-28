# Results vs. 3.12.6

- fork: colesbury
- ref: gh_130382_reftracer_
- machine: linux-x86_64
- commit hash: d15b422
- commit date: 2025-02-28
- overall geometric mean: 1.108x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                      |
| docutils       | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                      |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                      |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                      |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                     |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| nbody          | 89.3 ms                                                | 93.2 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                     |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                      |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                      |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                     |
| xml_etree_process    | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                     |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                     |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.53 ms: 1.05x slower                                                     |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                     |
| genshi_xml      | 50.2 ms                                                | 47.5 ms: 1.06x faster                                                     |
| django_template | 34.7 ms                                                | 33.6 ms: 1.03x faster                                                     |
| mako            | 11.0 ms                                                | 11.3 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 593 ms: 1.87x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                      |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 251 ms: 1.78x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 471 ms: 1.53x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                      |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                     |
| go                         | 139 ms                                                 | 111 ms: 1.25x faster                                                      |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                     |
| spectral_norm              | 110 ms                                                 | 89.4 ms: 1.23x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.56 us: 1.20x faster                                                     |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.68 ms: 1.18x faster                                                     |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                     |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                                      |
| pylint                     | 319 ms                                                 | 275 ms: 1.16x faster                                                      |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                      |
| float                      | 80.8 ms                                                | 70.3 ms: 1.15x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 67.2 ms: 1.14x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                                    |
| chaos                      | 62.8 ms                                                | 55.3 ms: 1.14x faster                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                      |
| deltablue                  | 3.45 ms                                                | 3.04 ms: 1.13x faster                                                     |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                      |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                     |
| logging_simple             | 6.63 us                                                | 5.90 us: 1.12x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                    |
| logging_format             | 7.35 us                                                | 6.64 us: 1.11x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 673 ms: 1.10x faster                                                      |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                      |
| richards                   | 45.9 ms                                                | 41.9 ms: 1.10x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                     |
| logging_silent             | 109 ns                                                 | 99.5 ns: 1.10x faster                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                     |
| pyflate                    | 448 ms                                                 | 409 ms: 1.09x faster                                                      |
| thrift                     | 791 us                                                 | 723 us: 1.09x faster                                                      |
| sqlglot_transpile          | 1.67 ms                                                | 1.53 ms: 1.09x faster                                                     |
| sympy_str                  | 292 ms                                                 | 268 ms: 1.09x faster                                                      |
| richards_super             | 51.9 ms                                                | 47.9 ms: 1.08x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                      |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 64.1 ms: 1.07x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                    |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                      |
| genshi_xml                 | 50.2 ms                                                | 47.5 ms: 1.06x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.5 ms: 1.05x faster                                                     |
| sqlglot_normalize          | 107 ms                                                 | 101 ms: 1.05x faster                                                      |
| meteor_contest             | 104 ms                                                 | 98.4 ms: 1.05x faster                                                     |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 75.2 ms: 1.05x faster                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 50.9 ms: 1.05x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.52 sec: 1.05x faster                                                    |
| sympy_expand               | 468 ms                                                 | 451 ms: 1.04x faster                                                      |
| scimark_fft                | 342 ms                                                 | 330 ms: 1.04x faster                                                      |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                     |
| django_template            | 34.7 ms                                                | 33.6 ms: 1.03x faster                                                     |
| xml_etree_process          | 59.0 ms                                                | 57.5 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                                     |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                     |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| mako                       | 11.0 ms                                                | 11.3 ms: 1.02x slower                                                     |
| nbody                      | 89.3 ms                                                | 93.2 ms: 1.04x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.53 ms: 1.05x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.08x slower                                                     |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                     |
| coverage                   | 71.4 ms                                                | 78.9 ms: 1.11x slower                                                     |
| telco                      | 6.53 ms                                                | 7.27 ms: 1.11x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.14x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.18 ms: 1.21x slower                                                     |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 88.4 ms: 8.19x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                              |

Benchmark hidden because not significant (6): json, mdp, pickle_pure_python, fannkuch, asyncio_websockets, scimark_lu
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-d15b422/bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5+-d15b422.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.12x