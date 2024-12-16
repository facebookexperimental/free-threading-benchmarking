# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 7b72e7b
- commit date: 2024-12-17
- overall geometric mean: 1.066x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                                     |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 338 ms: 1.64x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 274 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 598 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                    |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.5 ms: 1.02x faster                                                    |
| nbody          | 89.3 ms                                                | 93.9 ms: 1.05x slower                                                    |
| pidigits       | 184 ms                                                 | 219 ms: 1.19x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                    |
| regex_compile  | 142 ms                                                 | 128 ms: 1.11x faster                                                     |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 126 ms: 1.10x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                    |
| json_loads           | 26.5 us                                                | 24.9 us: 1.07x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 85.8 ms: 1.01x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 316 us: 1.03x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                    |
| django_template | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                    |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 601 ms: 1.80x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                                     |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 338 ms: 1.64x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 274 ms: 1.63x faster                                                     |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 598 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.2 us: 1.15x faster                                                    |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                    |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.13x faster                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                     |
| generators                 | 32.2 ms                                                | 28.7 ms: 1.12x faster                                                    |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                     |
| json                       | 5.02 ms                                                | 4.49 ms: 1.12x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 68.7 ms: 1.11x faster                                                    |
| regex_compile              | 142 ms                                                 | 128 ms: 1.11x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 126 ms: 1.10x faster                                                     |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.04 us: 1.10x faster                                                    |
| logging_format             | 7.35 us                                                | 6.73 us: 1.09x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.34 sec: 1.09x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 90.2 ms: 1.07x faster                                                    |
| deltablue                  | 3.45 ms                                                | 3.22 ms: 1.07x faster                                                    |
| thrift                     | 791 us                                                 | 740 us: 1.07x faster                                                     |
| async_generators           | 384 ms                                                 | 359 ms: 1.07x faster                                                     |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                     |
| json_loads                 | 26.5 us                                                | 24.9 us: 1.07x faster                                                    |
| chaos                      | 62.8 ms                                                | 59.1 ms: 1.06x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 65.1 ms: 1.05x faster                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.05x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 75.3 ms: 1.05x faster                                                    |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.91 ms: 1.04x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                                     |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                    |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 718 ms: 1.03x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                   |
| nqueens                    | 80.1 ms                                                | 77.8 ms: 1.03x faster                                                    |
| mdp                        | 2.42 sec                                               | 2.35 sec: 1.03x faster                                                   |
| 2to3                       | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                     |
| float                      | 80.8 ms                                                | 79.5 ms: 1.02x faster                                                    |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                     |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                                     |
| sympy_expand               | 468 ms                                                 | 462 ms: 1.01x faster                                                     |
| sqlglot_normalize          | 107 ms                                                 | 107 ms: 1.00x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 85.8 ms: 1.01x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 522 ms: 1.01x slower                                                     |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                    |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.47 ms: 1.02x slower                                                    |
| django_template            | 34.7 ms                                                | 35.3 ms: 1.02x slower                                                    |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 316 us: 1.03x slower                                                     |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.04x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.46 ms: 1.04x slower                                                    |
| nbody                      | 89.3 ms                                                | 93.9 ms: 1.05x slower                                                    |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 80.0 ms: 1.12x slower                                                    |
| telco                      | 6.53 ms                                                | 7.34 ms: 1.13x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.16x slower                                                    |
| pidigits                   | 184 ms                                                 | 219 ms: 1.19x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 4.41 ms: 1.28x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.71 ms: 1.56x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 85.5 ms: 7.91x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (6): richards, tomli_loads, genshi_xml, sqlglot_optimize, pyflate, richards_super
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241217-3.14.0a2+-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-7b72e7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.11x