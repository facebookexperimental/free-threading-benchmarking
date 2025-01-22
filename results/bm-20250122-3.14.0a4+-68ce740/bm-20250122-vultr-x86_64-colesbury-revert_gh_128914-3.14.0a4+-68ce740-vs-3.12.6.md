# Results vs. 3.12.6

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 252 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 324 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 492 ms: 1.45x faster                                                  |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 207 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.11 sec                                               | 1.91 sec: 1.11x faster                                                |
| xml_etree_parse     | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| xml_etree_iterparse | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| xml_etree_generate  | 85.2 ms                                                | 84.4 ms: 1.01x faster                                                 |
| pickle_pure_python  | 308 us                                                 | 313 us: 1.02x slower                                                  |
| json_loads          | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| json_dumps          | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                 |
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 324 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 492 ms: 1.45x faster                                                  |
| deepcopy                   | 352 us                                                 | 259 us: 1.36x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                 |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                                 |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                 |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.8 ms: 1.17x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.1 ms: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 281 ms: 1.13x faster                                                  |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.3 ms: 1.13x faster                                                 |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.9 ms: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.11x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.11x faster                                                |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.08x faster                                                 |
| thrift                     | 791 us                                                 | 733 us: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 63.7 ms: 1.07x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.17 us: 1.07x faster                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.09 ms: 1.07x faster                                                 |
| richards                   | 45.9 ms                                                | 42.8 ms: 1.07x faster                                                 |
| logging_format             | 7.35 us                                                | 6.89 us: 1.07x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.79 ms: 1.06x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.1 ms: 1.06x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                |
| generators                 | 32.2 ms                                                | 30.6 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 705 ms: 1.05x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.7 ms: 1.05x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.05x faster                                                  |
| pyflate                    | 448 ms                                                 | 428 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 252 ms: 1.04x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 75.6 ms: 1.04x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                                 |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                                |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.03x faster                                                  |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 78.2 ms: 1.02x faster                                                 |
| logging_silent             | 109 ns                                                 | 106 ns: 1.02x faster                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 52.0 ms: 1.02x faster                                                 |
| fannkuch                   | 372 ms                                                 | 366 ms: 1.02x faster                                                  |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 84.4 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                  |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.41 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                 |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                 |
| telco                      | 6.53 ms                                                | 7.18 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 207 ms: 1.12x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.16x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.29 ms: 1.24x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 87.9 ms: 8.14x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (4): unpickle_pure_python, nbody, xml_etree_process, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250122-3.14.0a4+-68ce740/bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x